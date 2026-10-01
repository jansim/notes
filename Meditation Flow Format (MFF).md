# Meditation Flow Format (MFF) Specification v1.0

## 1. Overview

The **Meditation Flow Format (MFF)** is a recursive, JSON-based standard for defining non-linear audio sessions. It is designed to support complex sequencing, such as randomized guidance, optional segments, and variable silence intervals (pauses) between snippets.

## 2. Core Concepts

### 2.1 The Tree Structure

The file describes a tree where:

- **Root:** The entry point of the session.
    
- **Group:** A branch node that contains a list of children. It defines _how_ those children are played (sequentially, shuffled, or sampled).
    
- **Phrase:** A leaf node representing a concrete piece of media (audio/text).
    

### 2.2 Timing & Silence

Durations and pauses are strictly defined in **milliseconds (ms)**.

- **Duration:** The exact length of the audio file.
    
- **Pause (Post-Roll):** A variable amount of silence to generate _after_ a node finishes but _before_ the next one begins.
    

### 2.3 Selection Logic

Nodes can be marked as **Required** or **Optional**. This flag interacts with the parent Group's strategy (specifically `sample`) to determine which nodes are selected for the final playlist.

## 3. JSON Schema

### 3.1 Root Object

The top-level object containing metadata and the content tree.

|Field|Type|Required|Description|
|---|---|---|---|
|`meta`|Object|Yes|Global metadata and defaults.|
|`root`|Node (Group)|Yes|The entry point of the session structure.|

### 3.2 Meta Object

Contains session info and global configuration defaults.

|Field|Type|Description|
|---|---|---|
|`title`|String|The human-readable title of the session.|
|`author`|String|The creator of the content.|
|`version`|String|Schema version (e.g., "1.1").|
|`default_phrase_pause`|[PauseConfig](https://www.google.com/search?q=%2333-pauseconfig-object "null")|**Phrase Default.** Applied to any **Phrase** Node that does not define its own pause.|
|`default_group_pause`|[PauseConfig](https://www.google.com/search?q=%2333-pauseconfig-object "null")|**Group Default.** Applied to any **Group** Node that does not define its own pause.|

### 3.3 PauseConfig Object

Defines a variable duration of silence.

|Field|Type|Description|
|---|---|---|
|`min`|Integer|Minimum silence in ms.|
|`max`|Integer|Maximum silence in ms.|

_Note: If `min` equals `max`, the pause is constant._

### 3.4 Node Object (Common Fields)

These fields exist on both **Groups** and **Phrases**.

|Field|Type|Default|Description|
|---|---|---|---|
|`type`|String|-|Enum: `"group"`|
|`id`|String|-|Unique identifier (optional, for logging/debugging).|
|`required`|Boolean|`false`|**Selection Priority.** See [Logic Section](https://www.google.com/search?q=%234-logic-and-behavior "null").|
|`pause`|[PauseConfig](https://www.google.com/search?q=%2333-pauseconfig-object "null")|`null`|Overrides the type-specific default pause. Defines silence _after_ this node.|

### 3.5 Group Node (Specific Fields)

A container for other nodes.

|Field|Type|Description|
|---|---|---|
|`strategy`|String|Enum: `"sequence"`|
|`children`|Array<Node>|List of child nodes.|
|`sample_count`|Int|Range|

### 3.6 Phrase Node (Specific Fields)

The actual content leaf.

|Field|Type|Description|
|---|---|---|
|`text`|String|The transcript or text to display.|
|`audio`|String|Filename of the audio file (e.g., `step_1.mp3`).|
|`duration_ms`|Integer|Exact duration of the audio file.|

## 4. Logic and Behavior

### 4.1 Sampling Strategy & Required Nodes

When a Group has `strategy: "sample"`, it must select `N` items from its `children`. The `required` flag dictates priority:

1. **Bucket Sort:** Children are split into **Required** and **Optional** pools.
    
2. **Mandatory Inclusion:** All **Required** nodes are added to the selection first.
    
    - _Edge Case:_ If the number of Required nodes > `sample_count`, the player should cap at `sample_count` (taking the first available required nodes) and log a warning, OR strictly enforce all required nodes (implementation dependent).
        
3. **Filling the Rest:** If the selection is not full (count < `sample_count`), the remaining slots are filled by randomly picking from the **Optional** pool.
    

### 4.2 Pause Inheritance

The logic for determining the final pause duration for a Node is as follows:

1. **Local Override:** If the Node (Group or Phrase) has a local `pause` object defined, use it.
    
2. **Type Default:** If the local `pause` is missing or `null`:
    
    - If `type` is `"phrase"`, use `meta.default_phrase_pause`.
        
    - If `type` is `"group"`, use `meta.default_group_pause`.
        
3. **Group Pauses:** A pause on a Group node occurs _after_ the entire group has finished playing, not between its children.
    
4. **Phrase Pauses:** A pause on a Phrase node occurs _after_ that specific phrase.
    

## 5. Example File

This example demonstrates:

- Separate global defaults: Phrases have a longer default pause (3-5s), Groups have a very short one (0.5-1s).
- A **Sample Group** ("Body Scan") that _must_ include the "Torso" (Required), but picks random limbs (Optional) to fill the rest.
- Local pause overrides on the Intro phrase.
    

<!-- end list -->

```
{
  "meta": {
    "title": "Flexible Focus",
    "author": "Mindful Tech",
    "version": "1.1",
    "default_phrase_pause": { "min": 3000, "max": 5000 },
    "default_group_pause": { "min": 500, "max": 1000 }
  },
  "root": {
    "type": "group",
    "strategy": "sequence",
    "children": [
      {
        "id": "intro",
        "type": "phrase",
        "required": true,
        "text": "Let's settle in.",
        "audio": "intro.mp3",
        "duration_ms": 3000,
        "pause": { "min": 500, "max": 1000 }
      },
      {
        "id": "body_scan_section",
        "type": "group",
        "strategy": "sample",
        "sample_count": { "min": 2, "max": 3 },
        "children": [
          {
            "id": "torso_core",
            "type": "phrase",
            "required": true,
            "text": "Center your attention on your chest.",
            "audio": "torso.mp3",
            "duration_ms": 5000
          },
          {
            "id": "hand_L",
            "type": "phrase",
            "required": false,
            "text": "Notice your left hand.",
            "audio": "hand_l.mp3",
            "duration_ms": 4000
          },
          {
            "id": "hand_R",
            "type": "phrase",
            "required": false,
            "text": "Notice your right hand.",
            "audio": "hand_r.mp3",
            "duration_ms": 4000
          },
          {
            "id": "feet",
            "type": "phrase",
            "required": false,
            "text": "Feel your feet on the floor.",
            "audio": "feet.mp3",
            "duration_ms": 4000
          }
        ]
      },
      {
        "id": "outro",
        "type": "phrase",
        "required": true,
        "text": "Namaste.",
        "audio": "outro.mp3",
        "duration_ms": 2000
      }
    ]
  }
}
```

### Example Logic Trace

In the "Body Scan Section" above, let's assume the randomizer picks a `sample_count` of **2**:

1. **Slot 1:** The logic identifies `torso_core` is `required: true`. It is added immediately.
    
2. **Slot 2:** The logic randomly picks **one** item from the remaining optional pool (`hand_L`, `hand_R`, `feet`).
    
3. **Result:** The user hears "Center your attention..." followed by one random limb.