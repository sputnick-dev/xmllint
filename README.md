## xmllint is a simple wrapper over [xmllint](http://xmlsoft.org/) from `libxml2`

The main goal is to 'hack' around [this bug](https://bugzilla.gnome.org/show_bug.cgi?id=740827)

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

