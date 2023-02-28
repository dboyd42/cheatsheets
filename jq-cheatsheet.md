# jq Cheatsheet

**Selecting Records Based on Order**

> `-s` will `s`lurp (read) all inputs into an array.<br>
> This allows you to filter the records processed from their index.  Useful for
> when you want the overall layout and field names of data.

`jq -s '.[0]' filename.json`

