## **[BASIC]** Board [(4chan)](../README.md)

This object describes a 4chan board in great detail. It talks about the max filesize and comment lengths, cooldowns, and more. Some of it isn't too helpful for the average API consumer (cooldowns in particular, as most of those rate-limited operations can't even be done over the API, like posting).

### Usage

* [**/boards.json**](../operations/boards.md)
  - Most operations deal with threads/posts, so it makes sense that only the **/boards.json** operation would use this object.

### Fields

| Name | Type & Restrictions | Required? | Description |
| --- | --- | --- | --- |
[`board`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L3) | `string` | **Yes** | Unique, static board identifier, minus the `/`s (or in [s4s]'s sake, the `[]`s, but internally they're both `/`s). Sometimes called a shortcode. Used in various API operations, as well as in normal URLs. (e.g. `https://boards.4chan.org/g/catalog`) |
[`title`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L4) | `string` | **Yes** | The human-readable board title. Can contain unicode characters via codes like `\u1234`. |
[`ws_board`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L5) | `boolean` as `number` | **Yes** | Whether or not the board is work-safe (`1` if `true`, `0` if `false`). |
[`per_page`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L6) | `number` | **Yes** | Can be used in conjunction with `pages` to get the total number of alive threads at any given time. |
[`pages`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L7) | `number` | **Yes** | Can be used in conjunction with `per_page` to get the total number of alive threads at any given time. |
[`max_filesize`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L8) | `number` | **Yes** | The maximum number of bytes a file can be. It's typically a few [mebibytes](https://en.wikipedia.org/wiki/Mebibyte). |
[`max_webm_filesize`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L9) | `number` | **Yes** | The maximum number of bytes a `.webm` can be. This overrides the max filesize, and is *usually* smaller. Still only a few [mebibytes](https://en.wikipedia.org/wiki/Mebibyte). |
[`max_comment_chars`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L10) | `number` | **Yes** | The maximum number of characters that can be in a post. |
[`max_webm_duration`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L11) | `number` | **Yes** | The maximum number of seconds that can be in a `.webm`. |
[`bump_limit`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L12) | `number` | **Yes** | The number of posts in a thread it takes to hit the bumb limit. |
[`image_limit`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L13) | `number` | **Yes** | The number of images in a thread it takes to hit the bumb limit. |
[`cooldowns`.`threads`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L15) | `number` | **Yes** | The number of seconds you must wait after making a thread to perform another action. |
[`cooldowns`.`replies`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L16) | `number` | **Yes** | The number of seconds you must wait after making a reply to perform another action. |
[`cooldowns`.`images`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L17) | `number` | **Yes** | The number of seconds you must wait after posting an image to perform another action. |
[`cooldowns`.`replies_intra`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L18) | `number` | **Yes** | **[placeholder]** |
[`cooldowns`.`images_intra`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L19) | `number` | **Yes** | **[placeholder]** |
[`meta_description`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L21) | `string` | **Yes** | **[placeholder]** |
[`spoilers`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L65) | `boolean` as `number` | **No** | Whether or not image spoilers are enabled. |
[`custom_spoilers`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L66) | `number` | **No** | **[placeholder]** |
[`is_archived`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L44) | `boolean` as `number` | **No** | Whether or not threads are stored for a little while after they expire and are accessible through [/`b`/archive.json](operations/archive.md). |
[`forced_anon`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L22) | `boolean` as `number` | **No** | **[placeholder]** |
[`user_ids`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L43) | `boolean` as `number` | **No** | **[placeholder]** |
[`code_tags`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L89) | `boolean` as `number` | **No** | Whether or not `[code]` tags ([see rule #3 for /g/](https://www.4chan.org/rules#g4)) are acknowledged. |
[`webm_audio`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L111) | `boolean` as `number` | **No** | **[placeholder]** |
[`min_image_width`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L133) | `number` | **No** | The minimum required width for all posted images. |
[`min_image_height`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L134) | `number` | **No** | **[placeholder]** |
[`oekaki`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L156) | `boolean` as `number` | **No** | Whether or not the Oekaki applet is enabled |
[`country_flags`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L178) | `boolean` as `number` | **No** | **[placeholder]** |
[`sjis_tags`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L202) | `boolean` as `number` | **No** | **[placeholder]** |
[`text_only`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L226) | `boolean` as `number` | **No** | **[placeholder]** |
[`require_subject`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L227) | `boolean` as `number` | **No** | **[placeholder]** |
[`math_tags`](https://gist.github.com/r3c0d3x/696beb31b21df133332094462d3763d5#file-boards-json-L249) | `boolean` as `number` | **No** | **[placeholder]** |
