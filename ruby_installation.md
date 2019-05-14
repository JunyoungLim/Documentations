# Ruby Installation Guide

This guide is for Mac Mojave (10.14.x) or higher.

## Homebrew Installation

This section is for installing Ruby using Homebrew.

### Ruby Installation

Install Ruby with Homebrew:

```bash
brew install ruby
```

Check Ruby version using:

```bash
ruby -v
```

Make sure to export the following variables:

```bash
# For compilers to find ruby you may need to set:
export LDFLAGS="-L/usr/local/opt/ruby/lib"
export CPPFLAGS="-I/usr/local/opt/ruby/include"

# For pkg-config to find ruby you may need to set:
export PKG_CONFIG_PATH="/usr/local/opt/ruby/lib/pkgconfig"
```
