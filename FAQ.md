# Frequently Asked Questions

- [R plugin in Pycharm](#r-plugin-in-pycharm)
  - [argument encoding="UTF-8" is ignored in MBCS locales](#warning-argument-encodingutf-8-is-ignored-in-mbcs-locales)
  - [how to automatically add binder files](#how-to-automatically-add-binder-files)

- [R usages](#r-usages)
  - [how to list available datasets in R?](#how-to-list-available-datasets-in-r)

## R plugin in Pycharm
### Warning: argument encoding="UTF-8" is ignored in MBCS locales

1. **Why**: The encoding is not supported.  
2. **How**: Run `Sys.setlocale(category = 'LC_CTYPE', locale = 'C')` in the R Console.  
3. **Further Question**: It is not permanent. You need to run the above code in the R console when restarting Pycharm.  


### How to automatically add binder files?

Use the "holepunch" package. Run R codes as below:

```
remotes::install_github("karthik/holepunch")  # install package
holepunch::write_runtime()  # create a runtime.txt in the .binder/ directory
holepunch::write_install()  # automatically add the code to install all dependencies in the project
```

## R Usages
### How to list available datasets in R?

```
data()  # list built-in datasets in R
data(package = "MASS")  # list available datasets in a downloaded package, e.g., "MASS"
```

### How to assign a new name when import a built-in dataset?

```
data("cars")  # first, import a built-in dataset named in "cars"

# method 1
data <- get("cars")  # then, rename it into "data".

# method 2
assign("data", cars)  # rename it into "data"
```