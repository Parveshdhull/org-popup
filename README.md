# org-popup - Take notes in cool way

Take notes for emacs org-mode using pop-ups

![demo](https://user-images.githubusercontent.com/17097240/109394477-3abf7280-794d-11eb-909f-293a8cc6d29f.gif)


## Features
- Take notes very very fast
- Clipboard inserted in template by default
- No limitations of [Org Capture Protocol](https://orgmode.org/manual/The-capture-protocol.html), where data is only carried by one variable (body) and line breaks, tabs etc. not allowed.
- No Running client is needed
- Verify note before adding. If use %x of org-capture, it is sometime empty, specially when client is not running. 
- Highly configurable, like include todo, title, line breaks etc.

## Prerequisite
- xsel - For access clipboard content
- yad - For create popup

## Usage
1. Create [Org Template](https://orgmode.org/manual/Capture-templates.html)

```
(setq org-capture-templates
      '(("s" "Simple" entry (file+headline "~/test" "Simple Notes")
         "%[~/.emacs.d/.org-popup]" :immediate-finish t :prepend t)
        ("a" "Titled" entry (file+headline "~/test" "Titled Notes")
         "%[~/.emacs.d/.org-popup]" :immediate-finish t :prepend t)))
```

2. Running org-popup
	- Simple
		  `org-popup s`
	
	- Titled
		  `org-popup a titled`
	

- For save note press - "Ctrl + Shift + Enter"

- For Cancel press - "Esc"

## TIP
Assign these commands to keyboard hot-keys, and take note from anywhere, like while reading ebook or surfing net.

## YouTube Tutorial
[Coming Soon]


## Websites
https://github.com/Parveshdhull
<br />https://twitter.com/ParveshMonu
<br />https://youtube.com/right2trick
