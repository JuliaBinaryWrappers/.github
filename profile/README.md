# JuliaBinaryWrappers

Welcome to the **JuliaBinaryWrappers** GitHub organization! This organization hosts auto-generated Julia packages that provide pre-compiled binary dependencies for the Julia ecosystem.

These packages, known as **JLL (Julia Language Linking) packages**, allow Julia users to seamlessly utilize external C/C++/Fortran libraries (e.g., `FFTW_jll`, `OpenBLAS_jll`, `Python_jll`) on a variety of platforms without needing to compile them from source.

## How It Works

The entire process is automated:

1.  **Build Recipes:** The build recipes are all stored in [Yggdrasil](https://github.com/JuliaPackaging/Yggdrasil).
2.  **BinaryBuilder.jl:** [`BinaryBuilder`](https://binarybuilder.org) provides the toolchains to compile these recipes in a consistent, reproducible environment.
3.  **JLL Package Generation:** The output of a successful build is an auto-generated JLL package (e.g., `FFTW_jll.jl`) which is hosted here within the `JuliaBinaryWrappers` organization.
4.  **Distribution:** The resulting tarballs are uploaded to GitHub releases and linked via an `Artifacts.toml` file in the Julia Registry.

## Usage

Most users will never need to interact with this organization directly. JLL packages are typically used as dependencies by higher-level Julia packages.

If you are a package developer wanting to add a binary dependency to your Julia package, refer to the official [BinaryBuilder.jl documentation](https://docs.binarybuilder.org/stable) for details on how to integrate JLL packages.

## Contributing and Getting Help

These repositories are largely auto-generated.

*   **Bug Reports:** If you encounter an issue with a specific JLL package (e.g., a binary fails to load on your system), please report it to the [Yggdrasil bug tracker](https://github.com/JuliaPackaging/Yggdrasil/issues) by opening an issue there.
*   **Build Scripts:** Contributions (e.g., updating a library version, fixing a build issue for a specific platform) are welcome via Pull Requests to the [Yggdrasil repository](https://github.com/JuliaPackaging/Yggdrasil).
*   **General Documentation:** For more details about JLL packages and how to use them, see the [BinaryBuilder.jl documentation](https://docs.binarybuilder.org/stable).

## License

Each repository within this organization contains a `LICENSE` file. Note that the license for the JLL *wrapper* package may differ from the license of the underlying binary library it wraps. The licenses for the wrapped libraries are included within the distributed tarballs.
