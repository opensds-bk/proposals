package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
)

go_library(
    name = "go_default_library",
    srcs = [
        "attach.go",
        "constants.go",
        "doc.go",
        "exec.go",
        "httpstream.go",
        "websocket.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/errors:go_default_library",
        "//pkg/apis/meta/v1:go_default_library",
        "//pkg/httplog:go_default_library",
        "//pkg/types:go_default_library",
        "//pkg/util/exec:go_default_library",
        "//pkg/util/httpstream:go_default_library",
        "//pkg/util/httpstream/spdy:go_default_library",
        "//pkg/util/runtime:go_default_library",
        "//pkg/util/term:go_default_library",
        "//pkg/util/wsstream:go_default_library",
        "//vendor:github.com/golang/glog",
    ],
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
