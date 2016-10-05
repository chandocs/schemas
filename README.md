# Chan API Documentation Project [![Build Status](https://travis-ci.org/chandocs/schemas.svg?branch=master)](https://travis-ci.org/chandocs/schemas)

## About

We try to maintain comprehensive and up-to-date documentation for various chan APIs. Typically a chan's in-house documentation is outdated and lacking examples, which forces developers to waste time figuring out how it really works. We are here to change that.

## Supported APIs

Each API title is also a link to our documentation on it, and the priority shields (**TODO: Create small wiki page about them**) will lead you to the site's original documentation.

* [420chan's API](apis/420chan/README.md) [![Low priority](misc/priority_shields/low.png)](http://api.420chan.org/)
  - Their documentation is detailed and lists example responses for each of their endpoints. It is good enough at the moment, but we should still have some documentation here for it in the future.
  - Currently only being used by [420chan (`420chan.org`)](http://420chan.org/).
* [4chan's API](apis/4chan/README.md) [![Normal priority](misc/priority_shields/normal.png)](https://github.com/4chan/4chan-api/)
  - While it does have some documentation, it's only for its `post` object. It lists multiple endpoints without going into detail about them, and doesn't seem to be updated very often.
  - Currently only being used by [4chan (`4chan.org`)](https://4chan.org).
* Lynxchan's API [![Low priority](misc/priority_shields/low.png)](https://gitgud.io/LynxChan/LynxChan/tree/master/doc)
  - The documentation is good, but a little disorganized. Certainly better than 4chan and vichan though.
  - Currently being used by [these sites](http://lynxhub.com/lynxchan/res/285.html).
* [vichan's API](apis/vichan/README.md) [![Normal priority](misc/priority_shields/normal.png)](https://github.com/vichan-devel/vichan-API/)
  - This has the same pitfalls of 4chan's API documentation because it's literally just a slightly modified fork of theirs. The lack of frequent updates is less important here though as we can at least tell when vichan's API changes because [it's open source](https://github.com/vichan-devel/vichan/).
  - Currently being used by:
    - [8chan (`8ch.net`)](https://8ch.net/index.html)
    - [`8ch.pl`](http://8ch.pl/)/[`vichan.net`](https://vichan.net/)
    - [Polski vichan (`pl.vichan.net`)](https://pl.vichan.net/*/index.html)
    - [(the testing site) `engine.vichan.net`](https://engine.vichan.net/)

## Chat

We have IRC channels to discuss pretty much anything related to chan APIs (and development in general):

``#chandocs @ irc.rizon.net`` ([webchat](http://qchat.rizon.net/?channels=chandocs))

## License

[![Creative Commons License](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/)
<br>
This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0)](http://creativecommons.org/licenses/by-nc-sa/4.0/).

A Markdown version of the license is available in [`LICENSE.md` in the root directory of this repository](LICENSE.md) courtesy of [GitHub user `idleberg`'s project](https://github.com/idleberg/Creative-Commons-Markdown/).
