# Django Inline SASS #

Potentially improve SEO and reduce CSS include bloat by inlining page-specific SASS.

## Sample usage ##

```
{% load inline_sass %}

{% sass %}
@import 'myapp/variables';

.description {
  font-weight: 300;
  p {
      font-size: 105%;
      color: $some-color-from-include;
  }
  h1 {
    text-transform: uppercase;
  }
}
{% endsass %}

```


## @import ##

Import paths are set up exactly like Django template paths. Put app specific SASS files within a 'sass/app_name' directory inside of the app. In the sample usage above, you would creae a `_variables.scss` file inside `myapp/sass/myapp`.

## Installation ##

`pip install django-inline-sass` and put `django_inline_sass` inside your `settings.py` `INSTALLED_APPS`.
