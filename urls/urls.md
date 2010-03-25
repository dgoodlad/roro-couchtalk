!SLIDE
# Scene III
## Ooooh Pretty
### (urls)

!SLIDE bullets
* http://localhost:5984/roro/\_design/roro/index.html
* http://localhost:5984/roro/\_design/roro/\_views/topics?startkey=234
* .../roro/\_design/roro/\_list/html/topics

!SLIDE bullets
# Yuck
* Functional
* ... but not pretty

!SLIDE
# Proxy?
## Nah!

!SLIDE
# Rewrites

!SLIDE code smaller
    @@@ javascript
    [
      { "from": "", "to": "index.html" },
      { "from": "/robots.txt", "to": "robots.txt" },
    
      { "from": "/topics", "to": "/_list/html/topics" },
    
      { "from": "/db/*", "to":   "../../*" },
      { "from": "/_session", "to":   "../../../_session" },
    
      { "from": "/images/*", "to": "images/*" },
      { "from": "/stylesheets/*", "to": "stylesheets/*" },
      { "from": "/javascripts/*", "to": "javascripts/*" }
      { "from": "/vendor/*", "to": "vendor/*" },
      { "from": "/_utils/script/:script.js",
        "to":   "../../../_utils/script/:script.js" },
    ]

!SLIDE bullets
# Still not _quite_ right
* http://.../roro/\_design/roro/\_rewrite/topics

!SLIDE bullets
# Vhosts!
## Proxy?
### Nah!

!SLIDE code smaller
# local.ini:
    [vhosts]
    roro.local:5984 = /roro/_design/roro/_rewrite

!SLIDE commandline
# Ahhhhh
    $ curl -X GET http://roro.local/index.html
    <!DOCTYPE html>
    <html>
      <head>
        <title>Generated CouchApp</title>
        ...

