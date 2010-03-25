!SLIDE
# Scene I
## The Basics

!SLIDE bullets
# Four-letter ... words
* HTTP
* REST
* JSON

!SLIDE
# Curl up

!SLIDE incremental commandline
    $ export DB=http://localhost:5984

    $ curl -X GET $DB/
    {"couchdb":"Welcome","version":"0.11.0b15d10793-git"}

!SLIDE bullets
# Couchapp
## http://github.com/couchapp/couchapp

!SLIDE incremental commandline
    $ couchapp generate app roro && cd roro
    $ couchapp push
    [INFO] database roro created.
    [INFO] Visit your CouchApp here:
    http://localhost:5984/roro/_design/roro/index.html

!SLIDE commandline
    $ ls -1
    _attachments/
    _id
    couchapp.json
    lists/
    shows/
    updates/
    vendor/
    views/

!SLIDE incremental commandline
    $ curl -X GET $DB/roro/_design/roro/index.html
    <!DOCTYPE html>
    <html>
      <head>
        <title>Generated CouchApp</title>
        ...

!SLIDE
# Hooray!
## A complicated, but functional static web server
