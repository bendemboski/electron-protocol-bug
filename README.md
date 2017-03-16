# electron-protocol-bug

To reproduce, first run

```
$ <path to electron> .
```

and observe "Required fs-extra" on the page, indicating that it was able to require a dependency when loading index.html via a `file:` URL. Next run

```
$ <path to electron> . serve
```

and observe the exception printed to the page, indicating that it was unable to require a dependency when loading index.html via a URL with a custom protocol (`serve://`).