# How to use


Build a new site

Create a New Lotus Docs Site 


With Hugo installed, create a new Hugo project using the hugo new command:
```
hugo new site demo4 && cd demo4

```

Now initialize your project as a Hugo Module using the hugo mod init command:

hugo mod init demo4

info



git clone https://github.com/maniak-academy-courses/main themes/main

Edit the hugo.toml configuration file to include the Lotus Docs theme and the Hugo Bootstrap module (lines 5 to 14 below):



baseURL = 'http://example.org/'
languageCode = 'en-us'
title = 'My New Hugo Site'

[module]
    # uncomment line below for temporary local development of module,
    # when using a 'theme' as a git submodule or git cloned files
    replacements = "github.com/sebbycorp/demo3 -> demo3"
    [[module.imports]]
        path = "github.com/sebbycorp/demo3"
        disable = false
    [[module.imports]]
        path = "github.com/gohugoio/hugo-mod-bootstrap-scss/v5"
        disable = false