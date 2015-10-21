#Usage

This project is meant to be used via the Forms System e.g. sections, question groups or questions within the XML may instead be designated to pass a request to Django.  This project will accept get or post requests and will return a chunk of html.  URLs have to be in the following forms:

To get down to a question or textnode level:

```
http://server-name:port/althtml/<section>/<question group>/<question>/?id=<username>
```

Where `<section>`, `<question group>` and `<question>` are the position numbers of the elements, e.g.

```
http://server-name:port/althtml/1/2/3/?id=davidg
```

This would return the html for question in position 3, in Question Group 2 that is in Section 1.  Likewise 

```
http://server-name:port/althtml/<section>/<question group>/?id=<username>
```

This will return the full Question Group html, e.g.

```
http://server-name:port/althtml/1/2/?id=davidg
```
would return the full html for question group 2 in Section 1.  For the full section html it needs to be

```
http://server-name:port/althtml/<section>/?id=<username>
```

e.g.
```
http://server-name:port/althtml/1/?id=davidg
```

This would return Section 1.
