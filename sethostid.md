# Edit machine hostid

```bash
#!/bin/bash

if [ -n "$1" ]; then
  host_id=$1
  egrep -o '^[a-fA-F0-9]{8}$' <<< $host_id || exit 1
else
  host_id=$(hostid)
fi

a=${host_id:6:2}
b=${host_id:4:2}
c=${host_id:2:2}
d=${host_id:0:2}

echo -ne \\x$a\\x$b\\x$c\\x$d > /etc/hostid

exit 0
```

```bash
$ bash myhostid.sh 007f0100
```
