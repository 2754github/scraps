# scraps

```sh
echo
dirs=(
  gas
  github
  golang
)
for dir in ${dirs[@]}; do
  find $dir -type f -print | sort | xargs md5 -q | md5
done

# e880487572454adbc7cb5c5a4857c065
# c00f9ab1b0d5eddc9e8c2a7d24f0da3c
# ec8f78984d7a9e02810929635cd90a23
```

1. [8fe5cc6] setup
1. [5d338a0] init
