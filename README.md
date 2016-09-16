# Chan API Documentation Project

## About

We try to maintain comprehensive and up-to-date documentation for various chan APIs. Typically a chan's in-house documentation is outdated and lacking examples, which forces developers to waste time figuring out how it really works. We are here to change that.

## Supported APIs

Each API title is also a link to our documentation on it, and the priority shields (**TODO: Create small wiki page about them**) will lead you to the site's original documentation.

* [420chan's API](apis/420chan/README.md) [![Low priority](https://r3c0d3x.github.io/chan-apis/priority_shields/420chan.svg)](http://api.420chan.org/)
  - Their documentation is detailed and lists example responses for each of their endpoints. It is good enough at the moment, but we should still have some documentation here for it in the future.
* [4chan's API](apis/4chan/README.md) [![Normal priority](https://r3c0d3x.github.io/chan-apis/priority_shields/4chan.svg)](https://github.com/4chan/4chan-api/)
  - While it does have some documentation, it's only for its `post` object. It lists multiple endpoints without going into detail about them, and doesn't seem to be updated very often.
* [vichan's API](apis/vichan/README.md) [![Normal priority](https://r3c0d3x.github.io/chan-apis/priority_shields/vichan.svg)](https://github.com/vichan-devel/vichan-API/) (used by 8chan)
  - This has the same pitfalls of 4chan's API documentation because it's literally just a slightly modified fork of theirs. The lack of frequent updates is less important here though as we can at least tell when they change vichan's API, because vichan is open-source.
