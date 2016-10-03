# Chan API Documentation Project [![Build Status](https://travis-ci.org/chandocs/schemas.svg?branch=master)](https://travis-ci.org/chandocs/schemas)

## About

We try to maintain comprehensive and up-to-date documentation for various chan APIs. Typically a chan's in-house documentation is outdated and lacking examples, which forces developers to waste time figuring out how it really works. We are here to change that.

## Supported APIs

Each API title is also a link to our documentation on it, and the priority shields (**TODO: Create small wiki page about them**) will lead you to the site's original documentation.

* [420chan's API](apis/420chan/README.md) [![Low priority](misc/priority_shields/low.png)](http://api.420chan.org/)
  - Their documentation is detailed and lists example responses for each of their endpoints. It is good enough at the moment, but we should still have some documentation here for it in the future.
* [4chan's API](apis/4chan/README.md) [![Normal priority](misc/priority_shields/normal.png)](https://github.com/4chan/4chan-api/)
  - While it does have some documentation, it's only for its `post` object. It lists multiple endpoints without going into detail about them, and doesn't seem to be updated very often.
* [vichan's API](apis/vichan/README.md) [![Normal priority](misc/priority_shields/normal.png)](https://github.com/vichan-devel/vichan-API/) (used by 8chan)
  - This has the same pitfalls of 4chan's API documentation because it's literally just a slightly modified fork of theirs. The lack of frequent updates is less important here though as we can at least tell when vichan's API changes because [it's open source](https://github.com/vichan-devel/vichan/).

## License

[![Creative Commons License](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/)
<br>
This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0)](http://creativecommons.org/licenses/by-nc-sa/4.0/).

A Markdown version of the license is available in [`LICENSE.md` in the root directory of this repository](LICENSE.md) courtesy of [GitHub user `idleberg`'s project](https://github.com/idleberg/Creative-Commons-Markdown/).