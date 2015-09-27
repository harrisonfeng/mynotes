# Redis Essentials


## Redis data types

### Strings

A string can behave as an integer, float, text string, or bitmap based on its 
value and the commands used. It can store any kind of data: text(XML, JSON, 
HTML, or raw text), integers, floats, or binary data(videos, images, or audio 
files). A string value cannot exceed 512M of text or binary data.

The following are some use cases for strings:

* *Cache mechanisms:* It is possible to cache text or binary data in Redis, 
which could be anything for HTML pages and API responses to images and videos.
A simple cache system can be implemented with the commands *SET*, *GET*, 
*MSET*, and *MGET*.
* *Cache with automatic expiration:* String combined with automatic key 
expiration can make a robust cache system using the commands *SETEX*, *EXPIRE*, 
and *EXPIREAT*. This is very useful when database queries take a long time to 
run and can be cached for a given period of time. Consequently, this avoids 
running those queries too frequently and can give a performance boost to 
application.
* *Counting:* A counter can easily be implemented with strings and the 
commands *INCR* and *INCRBY*. Good examples of counters are pages views, 
video views, and likes. Strings also provide other counting commands, such 
as *DECR*, *DECRBY* and *INCRFLOATBY*.
