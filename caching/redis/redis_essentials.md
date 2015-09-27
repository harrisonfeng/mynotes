# Redis Essentials


## Redis data types

### Strings

A string can behave as an integer, float, text string, or bitmap based on its 
value and the commands used. It can store any kind of data: text(XML, JSON, 
HTML, or raw text), integers, floats, or binary data(videos, images, or audio 
files). A string value cannot exceed 512M of text or binary data.

The following are some use cases for strings:

* **Cache mechanisms:** It is possible to cache text or binary data in Redis, 
which could be anything for HTML pages and API responses to images and videos.
A simple cache system can be implemented with the commands *SET*, *GET*, 
*MSET*, and *MGET*.
* **Cache with automatic expiration:** String combined with automatic key 
expiration can make a robust cache system using the commands *SETEX*, *EXPIRE*, 
and *EXPIREAT*. This is very useful when database queries take a long time to 
run and can be cached for a given period of time. Consequently, this avoids 
running those queries too frequently and can give a performance boost to 
application.
* **Counting:** A counter can easily be implemented with strings and the 
commands *INCR* and *INCRBY*. Good examples of counters are pages views, 
video views, and likes. Strings also provide other counting commands, such 
as *DECR*, *DECRBY* and *INCRFLOATBY*.

### Lists

Lists are very flexible data type in Redis because they can act like a simple 
`collection`, `stack`, or `queue`. Many event systems use lists of Redis as 
their queue because the operations of Lists ensure that concurrent systems 
will not overlap popping items from a queue - Lists commands are atomic. 
There are blocking commands in Lists of Redis, which means that when a client 
executes a blocking command in an empty List, the client will wait for a new 
item to be added to the List. The Lists of Redis are linked lists, therefore 
insertions and deletions from the beginning or the end of a List run in *O(1)*, 
constant time.

Some real-world use cases of Lists are as follows:

* **Event queue**: Lists are used in many tools, including Resque, Celery, and 
logstash.
* **Storing most recent user posts**: Twitter does this by storing the latest 
tweets of a user in a List.


