Releasing HashieForbiddenAttributes
======================

There're no particular rules about when to release hashie-forbidden_attributes. Release bug fixes frequenty, features not so frequently and breaking API changes rarely.

### Release

Run tests, check that all tests succeed locally.

```
bundle install
rake
```

Check that the last build succeeded in [Travis CI](https://travis-ci.org/Maxim-Filimonov/hashie-forbidden_attributes) for all supported platforms.

Increment the version, modify [lib/hashie-forbidden_attributes/version.rb](lib/hashie-forbidden_attributes/version.rb).

*  Increment the third number if the release has bug fixes and/or very minor features, only (eg. change `0.5.1` to `0.5.2`).
*  Increment the second number if the release contains major features or breaking API changes (eg. change `0.5.1` to `0.4.0`).

Change "Next Release" in [CHANGELOG.md](CHANGELOG.md) to the new version.

```
0.4.0 (2014-01-27)
==================
```

Remove the line with "Your contribution here.", since there will be no more contributions to this release.

Commit your changes.

```
git add CHANGELOG.md lib/hashie-forbidden_attributes/version.rb
git commit -m "Preparing for release, 0.4.0."
git push origin master
```

Release.

```
$ rake release

hashie-forbidden_attributes 0.4.0 built to pkg/hashie-forbidden_attributes-0.4.0.gem.
Tagged v0.4.0.
Pushed git commits and tags.
Pushed hashie-forbidden_attributes 0.4.0 to rubygems.org.
```

### Prepare for the Next Version

Add the next release to [CHANGELOG.md](CHANGELOG.md).

```
Next Release
============

* Your contribution here.
```

Increment the minor version, modify [lib/hashie-forbidden_attributes/version.rb](lib/hashie-forbidden_attributes/version.rb).

Comit your changes.

```
git add CHANGELOG.md lib/hashie-forbidden_attributes/version.rb
git commit -m "Preparing for next release, 0.4.1."
git push origin master
```
