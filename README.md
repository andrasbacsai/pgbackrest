# pgBackRest Binaries

Unofficial pre-built binaries for [pgBackRest](https://github.com/pgbackrest/pgbackrest).

## Downloads

Download the latest release from the [Releases](https://github.com/andrasbacsai/pgbackrest/releases) page.

### Supported Platforms

| Platform | Architecture | File |
|----------|--------------|------|
| Linux | amd64 | `pgbackrest-{VERSION}-linux-amd64.tar.gz` |
| Linux | arm64 | `pgbackrest-{VERSION}-linux-arm64.tar.gz` |
| macOS | amd64 (Intel) | `pgbackrest-{VERSION}-darwin-amd64.tar.gz` |
| macOS | arm64 (Apple Silicon) | `pgbackrest-{VERSION}-darwin-arm64.tar.gz` |

## Installation

```bash
# Download and extract (example for Linux amd64)
curl -L https://github.com/andrasbacsai/pgbackrest/releases/download/2.57.0/pgbackrest-2.57.0-linux-amd64.tar.gz | tar xz

# Move to a directory in your PATH
sudo mv pgbackrest-2.57.0-linux-amd64/pgbackrest /usr/local/bin/

# Verify installation
pgbackrest version
```

## Verification

Each release includes a `checksums.txt` file for verifying downloads:

```bash
# Download checksums
curl -LO https://github.com/andrasbacsai/pgbackrest/releases/download/2.57.0/checksums.txt

# Verify your download
sha256sum -c checksums.txt --ignore-missing
```

## Build Details

- **Linux binaries**: Built on Alpine Linux 3.21 with musl libc for maximum portability (fully static)
- **macOS binaries**: Built with Homebrew dependencies on native runners

## Official pgBackRest

This is an unofficial distribution. For official releases, documentation, and support, visit:

- Repository: https://github.com/pgbackrest/pgbackrest
- Documentation: https://pgbackrest.org
- Official packages: Available via apt, yum, and other package managers

## License

pgBackRest is licensed under the MIT License. See the [LICENSE](https://github.com/pgbackrest/pgbackrest/blob/main/LICENSE) file in the official repository.
