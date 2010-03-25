!SLIDE
# Scene II
## Databasing

!SLIDE bullets
# Documents
* JSON-formatted
* Each has \_id and \_rev properties
* GET, POST, PUT, DELETE

!SLIDE bullets
# Design Documents
* Normal docs, magic properties
* \_id starts with "_design/"
* Store many things, including attachments

!SLIDE bullets
# Views
* Map/Reduce
* Written in JS
* Generated _independent_ of client state

!SLIDE bullets
# Show functions
* Transforms a single document for output to the client
* Has access to request parameters and user

!SLIDE bullets
# List functions
* Transforms a view for output to the client
* Has access to request parameters and user

!SLIDE bullets
# Update functions
* Transforms posted documents before saving

!SLIDE bullets
# Changes feeds
* Outputs all the changes to a given db
* One-off, long-polling or continuous feed
* Optionally filtered
* Comet, anyone?
