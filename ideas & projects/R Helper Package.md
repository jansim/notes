
Function
```R
helpeR::whatswrong()

helpeR::lastCommand()

helpeR::helpKnit()

statProg::help()
```

#### Pass on
- error message
- current code chunk (if Rmd) / last statement (or X lines of code if possible)
- environment variable names
- working directory name
	- with ~ replaced for privacy
- working directory file names
	- only if not in home directory
	- including first level of dir contents?
- Extra info via rstudio api??


#### other stuff
- Needs proxy server (maybe also to verify message format?)
	- and to not leak API key
- 

