load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# main branch as of 2021-11-25
RULES_RUST_COMMIT = "6d5598ccf30c8b3a37c703e8f89726a1cb2d17a9"

RULES_RUST_SHA256 = "5c3814a8007c32e4ecb1d264c9a6c8b8fdd25713563882e26cf46cbd00c2e702"

http_archive(
    name = "rules_rust",
    sha256 = RULES_RUST_SHA256,
    strip_prefix = "rules_rust-" + RULES_RUST_COMMIT,
    urls = [
        "https://github.com/bazelbuild/rules_rust/archive/" + RULES_RUST_COMMIT + ".tar.gz",
    ],
)

load("@rules_rust//rust:repositories.bzl", "rust_repositories")

rust_repositories(
    edition = "2018",
    include_rustc_srcs = True,
    version = "1.55.0",
)

load("@rules_rust//tools/rust_analyzer:deps.bzl", "rust_analyzer_deps")

rust_analyzer_deps()
