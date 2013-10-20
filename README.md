# Pelican-iliork

A theme for [pelican][], inspired by [pelican-elegant][]. It's bulit on [Bootstrap][], version 3.0.0. I try to follow the [KISS][] and [DRY][] principle, while providing readability.

Pelican-iliork adopted a single column design due to simplicity and readability. But it can be extended to a double or triple column design easily. You can checkout out the source code or simply `Inspect Elemnt` in your favorite browser; you can see there are blank left and right sidebar. 

You can get a live demo at [iliork][], my personal blog, mainly in Chinese. Now or then, I'll try out some Bootstrap theme together with pelican-iliork. For the Bootstrap theme support feature of pelican-iliork, see below.

# Features
## Bootstrap theme support 

You can change the default appearance of Bootstrap to any Bootstrap theme you like. `BS3_THEME` defined the url of the theme's css file; `BS3_THEME_NAME` and `BS3_THEME_HOMEPAGE`, used in the footer, defined the title and title to the theme's homepage. Have a look at [Bootswatch][]

    BS3_THEME = '//netdna.bootstrapcdn.com/bootswatch/3.0.0/flatly/bootstrap.min.css'
    BS3_THEME_NAME = 'Flatly'
    BS3_THEME_HOMEPAGE = 'http://bootstrap.com/flatly'

## Use your own code highlighting css

    CODE_HIGHLIGHT = 'url to your favorite code highlight css'

## Nested menu items support

Nested menu items are put together as a drop-down button on the top navbar. Only 1-level nesting is allowed, because I think it's unnecessary and clumsy to have too much nesting in menu items.

    MENUITEMS = [
        ('Home', '/'),
        ('Archives', [
            ('Tags', '/tags.html'),
            ('Categories', '/categories.html'),
            ('Archives', '/archives.html'),
            ]),
        ('Social', [
            ('Email', 'url to your email'),
            ('Github', 'url to your github'),
            ('Facebook', 'url to your facebook'),
            ]),
        ]

## Built-in support for Google custom search

Put following in your MENUITEMS to have a search box on top navbar. 'Search' is the key, mandatory.
    
    MENUITEMS = [
        ('Search', 'your Google custom search value'),
        ]
    
## Multi-author support

You can direct the author link to whatever you want. It's not hard-coded in the theme.

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
