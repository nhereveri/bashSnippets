# Explode string

```bash
IFS=';' read -ra VARIABLE <<< "a;b;c"
echo ${VARIABLE[@]}
```
