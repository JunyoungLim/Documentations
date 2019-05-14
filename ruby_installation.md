# Ruby Installation Guide

This guide is for Mac Mojave (10.14.x) or higher.

## Homebrew Installation

This section is for installing Ruby using Homebrew.

### Ruby Installation

Install Ruby with Homebrew:

```bash
brew install ruby
```

Make sure to add PATH in order to use Homebrew version of Ruby to override System version of Ruby:

```bash
export PATH="/usr/local/opt/ruby/bin:$PATH"
```

Check Ruby version using:

```bash
ruby -v
```

### Gem Installation

This section is the installation guide for Gem.

#### Local Installation

Make sure to export the following variables:

```bash
# For compilers to find ruby you may need to set:
export LDFLAGS="-L/usr/local/opt/ruby/lib"
export CPPFLAGS="-I/usr/local/opt/ruby/include"

# For pkg-config to find ruby you may need to set:
export PKG_CONFIG_PATH="/usr/local/opt/ruby/lib/pkgconfig"
```

Then install the gems.

```bash
gem install --user-install bundler jekyll
```

Export the following PATH where X.X is the first two digits of the Ruby version:

```bash
export PATH=$HOME/.gem/ruby/X.X.0/bin:$PATH
```

Check the gem PATH using:

```bash
gem env
```

#### Global Installation

Due to Mojave's SIP Protections, use the following for the global installation:

```bash
sudo gem install bundler
sudo gem install -n /usr/local/bin/ jekyll
```

This is not recommended due to the use of `sudo` and Permission Errors.

## Common Source of Errors

This section describes common source of errors.

### XCode Command Line Tools

Make sure that you have updated version of XCode CLT.

```bash
xcode-select --install
```

And navigate to th XCode directory to install additional components:

```bash
cd /Library/Developer/CommandLineTools/Packages/
open macOS_SDK_headers_for_macOS_10.14.pkg
```

Also, make sure to launch `XCode App` at least once to install additional components.

## Official Documentations
* [Jekyll Documentation for MacOS](https://jekyllrb.com/docs/installation/macos/)
