# Frequently Asked Questions

- [R plugin in Pycharm](#r-plugin-in-pycharm)
  - [argument encoding="UTF-8" is ignored in MBCS locales](#argument-encodingutf-8-is-ignored-in-mbcs-locales)

## R plugin in Pycharm
### argument encoding="UTF-8" is ignored in MBCS locales

1. **Why**: The encoding is not supported.  
2. **How**: Run `Sys.setlocale(category = 'LC_CTYPE', locale = 'C')` in the R Console.  
3. **Further Question**: It is not permanent. You need to run the above code in the R console when restarting Pycharm.  


### how to automatically add binder files

Use the "holepunch" package. R codes as below:

```R
remotes::install_github("karthik/holepunch")  # install package
holepunch::write_runtime()  # create a runtime.txt in the .binder/ directory
holepunch::write_install()  # automatically add the code to install all dependencies in the project
```