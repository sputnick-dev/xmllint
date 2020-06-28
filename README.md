## xmllint is a wrapper over [xmllint](http://xmlsoft.org/) from `libxml2-utils`.

The goal is to implement `--xpath` switch for very old version of `xmllint` and to have newlines delimited output. (Unlike version < 2.9.9).    
Require `bash` and... `xmllint`

### Example with wrapper :

```bash
$ xmllint --html --xpath '//a/@href' http://www.w3.org/
href="/"
href="/standards/"
href="/participate/"
(...)
```

### Example without wrapper :

```bash
$ xmllint --html --xpath '//a/@href' http://www.w3.org/
 href="/" href="/standards/" href="/participate/" href="/Consortium/membership"
```

## Another approach

Install a subsystem: https://serverfault.com/a/1022826/120473

## edit 20180923: for _newline delimited output_, bug fixed upstream in `libxml2-utils` v2.9.9, check 

 - https://gitlab.gnome.org/GNOME/libxml2/commit/da35eeae5b92b88d8ebdb64b4b327ac1c2cf1bce
 - discussion: https://gitlab.gnome.org/GNOME/libxml2/-/merge_requests/8
 - https://mail.gnome.org/archives/xml/2018-March/msg00008.html
 - https://bugzilla.gnome.org/show_bug.cgi?id=740827

