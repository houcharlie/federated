load("@rules_python//python:defs.bzl", "py_binary", "py_library", "py_test")

package(default_visibility = ["//visibility:private"])

licenses(["notice"])

py_library(
    name = "flars_optimizer",
    srcs = ["flars_optimizer.py"],
    srcs_version = "PY3",
)

py_test(
    name = "flars_optimizer_test",
    srcs = ["flars_optimizer_test.py"],
    python_version = "PY3",
    srcs_version = "PY3",
    deps = [":flars_optimizer"],
)

py_library(
    name = "flars_fedavg",
    srcs = ["flars_fedavg.py"],
    srcs_version = "PY3",
    deps = [
        ":flars_optimizer",
        "//utils:tensor_utils",
    ],
)

py_test(
    name = "flars_fedavg_test",
    size = "large",
    srcs = ["flars_fedavg_test.py"],
    python_version = "PY3",
    srcs_version = "PY3",
    deps = [
        ":flars_fedavg",
        ":flars_optimizer",
    ],
)

py_binary(
    name = "run_emnist",
    srcs = ["run_emnist.py"],
    python_version = "PY3",
    srcs_version = "PY3",
    deps = [
        ":flars_fedavg",
        ":flars_optimizer",
        "//utils:utils_impl",
        "//utils/models:emnist_models",
    ],
)
