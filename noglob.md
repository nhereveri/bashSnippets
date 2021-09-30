# Disable filename expansion (globbing)

```bash
# enabled (default)
set +f

# list all files in current directory
ls *

# disabled
set -f

# error if no such file or directory
ls *
```
