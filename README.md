# protobuf

[protobuf](https://github.com/protocolbuffers/protobuf) but packaged for [Zig](https://ziglang.org).

## How to add to your project

`zig fetch --save git+https://github.com/allyourcodebase/protobuf`

You can then access the available libraries and executables like this:
```zig
const protobuf_dep = b.dependency("protobuf", .{
    .target = target,
    .optimize = optimize,
});

// libµpb
const libupb = protobuf_dep.artifact("libupb");

// libprotobuf
const libprotobuf = protobuf_dep.artifact("libprotobuf");

// libprotoc
const libprotoc = protobuf_dep.artifact("libprotoc");

// protoc
const protoc = protobuf_dep.artifact("protoc");
```

