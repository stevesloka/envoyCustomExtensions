# Envoy - Custom Extensions

This repo contains a sample of how to build custom extensions for Envoy.

1. Edit the file `extensions_build_config.bzl` and comment out any extensions you don't want added
2. From the Envoy repo, add the following command to the Bazel build command: 

    ```bash
    --override_repository envoy_build_config=<absolutePath>/envoy_custom
    ```

Example Command:

```bash
$ bazel --bazelrc=/dev/null build -c opt //source/exe:envoy-static.stripped --override_repository envoy_build_config=<absolutePath>/envoy_custom
```