load("@io_bazel_rules_dotnet//dotnet:defs.bzl", "dotnet_binary", "dotnet_library")

dotnet_library(
    name = "sample_lib.dll",
    srcs = [
        "Sample.cs",
    ],
    deps = [
        "@io_bazel_rules_dotnet//dotnet/stdlib:system.dll",
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
