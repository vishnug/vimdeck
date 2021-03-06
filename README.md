# vimdeck

VIM as a presentation tool


## Installation

Install the vim plugin [SyntaxRange](https://github.com/vim-scripts/SyntaxRange).

```
gem install vimdeck
```


## Usage

1. Write your slides in a markdown file (See below for details on _limited_ markdown syntax)

2. Run `vimdeck <file_name.md>` and it will generate a file for each slide and open them in VIM


## VIM Script

Vimdeck will also provide a script file that will set up keybindings for you.

- PageUp/Left go backwards
- PageDown/Right go forward


## A Note about VIM

This is a tool meant for VIM users. In other words, it is not a VIM plugin
&mdash; it's a script that converts a plain text document into multiple files.

The only hard dependency is [SyntaxRange](https://github.com/vim-scripts/SyntaxRange).

Other than that you may need some syntax highlighting plugins to handle the code syntax highlighting.


## A Note About Markdown

Slides are separated by 2 newlines in a row.

Example:

```
# Slide 1

- has some
- really important
- information


# Slide 2

Is less important
```

Vimdeck does not compile markdown into something else.
It uses a very small subset of markdown. List of items supported:

- h1s
- h2s
- images
- fenced code blocks

That's it. The point of Markdown is that it's human-readable. Other stuff like (un)ordered
lists, block quotes, indented code blocks, etc. will be displayed just as they were written.

Fenced code blocks look like this:

    ```javascript
       this.is = 'code'
    ```

# Why Ruby?

Additionally, I want to point out that I realize that it's odd to have a VIM-based tool
and not write it as a VIM script. Ruby was my language of choice only because the ascii art dependencies
were implemented as ruby gems. Plus, I &hearts; ruby.


##Screenshots:


Vimdeck converts h1s and h2s into ascii art
![](img/demo1.png)


Lists are displayed as they are written
![](img/demo2.png)


Vimdeck will also augment its vimscript to provide syntax highlighting
![](img/demo3.png)


Images are even converted to ascii art!
![](img/demo4.png)
