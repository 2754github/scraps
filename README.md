# scraps

```sh
echo
dirs=(
  gas
  github
  golang
)
for dir in ${dirs[@]}; do
  find $dir -type f ! -name .DS_Store -print | sort | xargs md5 | md5
done

# 1e00ef23fe9d78b2ec0b6474466a2415
# d0e39eb12b90d7fa8eb769d26b8362c3
# b507f0e867ac637808d4ea71386ec4e2
```

1. [8fe5cc6] setup
1. [5d338a0] init
