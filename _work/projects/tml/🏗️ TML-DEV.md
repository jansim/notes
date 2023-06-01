- [x] Create jsPsych Singleton somehow
- [ ] Send Ticket to Kraig

## iFrames

### Pros
- Games can use different jsPsych Versions
- Easier support for legacy games
- More standalone / less pushkinifaction necessary

### Cons
- For different jsPsych versions we'll need different versions of covariates etc.
- Harder debugging (since we need to communicate w/ iFrame)
- From jsPsych 7+ we *might* be able to have concurrent, different major versions (to a certain degree)

=> It all comes down to common covariates



- [ ] Is Headphone check working everywhere?

## Changes in Data in jsPsych v7
- button_pressed -> response
- 