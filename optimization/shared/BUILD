load("@rules_python//python:defs.bzl", "py_library", "py_test")

package(default_visibility = ["//visibility:public"])

licenses(["notice"])

py_library(
    name = "evaluation",
    srcs = ["evaluation.py"],
    srcs_version = "PY3",
)

py_test(
    name = "evaluation_test",
    size = "medium",
    srcs = ["evaluation_test.py"],
    python_version = "PY3",
    srcs_version = "PY3",
    deps = [":evaluation"],
)

py_library(
    name = "fed_avg_client_opt",
    srcs = ["fed_avg_client_opt.py"],
    srcs_version = "PY3",
    deps = ["//utils:tensor_utils"],
)

py_test(
    name = "fed_avg_client_opt_test",
    size = "large",
    srcs = ["fed_avg_client_opt_test.py"],
    python_version = "PY3",
    shard_count = 2,
    srcs_version = "PY3",
    deps = [":fed_avg_client_opt"],
)

py_library(
    name = "fed_avg_schedule",
    srcs = ["fed_avg_schedule.py"],
    srcs_version = "PY3",
    deps = ["//utils:tensor_utils"],
)

py_test(
    name = "fed_avg_schedule_test",
    size = "large",
    srcs = ["fed_avg_schedule_test.py"],
    python_version = "PY3",
    shard_count = 2,
    srcs_version = "PY3",
    deps = [":fed_avg_schedule"],
)

py_library(
    name = "keras_metrics",
    srcs = ["keras_metrics.py"],
    srcs_version = "PY3",
)

py_test(
    name = "keras_metrics_test",
    size = "small",
    srcs = ["keras_metrics_test.py"],
    python_version = "PY3",
    srcs_version = "PY3",
    deps = [":keras_metrics"],
)

py_library(
    name = "keras_callbacks",
    srcs = ["keras_callbacks.py"],
    srcs_version = "PY3",
    deps = ["//utils:utils_impl"],
)

py_test(
    name = "keras_callbacks_test",
    size = "small",
    srcs = ["keras_callbacks_test.py"],
    python_version = "PY3",
    srcs_version = "PY3",
    deps = [":keras_callbacks"],
)

py_library(
    name = "optimizer_utils",
    srcs = ["optimizer_utils.py"],
    srcs_version = "PY3",
    deps = [
        "//optimization/shared/keras_optimizers:lars",
        "//optimization/shared/keras_optimizers:shampoo",
        "//optimization/shared/keras_optimizers:yogi",
    ],
)

py_test(
    name = "optimizer_utils_test",
    size = "small",
    srcs = ["optimizer_utils_test.py"],
    python_version = "PY3",
    srcs_version = "PY3",
    deps = [":optimizer_utils"],
)

py_library(
    name = "schedule_utils",
    srcs = ["schedule_utils.py"],
    srcs_version = "PY3",
)

py_test(
    name = "schedule_utils_test",
    size = "small",
    srcs = ["schedule_utils_test.py"],
    python_version = "PY3",
    srcs_version = "PY3",
    deps = [":schedule_utils"],
)

py_library(
    name = "training_specs",
    srcs = ["training_specs.py"],
    srcs_version = "PY3",
)
