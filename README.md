# mime
A library to resolve mime types from file names

## get_mime_type
```c
char* get_mime_type(char* filename);
```

The `get_mime_type` function returns a mime type string of a given filename. (The file is not needed to be exist.)

e.g.
```c
get_mime_type("index.html");
// output: text/html
```
