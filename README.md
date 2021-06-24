# cidr-merge

Takes a list of CIDR ranges or IP addresses, and removes duplicates and
merges ranges.

## Example

```
$ cat input.txt
10.0.0.1
10.0.1.0/24
10.1.0.0/16
10.2.0.0/24
10.0.0.0/16
fc00:123:456::/48
fc00:123:457::/48

$ ./cidr-merge.py < input.txt
10.0.0.0/15
10.2.0.0/24
fc00:123:456::/47
```
