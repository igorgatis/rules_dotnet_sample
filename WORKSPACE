workspace(name = "rules_dotnet_sample")

# A newer version should be fine
load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")

git_repository(
    name = "io_bazel_rules_dotnet",
    remote = "https://github.com/bazelbuild/rules_dotnet",
    commit = "98cc58708e0ea150a8737e7f83a74f0f41ececf8",
    shallow_since = "1597432771 +0200",
)

load("@io_bazel_rules_dotnet//dotnet:deps.bzl", "dotnet_repositories")

dotnet_repositories()

load(
    "@io_bazel_rules_dotnet//dotnet:defs.bzl",
    "core_register_sdk",
    "dotnet_register_toolchains",
    "dotnet_repositories_nugets",
    "mono_register_sdk",
    "net_register_sdk",
    "nuget_package",
)

dotnet_register_toolchains()
dotnet_repositories_nugets()

# For .NET Core:
core_register_sdk()

# For .NET Framework:
net_register_sdk()

# For Mono:
mono_register_sdk()
