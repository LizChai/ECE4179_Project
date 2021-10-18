## Shuffle text

```bash
cat [name].txt| sort -R > [name_shuffled.txt
```

## Split text

do this twice to get 3 splits — train, test, dev

```bash

csplit [name]_shuffled.txt $(( $(wc -l < [name]_shuffled.txt) * 1 / 10 + 1))

```

## Generate label files

```bash
printf 'original\n%.0s' {1..[length]} > {train;test;dev}.label
```
