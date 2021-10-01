
## Development

### Environment Setup

1. Install the latest Rust stable from https://rustup.rs/
2. Install Solana v1.6.1 or later from https://docs.solana.com/cli/install-solana-cli-tools
3. Install the `libudev` development package for your distribution (`libudev-dev` on Debian-derived distros, `libudev-devel` on Redhat-derived).

### Build

The normal cargo build is available for building programs against your host machine:
```
$ cargo build
```

To build a specific program, such as SPL Token, for the Solana BPF target:
```
$ cd token/program
$ cargo build-bpf
```

### Test

Unit tests contained within all projects can be run with:
```bash
$ cargo test      # <-- runs host-based tests
$ cargo test-bpf  # <-- runs BPF program tests
```

To run a specific program's tests, such as SPL Token:
```
$ cd token/program
$ cargo test      # <-- runs host-based tests
$ cargo test-bpf  # <-- runs BPF program tests
```

Integration testing may be performed via the per-project .js bindings.  See the
[token program's js project](token/js) for an example.


