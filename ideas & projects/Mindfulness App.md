> Automatically generate a vast number of meditations using a small body of phrases. Allow for completely flexible setting of meditation duration.

- Different classes of meditaitons
	- Mindfulness
	- Only minimally guided relaxation
	- (progressive) Body Relaxation
	- Lower Prio
		- Loving Kindness
		- More visualisation based ones with a story etc.
- Make meditations within a class different enough to not get boring, but similar enough to be predictable => you know what you gets

## First Ideas
-   Categories of phrases
-   Test Recording quality
-   Find transcripts of meditations
-   Find course on how to guide a meditation

# Steps: MVP
1. Get a list of N = 10 youtube videos re guided mindfulness meditations
2. Scrape their transcripts via https://pypi.org/project/youtube-transcript-api/
3. Identify useful phrases and record them
4. Built a prototype function that takes in a duration + seed and outputs a meditation

## Related
- https://medium.com/@nfonseca85/ai-generated-guided-meditations-with-gpt-2-5d3d187ead2