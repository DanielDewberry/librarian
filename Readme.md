# Librarian

Due to confinement, my web browser cannot access documentation in /usr/share/doc or /usr/libexec.
I have therefore made this index page and nginx configuration to serve the documentation/ tools, locally.

## Preparation and Deployment

1. Update the file librarian/index.html, to configure the urls from "127.0.0.1:9000" to whatever best suits your needs.
2. Do the same for the nginx/librarian file.
3. From the project root execute:

```
./bin/deploy
```

## Development

### Bash script(s)

Ensure quality by executing `shellcheck` and `shfmt`.

shellcheck:

```
shellcheck bin/deploy
```

shfmt:

```
shfmt --diff --simplify --indent 4 --binary-next-line --case-indent --func-next-line  bin/deploy
```
