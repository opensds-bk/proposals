package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "fake.go",
        "mount.go",
        "mount_linux.go",
        "nsenter_mount.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/util/exec:go_default_library",
        "//pkg/util/sets:go_default_library",
        "//vendor:github.com/golang/glog",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "mount_linux_test.go",
        "safe_format_and_mount_test.go",
    ],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = ["//pkg/util/exec:go_default_library"],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)
