# r8-retrace
Meta repo to build R8 for retracing

## Rebuilding

```
git submodule update --init --recursive
cd r8
tools/gradle.py r8
```

## Retracing

```
java -cp ~/Projects/r8-retrace/build/libs/r8.jar com.android.tools.r8.retrace.Retrace \
  target/build/outputs/mapping/release/mapping.txt stacktrace.txt > retraced.txt
```
