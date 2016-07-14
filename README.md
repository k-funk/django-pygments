django-pygments
===============

django-pygments is a Django app that provides a template tag and 2 filters for doing syntax highlighting with [Pygments](http://pygments.org/).

#### Dependencies:
- pygments

#### Installation:
- Add `django_pygments` to your project directory and to `INSTALLED_APPS` in your `settings.py`
- If you want to see the integrated demo page, add a urls.py entry and copy/link the media files in the proper dir

#### Usage:
- Enclose your code snippet in a pre tag with the non-standard "lang" attribute set to a supported language like this:
  `<pre lang="python">....</pre>`
- [See the view and demo](django_pygments/templates/django_pygments/demo.html) template for examples on how to use the `pygmentify` and `pygmentify_inline` filters (the later is rather useful for RSS feeds) or the `pygment` tag
- While using the `pygment` template tag, you can pass keyword arguments that you would pass to Pygments HtmlFormatter class constructor by passing them as with keyword arguments along with the pygment tag. Look at demo template for examples. There is one caveat with this feature still. You can only pass Python values as argument values (like Strings wrapped within quotes or True or False boolean values, etc.). It doesn't support Django template/context variables as arguments yet.

#### Notes:
- The custom HTML formatter class displays each line as an ordered list element, thus implementing line numbering without interfering with copy/pasting
- To see a list of supported languages, look at the `lexer_names` variable in utils.py

The project's site is here: [od-eon.com/labs/django-pygments/](http://od-eon.com/labs/django-pygments/).
For technical support use the github issue tracker or contact us at developers@od-eon.com

