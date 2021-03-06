# rbenv-railsexpress

This repository contains the rbenv (ruby-build) build instructions for the
railsexpress patched versions of ruby.

## USAGE

Install the necessary binaries with homebrew first:

- `brew install rbenv`
- `brew install rbenv-aliases`
- `brew install ruby-build`
- clone this repository to with `git clone https://github.com/xing/rbenv-patchsets.git ~/.rbenv/plugins/ruby-build-railsexpress`.
- install a railsexpressed version, e.g. : `rbenv install 2.5.1-railsexpress`
- `rbenv alias --auto` creates an alias `2.5.1` for `2.5.1-railsexpress`

## TROUBLESHOOTING

On OSX El Capitan it can happen that gems fail to build because of openssl errors.
The following command might help:
```
gem install eventmachine -v '1.0.8' -- --with-cppflags=-I/usr/local/opt/openssl/include
```
