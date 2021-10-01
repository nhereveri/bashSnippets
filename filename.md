# Filename and extension

```bash
filename=$(basename -- "$0") # or any string
extension="${filename##*.}"
filename="${filename%.*}"
```

## Source

[@Petesh](https://stackoverflow.com/users/17833/petesh) in [Stack Overflow](https://stackoverflow.com/questions/965053/extract-filename-and-extension-in-bash/965072#965072)
