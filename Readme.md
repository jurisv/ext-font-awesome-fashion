# font-awesome

This package bundles Font Awesome for use by Sencha Cmd applications and packages.
To use this package, simply require it from `app.json`:

    "requires": [
        "font-awesome"
    ]

See the Font Awesome [web page](https://fontawesome.com/v4.7.0/) for
more details.


This version of the package is enhanced with option to selectively pick only icons that are used in the application.


To find icons used by your application run this command from the app root folder

```
find . -type f -exec cat {} + | grep -a -o 'fa-[a-zA-Z0-9-]*' | sort -u
```

By default all icons will be excluded.
Set $ext-use-all-fa-icons to true to override this:
```
$ext-use-all-fa-icons: true;
```

To enable icon that is being used by application, construct the variable as from icon name and prefix it with 'ext-use-' and set it to true, for example: 
```
$ext-use-fa-search: true;
```