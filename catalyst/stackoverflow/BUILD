load("@rules_python//python:defs.bzl", "py_library")

package(default_visibility = ["//visibility:public"])

licenses(["notice"])

py_library(
    name = "centralized_stackoverflow",
    srcs = ["centralized_stackoverflow.py"],
    srcs_version = "PY3",
    deps = [
        "//catalyst/shared:keras_metrics",
        "//utils:centralized_training_loop",
        "//utils/datasets:stackoverflow_word_prediction",
        "//utils/models:stackoverflow_models",
    ],
)

py_library(
    name = "federated_stackoverflow",
    srcs = ["federated_stackoverflow.py"],
    srcs_version = "PY3",
    deps = [
        "//catalyst/shared:keras_metrics",
        "//catalyst/shared:training_specs",
        "//utils:training_utils",
        "//utils/datasets:stackoverflow_word_prediction",
        "//utils/models:stackoverflow_models",
    ],
)
