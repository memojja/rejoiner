package(default_visibility = ["//visibility:public"])

java_library(
    name = "rejoiner",
    srcs = glob(["src/main/java/com/google/api/graphql/rejoiner/*.java"]),
    plugins = [":auto_plugin"],
    deps = [
        ":auto",
        "@aop//jar",
        "@com_google_guava_guava//jar",
        "@com_google_guice//jar",
        "@com_google_guice_multibindings//jar",
        "@com_google_protobuf_java//jar",
        "@com_graphql_java//jar",
        "@javax_annotations//jar",
        "@javax_inject//jar",
    ],
)

java_plugin(
    name = "auto_plugin",
    processor_class = "com.google.auto.value.processor.AutoValueProcessor",
    deps = ["@com_google_autovalue//jar"],
)

java_library(
    name = "auto",
    exported_plugins = [":auto_plugin"],
    exports = ["@com_google_autovalue//jar"],
)
