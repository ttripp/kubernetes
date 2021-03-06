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
        "bootstrap.go",
        "csr.go",
        "discovery.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//cmd/kubeadm/app/apis/kubeadm:go_default_library",
        "//cmd/kubeadm/app/phases/kubeconfig:go_default_library",
        "//cmd/kubeadm/app/util:go_default_library",
        "//pkg/kubelet/util/csr:go_default_library",
        "//vendor:github.com/square/go-jose",
        "//vendor:k8s.io/apimachinery/pkg/types",
        "//vendor:k8s.io/apimachinery/pkg/util/wait",
        "//vendor:k8s.io/client-go/kubernetes",
        "//vendor:k8s.io/client-go/pkg/apis/certificates",
        "//vendor:k8s.io/client-go/tools/clientcmd",
        "//vendor:k8s.io/client-go/tools/clientcmd/api",
        "//vendor:k8s.io/client-go/util/cert",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "bootstrap_test.go",
        "discovery_test.go",
    ],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//cmd/kubeadm/app/apis/kubeadm:go_default_library",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/v1",
        "//vendor:k8s.io/apimachinery/pkg/version",
        "//vendor:k8s.io/client-go/discovery",
        "//vendor:k8s.io/client-go/kubernetes",
        "//vendor:k8s.io/client-go/rest",
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
