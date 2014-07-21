# reveal-md

[reveal.js](http://lab.hakim.se/reveal-js/#/) on steroids! Get beautiful reveal.js presentations from your Markdown files.

## Clarifications

This repository is a fork of [abelnation/reveal-md](https://github.com/abelnation/reveal-md).

Thanks to [@abelnation](https://github.com/abelnation) to add code highlight on his fork of the original project [webpro/reveal-md](https://github.com/webpro/reveal-md).

## Installation

Create a sym link to you local bin version:

``` bash
sudo ln -s /path/to/you/clone/repo/reveal-md/bin/server-cli.js /usr/local/bin/reveal-mdc
```

## Quick demo

Execute your local version passing the path of your *.md file:

``` bash
reveal-mdc path/to/README.md
```

## Markdown in reveal.js

The Markdown feature of reveal.js is awesome, and has an easy (and configurable) syntax to separate slides.
Use three dashes surrounded by two blank lines (`\n---\n`).
Example:

``` text
# Title

* Point 1
* Point 2

---

## Second slide

> Best quote ever.

```

The separator syntax can be overriden (e.g. I like to use three blank lines).

## Usage

To open specific Markdown file as Reveal.js slideshow:

``` bash
reveal-md slides.md
```

You can also provide a url that resolves to a Markdown resource (over http(s)).

``` bash
reveal-md https://raw.github.com/webpro/reveal-md/master/demo/a.md
```

Show (recursive) directory listing of Markdown files:

``` bash
reveal-md dir/
```

Show directory listing of Markdown files in current directory:

``` bash
reveal-md
```

Override theme (default: `default`):

``` bash
reveal-md slides.md --theme solarized
```

Override slide separator (default: `\n---\n`):

``` bash
reveal-md slides.md --separator "^\n\n\n"
```

Override vertical/nested slide separator (default: `\n----\n`):

``` bash
reveal-md slides.md --vertical "^\n\n"
```

Override port (default: `1948`):

``` bash
reveal-md slides.md --port 8888
```

## Print Support

*Requires phantomjs to be installed (preferably globally)*

This will try to create a pdf with the passed in file (eg slides.md) and outputted to the name passed into the `--print` parameter (eg slides.pdf)

``` bash
reveal-md slides.md --print slides.pdf
```

## Notes

* `reveal-md` always starts a local server and opens the default browser
* From any presentation, navigate to the root (e.g. [http://localhost:1948](http://localhost:1948)) to get directory listing of (linked) Markdown files. Root folder is resolved from Markdown file (or directory) `reveal-md` was started with.

## License

[MIT](http://webpro.mit-license.org)
