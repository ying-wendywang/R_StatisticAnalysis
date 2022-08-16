# Frequently Asked Questions

- [R plugin in Pycharm](#r-plugin-in-pycharm)
  - [argument encoding="UTF-8" is ignored in MBCS locales](#argument-encodingutf-8-is-ignored-in-mbcs-locales)

## R plugin in Pycharm
### argument encoding="UTF-8" is ignored in MBCS locales

> **原因**：编码不支持。  
> 
> **解决**：`Sys.setlocale(category = 'LC_CTYPE', locale = 'C')`  
> 
> **问题**：无法永久解决，需要每次都在 R Console 中输入