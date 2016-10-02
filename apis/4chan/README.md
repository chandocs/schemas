## 4chan's API

All URLs listed are clickable examples (watch for potentially NSFW content).

Portions of the URL listed in `code blocks` are arguments and can be changed.

### Endpoint

Default API endpoint: `https://a.4cdn.org` (accessible over both HTTP and HTTPS)

### Operations

CORS is supported with the origin: `boards.4chan.org` (over both HTTP and HTTPS)

Supported request methods are: **GET**, **HEAD**, **OPTIONS**

* **GET** [/boards.json](operations/boards.md) ([compressed](https://a.4cdn.org/boards.json), [decompressed (9/24/2016)](https://gist.githubusercontent.com/r3c0d3x/5ad62347e26eaa711f13250e3f535b05/raw/37e86e2e1b66f967b31896f66185d3fbda1f7636/boards.json)) 
  - Lists all publicly accessible boards.
* **GET** [/`b`/archive.json](operations/archive.md) ([compressed](https://a.4cdn.org/g/archive.json), [decompressed (9/24/2016)](https://gist.githubusercontent.com/r3c0d3x/327b25cf723b629a3240a0fd7489c869/raw/55d990c8a1af1e6a7c6aa202ef4106fccc620b49/archive.json))
  - Lists the recently expired threads (before they're actually deleted) from board `b`. (not used by all boards, see `/boards.json`'s documentation)
* **GET** [/`b`/catalog.json](operations/catalog.md) ([compressed](https://a.4cdn.org/g/catalog.json), [decompressed (9/24/2016)](https://gist.githubusercontent.com/r3c0d3x/89ac25c0848ff1bca9d15bcb69a99d14/raw/dcc52833595bf12865291386041ef2ee55e1be2d/catalog.json))
  - Lists the currently alive threads for board `b`, by page, including their OP. Used internally for the catalog, as referenced by the name.
* **GET** [/`b`/threads.json](operations/threads.md) ([compressed](https://a.4cdn.org/g/threads.json), [decompressed (9/24/2016)](https://gist.githubusercontent.com/r3c0d3x/1291165a4b18e7b2a723ea05ddb28912/raw/40bec293f3115a398ae2377a8428b0d2625a853a/threads.json))
  - Lists the currently alive threads for board `b`, by page, **not** including their OP. (significantly smaller filesize than `/catalog.json`, if you're into that)
* **GET** [/`b`/`n`.json](operations/pagenum.md) ([compressed](https://a.4cdn.org/g/1.json), [decompressed (9/24/2016)](https://gist.githubusercontent.com/r3c0d3x/af94917461d8de3fffefc23251859016/raw/f90d95be2a861d5a667f7b88614bd2b7fe618e79/1.json))
  - Lists the currently alive threads on the `n`-th page of board `b`, counting from 1 (i.e. the first page is `1`), including their OP. (like `/catalog.json`)
* **GET** [/`b`/thread/`n`.json](operations/threadnum.md) ([compressed](https://a.4cdn.org/g/thread/51971506.json), [decompressed (9/24/2016)](https://gist.githubusercontent.com/r3c0d3x/7d9f33c724a8e8105cbda21e06bc744f/raw/0bce0812ef7b10e126e6fb93f2294292b19a48c7/51971506.json))
  - Lists the currently alive posts in the thread with the OP post number `n` on board `b`.

### Objects

* **BASIC** [Board](objects/board.md)
  - Contains information about a board.
  - Used in:
    * **/boards.json**
* **BASIC** [Post](objects/post.md)
  - Describes a post.
* **COMPOUND** [Page](objects/page.md)
  - A collection of threads.
  - Uses:
    * Thread
  - Used in:
    * **/`b`/catalog.json**
    * **/`b`/threads.json**
* **COMPOUND** [Thread](objects/thread.md)
  - Basically a list of posts.
  - Uses:
    * Post
  - Used in:
    * **/`b`/`n`.json**
    * **/`b`/thread/`n`.json**
    * **/`b`/catalog.json**
