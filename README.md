# zig-version-tester

Find out which versions of Zig work with a project.

Call `zig-version-tester` like you would `zig`, i.e.

```sh
./zig-version-tester build test
```

`zig-version-tester` will start by testing the latest version of zig. It will continue until it finds a version that works.  Once it does, it will continue testing until it finds the oldest version that works and inform you of the result, i.e.

```
...
Works with 1 version(s) out of 6, from 0.10.0-dev.1335+c64279b15 to 0.10.0-dev.1335+c64279b15
```

By default `zig-version-tester` will test the versions in `~/zig-versions.txt`.  You can populate this manually starting with the newest first, i.e.

```
0.10.0-dev.2836+2360f8c49
0.10.0-dev.2490+135b91aec
0.10.0-dev.2413+ee1a95b55
0.10.0-dev.2186+3a64693db
0.10.0-dev.2063+49a7ceb5b
0.10.0-dev.1335+c64279b15
```

I've yet to implement an "update" command that will download the latest list of versions.  You can also create your own custom list of versions to test and pass them with `zig-version-tester --version-file MY_VERSION_FILE`.
