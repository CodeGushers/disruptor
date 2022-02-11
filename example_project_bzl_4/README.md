# Example of using `copy_dynamic_libraries_to_binary` feature
```
bazel build //readline_example_c:main --features copy_dynamic_libraries_to_binary --override_repository=bazel_tools=$(pwd)/bazel_tools
cp -r bazel-bin/readline_example_c/ /tmp/rec
cd /tmp/rec
ldd main
ls -l *.so
./main
```
