#occ 

- [x] Please write references in the description of the DESCRIPTION file in the form  
authors (year) <doi:...>  
with no space after 'doi:' and angle brackets for auto-linking.  
(If you want to add a title as well please put it in quotes: "Title")  
-> Please only put the year in brackets, not the authors as well.  
  
- [x] "Using foo:::f instead of foo::f allows access to unexported objects. This is generally not recommended, as the semantics of unexported objects may be changed by the package author in routine maintenance."  
Please omit one colon.  
Used ::: in documentation:  
     man/get_page_data.Rd:  
        if (interactive()) {  
 occupationMeasurement:::get_page_data(session = session, key = "user_answer")  
}  
     man/set_page_data.Rd:  
        occupationMeasurement:::set_page_data(session = session, page_id = "example", values = list(user_answer = "Some User Answer"))  
  
You have examples for unexported functions. Please either omit these examples or export these functions.  
Examples for unexported function  
  get_job_suggestions() in:  
     get_page_data.Rd  
  set_item_data() in:  
     set_page_data.Rd  
  
- [x] \dontrun{} should only be used if the example really cannot be executed (e.g. because of missing additional software, missing API keys, ...) by the user. That's why wrapping examples in \dontrun{} adds the comment ("# Not run:") as a warning for the user.  
Does not seem necessary.  
Please unwrap the examples if they are executable in < 5 sec, or replace \dontrun{} with \donttest{}.  
  
Please ensure that your functions do not write by default or in your examples/vignettes/tests in the user's home filespace (including the package directory and getwd()). This is not allowed by CRAN policies.  
Please omit any default path in writing functions. In your examples/vignettes/tests you can write to tempdir().  
  
- [x] Please make sure that you do not change the user's options, par or working directory. If you really have to do so within functions, please ensure with an ***immediate*** call of on.exit() that the settings are reset when the function is exited. e.g.:  
...  
oldpar <- par(no.readonly = TRUE)    # code line i  
on.exit(par(oldpar))            # code line i + 1  
...  
par(mfrow=c(2,2))            # somewhere after  
...  
  
...  
old <- options()         # code line i  
on.exit(options(old))      # code line i+1  
...  
options(digits = 3)  
...  
e.g.: R/model_training.R ; R/app.R  
If you're not familiar with the function, please check ?on.exit. This function makes it possible to restore options before exiting a function even if the function breaks. Therefore it needs to be called immediately after the option change within a function.  
  
Please do not modifiy the .GlobalEnv. This is not allowed by the CRAN policies. e.g.: tests/testthat/helper.R