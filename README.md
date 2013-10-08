# pelican-iliork

A theme for [pelican][], inspired by [pelican-elegant][], bulit on [Bootstrap][]. Have a live demo at [iliork][]. Now or then, I'll try out some Bootstrap theme together with pelican-iliork. For the Bootstrap theme support feature of pelican-iliork, see below.

# Features
## Author link customization

    AUTHORS = {
        u'jack': '/about.html',
        u'mary': 'http://mary.info',
    }

## Bootstrap theme support 

You can change the default appearance of Bootstrap to any Bootstrap theme you like. Have a look at [Bootswatch][]

    B3_THEME = '//netdna.bootstrapcdn.com/bootswatch/3.0.0/flatly/bootstrap.min.css'

## Use your own code highlight css

    CODE_HIGHLIGHT = '/theme/css/solarized-light.css'

## Nested MENUITEMS

For now, only 1-level nesting is allowed. More nesting seems not clean

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

## Support for Google custom search

Put following in your MENUITEMS to have a search box on top navbar. 'Search' is the key, mandatory.
    
    MENUITEMS = [
        ('Search', 'your Google custom search value'),
        ]
    
[pelican]: https://github.com/getpelican/pelican
[pelican-elegant]: https://github.com/talha131/pelican-elegant
[Bootstrap]: http://getbootstrap.com
[iliork]: http://blog.iliork.com
[Bootswatch]: http://bootswatch.com
[Flatly]: http://bootswatch.com/flatly/
