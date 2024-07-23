[![Upload Python Package](https://github.com/myridia/django-auto-translator/actions/workflows/publish.yml/badge.svg)](https://github.com/myridia/django-auto-translator/actions/workflows/publish.yml)


# ![django-deep-translator](img/django-deep-translator.png ) django-auto-translator  

Autotranslate django `.po` translation files package built on top of  [deep-translator](https://pypi.org/project/deep-translator/)

Finds all the generated pot (.po) files under the locale paths (LOCALE_PATHS) specified in django project settings, and translates them automatically with default source language as **english**.



## Install 

### Install via PIP 

```bash
  pip install django-auto-translator
  ```

## Add `'django-auto-translator'` to your `INSTALLED_APPS` setting:

```py
INSTALLED_APPS = (
 ...
 'django-auto-translator',
 )

```

## Command translate to all  languages 

```bash 
python manage.py translate_messages
```

## Option Parameter
- ``-f, --set-fuzzy``: Set the 'fuzzy' flag on autotranslated entries
- ``-l, --locale 'locale'``: Only translate the specified locales
- ``-u, --untranslated``: Only translate the untranslated messages
- ``-s, --source-language``: Override the default source language (en) used for translation
- ``-S, --silent``: Don't show the verbose output
- ``-t, --throttle``: Throttle the maximum of seconds for the next translate request(default=10 sec)
         

### Example:
```bash
    python manage.py translate_messages -l 'de' -l 'es'
```

## Important Django Language Setting

In your settings, list the relative path to locale folders, example:

```py
LOCALE_PATHS = (
    'locale',
    'home/locale',
    'products/locale',
    'services/locale',
)
```



---

## Credits

Forked from:  https://github.com/wmo-raf/django-deep-translator

Artwork Logo from Eypros: https://openclipart.org/artist/Eypros 
