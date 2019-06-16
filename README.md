# markdeep-slides

TODO hero image thingy?

*Build presentation slides with Markdeep and present them right in your browser.*

* Two modes: **Draft** (with inline presenter notes) and **presentation** (full-screen, with *presenter notes in a separate window*). You can also **generate a PDF** of your slides!
* **Keyboard shortcuts** for all relevant functions.
* Supports **everything Markdeep has to offer** – diagrams, math, inline videos, citations, admonitions, and all the standard Markdown stuff.
* If you don't like any of the predefined themes: **Style your slides with CSS!** LaTeX Beamer is great, but things can get tricky. And *let's not talk about PowerPoint* and its various knockoffs.
* The full power of CSS animations and JavaScript is at your fingertips – use it wisely.
* 3 built-in themes – but you can make your own with a couple dozen lines of CSS.
* Compatible with those little [presenter gadgets](https://www.amazon.com/Logitech-Wireless-Presenter-Presentation-Pointer/dp/B00B6MODOA/).

#### **Demo:** Try it out [right here on GitHub Pages](https://doersino.github.io/markdeep-slides/slides.md.html)!


## Getting started

### Setup

It's best to **download a release**, since that comes **prepackaged with a well-tested combination of Markdeep, MathJax**, the webfonts used by the built-in themes, and more – it'll **work offline** (unless you include YouTube videos or something in your slides). *You don't want to rely on wifi being available when and where you'll present – that's just asking for trouble.*

#### The most recent releases are [available here](https://github.com/doersino/markdeep-slides/releases). [📦](https://github.com/doersino/markdeep-slides/releases)

Alternatively, you can `git clone` this repository and then `git checkout` the `release` branch.

But if you just want to take a quick look at how this thing works on your own machine, go ahead and `git clone` the hell out of this repository. Then, open `slides.md.html` in your text editor and browser of choice. Again, if you decide to use this thing for an actualy presentation, grab a release so you're unaffected by the whims of the WiFi gods.

### Options

There's a few global options you might be interested in modifying:

TODO

TODO another note on css variables of themes


## Contributing

Got an idea on how to improve something? Found a bug? (Maybe even fixed that bug?)

*Please [file an issue](https://github.com/doersino/markdeep-slides/issues) or send a pull request! I'll be happy to take a look at it.*


---


### Notes & Implementation details

* Tested in recent versions of Chrome, Firefox and Safari. I don't have access to Edge/IE, so you're on your own there (although I suspect the folks interested in writing their slides in Markdeep aren't using these browsers anyway). Not really made for mobile use.
* If you're making your own themes, only use relative sizes: `em`, `rem`, `%`. This allows the slides to scale arbitrarily. So don't use `px`, `pt`, `mm` etc. Also don't use `vw` and `vh` – depending on the aspect ratio of your display and your slides, your slides will be [letterboxed](https://en.wikipedia.org/wiki/Letterboxing_(filming)), so `100vh` might be larger than the width of your slides (the same goes for height).
* To download fonts from Google fonts, I recommend using [this tool](https://google-webfonts-helper.herokuapp.com/fonts).
* If your presenter gadget doesn't work, please go to https://keycode.info and record which keycodes each button sends, what happened, what you expected to happen and file an issue accordingly.
* TODO more


### Known issues

If you know of an elegant way of fixing these, I'd very much appreciate a heads up.

* When resizing the window in Safari in draft mode, the font size is not scaled accordingly. No idea why – it's defined in terms of `vw` units in CSS, so it *should* scale as the viewport width changes.
* When leaving fullscreen mode in Firefox using <kbd>Esc</kbd>, presentation mode sometimes persists. No idea why – leaving it by pressing <kbd>f</kbd> fires the same event, so the same stuff *should* happen.
* After refreshing while in fullscreen mode in Safari, the only way to exit fullscreen mode is clicking the green button – and even after that, presentation mode persists because the `webkitfullscreenchange` event does not fire in this situation. (Other browsers exit fullscreen mode upon refresh, making this a non-issue there.)


### License

You may use this repository's contents under the terms of the *BSD 2-Clause "Simplified" License*, see `LICENSE`.

In the *release* branch, some **third-party software with its own licenses** has been bundled:

* Morgan McGuire's **Markdeep** is *also* licensed under the *BSD 2-Clause "Simplified" License*, see [here](https://casual-effects.com/markdeep/#license).
* Markdeep includes Ivan Sagalaev's **highlight.js** with its *BSD 3-Clause License*, see [here](https://github.com/highlightjs/highlight.js/blob/master/LICENSE).
* **MathJax** (only a stripped-down variant of which is included – nobody needs image fonts these days) is licensed under the *Apache License 2.0*, see [here](https://github.com/mathjax/MathJax/blob/master/LICENSE).
* All included **webfonts** (Source Sans Pro, Fira Mono, Vollkorn, Vollkorn SC, Libre Franklin, Source Serif Pro) are licensed under the *Open Font License*, see [here](https://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&id=OFL_web).
