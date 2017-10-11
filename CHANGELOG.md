# Changelog
All notable changes to this project will be documented in this file.

We use version numbers with three digits such as 1.0.0.
Any version bump in the last digit is backwards-compatible, in that a model trained with the previous version can still
be used for translation with the new version.
Any bump in the second digit indicates potential backwards incompatibilities, e.g. due to changing the architecture or
simply modifying weight names.
Note that Sockeye has checks in place to not translate with an old model that was trained with an incompatible version.

For each item we will potentially have subsections for: _Added_, _Changed_, _Removed_, _Deprecated_ and _Fixed_.

## [1.8.1]
### Changed
 - Instead of truncating sentences exceeding the maximum input length they are now translated in chunks.

## [1.8.0]
### Added
 - Convolutional decoder.
 - Weight normalization (for CNN only so far).
 - Learned positional embeddings for the transformer.

### Changed
 - `--attention-*` CLI params renamed to `--rnn-attention-*`.
 - `--transformer-no-positional-encodings` generalized to `--transformer-positional-embedding-type`.
