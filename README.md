# r8-retrace
Meta repo to build R8 for retracing

## Building

```
# Fresh clone
git clone --recurse-submodules git@github.com:dandc87/r8-retrace.git
# After a pull
git submodule update --init --recursive
export PATH=/path/to/r8-retrace/depot_tools:$PATH
cd r8
tools/gradle.py r8
```

## Retracing

```
java -cp ~/Projects/r8-retrace/r8/build/libs/r8.jar com.android.tools.r8.retrace.Retrace \
  target/build/outputs/mapping/release/mapping.txt stacktrace.txt > retraced.txt
```
