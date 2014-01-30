# Pelican-iliork

Pelican-iliork is a single-column theme for [pelican][], targeting at blog writing. The primary goal of pelican-iliork is to provide simplicity and readability.

Pelican-iliork is built on [Bootstrap][] version 3.0. Some notable features are:

- Support for bootstrap theme
- Support for self-configurable code highlighting CSS
- Support for nestable menu items
- Support for Google custom search
- Support for multi-author

You can get a live demo at [iliork][], my personal blog, mainly in Chinese.

# Features
## Bootstrap theme

You can change the default appearance of Bootstrap to any Bootstrap theme you like. `BS3_THEME` defines the url of the theme's css file; `BS3_THEME_NAME` and `BS3_THEME_HOMEPAGE` define the name and url, used in the footer, of bootstrap theme. Have a look at [Bootswatch][].

    BS3_THEME = '//netdna.bootstrapcdn.com/bootswatch/3.0.0/flatly/bootstrap.min.css'
    BS3_THEME_NAME = 'Flatly'
    BS3_THEME_HOMEPAGE = 'http://bootstrap.com/flatly'

## Use your own code highlight CSS

You can use your own css file for code highlight. If you do not provide this value, pelican-iliork will the default css file, `code.css`.

    CODE_HIGHLIGHT = 'url to your favorite code highlight css'

## Nestable menu items

Menu items in pelican-iliork is nestable. `MENUITEMS` are rendered as a top navbar. Nested menu items are rendered together as a drop-down button on the top navbar. But only 1-level nesting is allowed; it's clumsy, and perhaps wrong, to nest too much items in the menu. Here's a example.

    MENUITEMS = [
        ('Home', '/'),
        ('Archives', [
            ('Tags', '/tags.html'),
            ('Categories', '/categories.html'),
            ('Chronological', '/archives.html'),
            ]),
        ('Social', [
            ('Email', 'url to your email'),
            ('Github', 'url to your github'),
            ('Facebook', 'url to your facebook'),
            ]),
        ]

## Google custom search

Put following in your MENUITEMS to have a Google custom search box on top navbar. 'Search' is the key, mandatory.

    MENUITEMS = [
        ('Search', 'your Google custom search value'),
        ]

## Multi-author
You can direct the author link to whichever you want. It's not hard-coded in the theme.

    AUTHORS = {
        u'jack': '/about.html',
        u'mary': 'http://mary.info',
        u'tony': 'http://tony.me',
    }


[pelican]: https://github.com/getpelican/pelican
[pelican-elegant]: https://github.com/talha131/pelican-elegant
[Bootstrap]: http://getbootstrap.com
[KISS]: http://en.wikipedia.org/wiki/KISS_principle
[DRY]: http://en.wikipedia.org/wiki/Don%27t_Repeat_Yourself
[iliork]: http://blog.iliork.com
[Bootswatch]: http://bootswatch.com
[Flatly]: http://bootswatch.com/flatly/
