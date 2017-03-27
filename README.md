# SYNOPSIS
Pretty print your [`newline delimited json`](http://ndjson.org/), tolerate
unparsable lines.

# INSTALL
`npm install ntail -g`

# USAGE
Let's say your program outputs new line delimited JSON, that's not going to be
readable (ever). So pipe the output of your program to `ntail` and it will try
to parse anything that is a valid line of JSON!

```bash
node myprogram.js | ntail
```

A more fancy way to capture the output in a different terminal window from where
your process is running, is to pipe to a temp file and then tail that file, for
example `tail -f logfile | ntail`.

If you want to mute all non parsable lines, use `--mute`.

# OUTPUT

![screenshot](/screenshot.png)
