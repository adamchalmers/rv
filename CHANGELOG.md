# rv 0.2.0

## Added

* Add support for Intel (x86_64) Mac
* Add support for Ruby 3.3.x (#132)
* `rv shell` for adding CLI completions and automatically changing Ruby on `cd`. ()
* Nushell support in `rv shell` (#123, #120)
* Fish support in `rv shell` (#81)

## Fixed

* GEM_PATH set to repository roots (#110)
* Respect XDG config dir conventions
* Read native TLS certs so that `rv` works behind proxies (#131)
* Errors while downloading a Ruby won't prevent future downloads (#89)
* Validate tarballs before reusing them (#101)
* Typos (#107, #88)
* Slight speedups (#98)
* Terminate with a nice error on an unsupported platform (#99)

## Internal improvements

* Benchmarks (#93, #96)
* Fuzzer setup (#95)
* Many more unit tests
* Integration tests for `rv ruby install` (#89)
* Run `cargo deny` in CI to detect bad dependencies (#124)
* Removed unused dependencies and cargo features of dependencies
* Track unit test coverage in Codecov.io

# rv 0.1.1

* Dual license MIT / Apache-2
* turn up LTO for smaller releases
* Fix `rv ruby pin` if not run in a project_dir
* Fix `bin/setup` in non-root situations under Ubuntu
* replace openssl with rustls
* Added bash to supported shells

# rv 0.1.0

First release. Supports macOS 14+, Ubuntu 24.04+, Ruby 3.4.1+, and zsh.

- `rv ruby` command group
  - `rv ruby list` command to show installed rubies
  - `rv ruby install` to install precompiled rubies
  - `rv ruby run` to run a specific ruby version regardless of `.ruby-version`
- `rv shell` command group
  - `rv shell init` command to set up automatic ruby switching that respects `.ruby-version` files
