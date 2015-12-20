# mdletter

A latex boilerplate to quickly write a basic letter using markdown. The system
uses the `scrlttr2` class to write the letter. The following parameters are
specified in a YAML block at the top of the markdown file (use a line containing
  `---` to mark the beginning and end of the YAML block)

Required arguments
- toname: addresse
- toaddress: addresse's address

Recommended arguments
- from: name of sender
- fromaddress: address of sender

Optional arguments
- phone: phone number of sender
- email: email address of sender
- signature: signature of the sender (defaults to [from] name)
- greeting: the greeting (default is Dear [toname],)
- closing: the closing (default is Yours sincerely)
- ps: a postscript for the letter
- language: language for hyphernation (see babel for options) (default is
  UKenglish)

## Requirements
You'll need [TeX Live](https://www.tug.org/texlive/) and [Pandoc](http://pandoc.org).

## Convert markdown to pdf letter
To convert just call pandoc with the template:
```
$ pandoc alice.md --latex-engine=pdflatex --template=template.tex -o letter.pdf
```
