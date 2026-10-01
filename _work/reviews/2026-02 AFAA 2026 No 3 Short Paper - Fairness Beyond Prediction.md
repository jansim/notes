- no refererences; as these do not count towards page limit I see no excuse not to reference prior literature??


## Title
From Static to Dynamic Evaluation

## Summary
The short paper discusses how evaluation / alignment needs to be treated differently for agentic and continuously updating systems as opposed to "classic" prediction settings. In particular, the paper poses the question of how principles and tools of algorithmic need to evolve / adapt for AI systems which are able to adapt and act (beyond just prediction). They argue that in this context, fairness needs to be evaluated across the alignment pipeline ifself. After briefly describing failure modes of existing approaches, the paper introduces a small framework comprised of three stages.

## Strengths
- The central question of the short paper, how fairness should evolve for agentic settings beyond prediction, is interesting and worthy of examination.
- Relatedly, using the alignment *pipeline* as a lense of examination seems like a worthwhile idea and the central conclusion of the paper, that the fairness of agentic AI systems should be seen as a dynamic property makes sense.


## Weaknesses
- The short paper does not provide any references. As references do not count towards the page limit, I do not see any compelling reason as to why the authors made this choice. Referencing prior work is foundational to the academic process and I believe this work would benefit from stronger engagement with the literature.
	- This is the only short paper I am reviewing, so I double checked the CfP to confirm that references in short papers are allowed (if not, I would welcome a correction by one of the chairs or the authors and would update my review accordingly).
- Relatedly many of the claims in the short paper are wide ranging and not supported. Oftentimes single examples are used to argue its case without addressing alternatives at all (e.g. L063 onwards, L079 onwards, ...).
- The paper is quite vague and does not concretely define the scope of its framework. Does this apply to any agentic system, to any decision making system, to any decision making system with agentic properties? Terminology is not clearly defined, nor are concrete examples provided. What is the understanding of an agentic system in this case? What does fairness of such a system mean?
- While multiple examples and points are provided it seems the central conclusion of the paper is that continuously running and potentially self-updating systems need to also be continuously evaluated. This conclusion, however, has already been proposed and discussed in large bodies of prior work.


### Rating
1 or 2

### Confidence
3 or 4
