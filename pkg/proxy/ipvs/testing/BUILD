package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = ["fake.go"],
    importpath = "k8s.io/kubernetes/pkg/proxy/ipvs/testing",
    tags = ["automanaged"],
    deps = ["//vendor/k8s.io/apimachinery/pkg/util/sets:go_default_library"],
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

go_test(
    name = "go_default_test",
    srcs = ["fake_test.go"],
    importpath = "k8s.io/kubernetes/pkg/proxy/ipvs/testing",
    library = ":go_default_library",
    deps = ["//vendor/k8s.io/apimachinery/pkg/util/sets:go_default_library"],
)
