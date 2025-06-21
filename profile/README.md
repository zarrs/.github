# zar<ins>rs</ins>

[`zarrs`] is a Rust library for the [Zarr] storage format for multidimensional arrays and metadata.
[`zarrs`] can be used as a codec pipeline in [`zarr-developers/zarr-python`], and also has C/C++ bindings.

This organisation hosts `zarrs` related repositories and serves `zarrs` web content:
- The `zarrs` Website <https://zarrs.dev>
- The `zarrs` Book <https://book.zarrs.dev>

## `zarrs` Ecosystem

### Core
- [`zarrs`]: The core library for manipulating Zarr hierarchies.

### Bindings
- [`zarrs-python`]: A high-performance codec pipeline for [`zarr-developers/zarr-python`].
- [`zarrs_ffi`]: A subset of `zarrs` exposed as a C/C++ API.

### Supporting Crates
- [`zarrs_metadata`]: Zarr metadata support (re-exported as `zarrs::metadata`).
- [`zarrs_metadata_ext`]: Zarr extensions metadata support.
- [`zarrs_data_type`]: The data type extension API for `zarrs` (re-exported in `zarrs::array::data_type`).
- [`zarrs_storage`]: The storage API for `zarrs` (re-exported as `zarrs::storage`).
- [`zarrs_plugin`]: The plugin API for `zarrs` (re-exported as `zarrs::plugin`).
- [`zarrs_registry`]: The Zarr extension point registry for `zarrs` (re-exported as `zarrs::registry`).

### Stores
- [`zarrs_filesystem`]: A filesystem store (re-exported as `zarrs::filesystem`).
- [`zarrs_object_store`]: [`object_store`] store support.
- [`zarrs_opendal`]: [`opendal`] store support.
- [`zarrs_http`]: A synchronous http store.
- [`zarrs_zip`]: A storage adapter for zip files.
- [`zarrs_icechunk`]: [`icechunk`] store support.
  - `git`-like version control for Zarr hierachies.
  - Read "virtual Zarr datacubes" of archival formats (e.g., [`netCDF4`](https://www.unidata.ucar.edu/software/netcdf/), [`HDF5`](https://www.hdfgroup.org/solutions/hdf5/), etc.) created by [`VirtualiZarr`](https://github.com/zarr-developers/VirtualiZarr) and backed by [`icechunk`].

### Zarr Metadata Conventions
- [`ome_zarr_metadata`]: A library for OME-Zarr (previously OME-NGFF) metadata.

### Tools
- [`zarrs_tools`]: Various tools for creating and manipulating Zarr V3 data with the zarrs rust crate
  - A reencoder that can change codecs, chunk shape, convert Zarr V2 to V3, etc.
  - Create an [OME-Zarr] hierarchy from a Zarr array.
  - Transform arrays: crop, rescale, downsample, gradient magnitude, gaussian, noise filtering, etc.

### Benchmarks
- [`zarr_benchmarks`]: Benchmarks of various Zarr V3 implementations: `zarrs`, `zarr-python`, `tensorstore`

[Zarr]: zarr.dev

[`zarrs`]: https://github.com/zarrs/zarrs/tree/main/zarrs
[`zarrs_data_type`]: https://github.com/zarrs/zarrs/tree/main/zarrs_data_type
[`zarrs_metadata`]: https://github.com/zarrs/zarrs/tree/main/zarrs_metadata
[`zarrs_metadata_ext`]: https://github.com/zarrs/zarrs/tree/main/zarrs_metadata_ext
[`zarrs_plugin`]: https://github.com/zarrs/zarrs/tree/main/zarrs_plugin
[`zarrs_registry`]: https://github.com/zarrs/zarrs/tree/main/zarrs_registry
[`zarrs_storage`]: https://github.com/zarrs/zarrs/tree/main/zarrs_storage
[`zarrs_filesystem`]: https://github.com/zarrs/zarrs/tree/main/zarrs_filesystem
[`zarrs_http`]: https://github.com/zarrs/zarrs/tree/main/zarrs_http
[`zarrs_object_store`]: https://github.com/zarrs/zarrs/tree/main/zarrs_object_store
[`zarrs_opendal`]: https://github.com/zarrs/zarrs/tree/main/zarrs_opendal
[`zarrs_zip`]: https://github.com/zarrs/zarrs/tree/main/zarrs_zip
[`zarrs_icechunk`]: https://github.com/zarrs/zarrs_icechunk
[`zarrs_ffi`]: https://github.com/zarrs/zarrs_ffi
[`zarrs-python`]: https://github.com/zarrs/zarrs-python
[`zarr-developers/zarr-python`]: https://github.com/zarr-developers/zarr-python
[`zarrs_tools`]: https://github.com/zarrs/zarrs_tools
[`zarr_benchmarks`]: https://github.com/zarrs/zarr_benchmarks
[`ome_zarr_metadata`]: https://github.com/zarrs/rust_ome_zarr_metadata
[`object_store`]: https://github.com/apache/arrow-rs/tree/main/object_store
[`opendal`]: https://github.com/apache/OpenDAL
[`icechunk`]: https://github.com/earth-mover/icechunk
[OME-Zarr]: https://ngff.openmicroscopy.org/latest/
