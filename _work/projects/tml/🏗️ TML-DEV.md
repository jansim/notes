
- Using a different prerenderer
	- https://github.com/Tofandel/prerenderer ??

- IP Ranges
	- LMU: https://doku.lrz.de/vpn-technik-10745907.html ![[Screenshot 2023-06-14 at 17.49.34.png]]
	- Yale
		- Yale's IP addresses are 130.132.0.0/16 and 128.36.0.0/16
	- Auckland
		- 130.216.0.0/16
		- 202.36.244.0/24
		- 202.37.88.0/24


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