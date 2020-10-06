load("@io_bazel_rules_dotnet//dotnet:defs.bzl", "dotnet_binary", "dotnet_library")

dotnet_library(
    name = "sample_lib.dll",
    srcs = [
        "Sample.cs",
    ],
)

dotnet_library(
    name = "sample.exe",
    srcs = [
        "Program.cs",
    ],
    deps = [
        ":sample_lib.dll",
    ],
)
