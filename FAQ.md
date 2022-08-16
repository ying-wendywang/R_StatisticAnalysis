# Frequently Asked Questions

- [R plugin in Pycharm](#r-plugin-in-pycharm)
  - [argument encoding="UTF-8" is ignored in MBCS locales](#argument-encodingutf-8-is-ignored-in-mbcs-locales)

## R plugin in Pycharm
### argument encoding="UTF-8" is ignored in MBCS locales

> **Why**: The encoding is not supported.  
> 
> **How**: Run `Sys.setlocale(category = 'LC_CTYPE', locale = 'C')` in the R Console.  
> 
> **Further Question**: It is not permanent. You need to run the above code in the R console when restarting Pycharm.  