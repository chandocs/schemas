## 4chan's API ![](https://r3c0d3x.github.io/chan-apis/priority_shields/4chan.svg)

All URLs listed are clickable examples (watch for potentially NSFW content).

Portions of the URL listed in `code blocks` are arguments and can be changed.

### Endpoint

Default API endpoint: `https://a.4cdn.org` (accessible over both HTTP and HTTPS)

### Operations

CORS is supported with the origin: `boards.4chan.org` (over both HTTP and HTTPS)

Supported request methods are: **GET**, **HEAD**, **OPTIONS**

* **GET** [/boards.json](operations/boards.md) ([example](https://a.4cdn.org/boards.json)) 
  - Lists all publicly accessible boards.
* **GET** [/`b`/archive.json](operations/archive.md) ([example](https://a.4cdn.org/g/archive.json))
  - Lists the recently expired threads (before they're actually deleted) from board `b`. (not used by all boards, see `/boards.json`'s documentation)
* **GET** [/`b`/catalog.json](operations/catalog.md) ([example](https://a.4cdn.org/g/catalog.json))
  - Lists the currently alive threads for board `b`, by page, including their OP. Used internally for the catalog, as referenced by the name.
* **GET** [/`b`/threads.json](operations/threads.md) ([example](https://a.4cdn.org/g/threads.json))
  - Lists the currently alive threads for board `b`, by page, **not** including their OP. (significantly smaller filesize than `/catalog.json`, if you're into that)
* **GET** [/`b`/`n`.json](operations/pagenum.md) ([example](https://a.4cdn.org/g/1.json))
  - Lists the currently alive threads on the `n`-th page of board `b`, counting from 1 (i.e. the first page is `1`), including their OP. (like `/catalog.json`)
* **GET** [/`b`/thread/`n`.json](operations/threadnum.md) ([example](https://a.4cdn.org/g/thread/51971506.json))
  - Lists the currently alive posts in the thread with the OP post number `n` on board `b`.

### Objects

* **BASIC** [Board](objects/board.md)
  - Contains information about a board.
  - Used in:
    * /boards.json
* **BASIC** [Post](objects/post.md)
  - Describes a post.
* **COMPOUND** [Page](objects/page.md)
  - A collection of threads.
  - Uses:
    * Thread
  - Used in:
    * /`b`/catalog.json
    * /`b`/threads.json
* **COMPOUND** [Thread](objects/thread.md)
  - Basically a list of posts.
  - Uses:
    * Post
  - Used in:
    * /`b`/`n`.json
    * /`b`/thread/`n`.json
    * /`b`/catalog.json