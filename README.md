# homebrew-bazel

Versioned formulae for the [Bazel build tool](https://bazel.build/).

## Details
The `homebrew-core` tap contains an unversioned [formula](https://github.com/Homebrew/homebrew-core/blob/master/Formula/bazel.rb) 
for a the current version of Bazel.

However sometimes you need an earlier version of Bazel. 
E.g., when building some Bazel-using repo at a version that 
predates the current Bazel version, and therefore may not
build under it.

This Tap contains keg-only formulae for various useful versions of Bazel.


## Usage

(Replace `0.3.2` below with any version for which this repo has a formula).

- `brew tap benjyw/bazel` to add this to your tapped repositories, if
  it isn't already.
  
- `brew update` to fetch the most recent formulae.

- `brew install bazel@0.3.2`


This will install the specified version of bazel into your keg.  
To actually link it into `/usr/local` so you can use it:

`brew unlink bazel` (if you've already installed the unversioned bazel from `homebrew-core`)
`brew link bazel@0.3.2`

To restore the version from `homebrew-core`:

`brew unlink bazel@0.3.2`
`brew link bazel`