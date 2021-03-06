# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/).

## [Unreleased]


## [0.13.0] - 2019-01-21

### Removed
- Due to library dependencies, support for Elixir 1.3, Elixir 1.4 and OTP 18.0, OTP 19.0 has been removed.
- Redix version older than 0.8.1 is no longer supported.
- Config options `reconnect_on_sleep` and `redis_timeout` are now removed.

### Added
- Support for Redix >= 0.8.1 by @ryansch and @ananthakumaran.
- Configuration for Mix Format by @chulkilee.
- Use :microsecond vs :microseconds by @KalvinHom.

## Changed
- Redis options are now passed in via `redis_options` by @ryansch and @ananthakumaran.
- Removed redix_sentinel dependency, now supported by new Redix version by @ananthakumaran.

## [0.12.2] - 2018-10-14

### Fixed
- Don't assume redis_opts is enumerable by @ryansch.

### Added
- Add {:system, VAR} format support for more config params by @LysanderGG
- Allow setting mode to both [:enqueuer, :api] by @buob

### Changed
- Specify less than 0.8.0 on redix version in mix.exs by @buob

## [0.12.1] - 2018-07-13

### Fixed
- Cleanup packaging for `elixir_uuid` change.

## [0.12.0] - 2018-07-12

### Fixed
- Change `uuid` to `elixir_uuid` which has been renamed. This will prevent future namespace clashes by @tzilist.

## [0.11.0] - 2018-05-12

### Added
- Trim dead jobs queue after certain size by @ananthakumaran.
- Add an api to list all subscriptions (active queues) by @robobakery.
- Have top supervisor wait for worker drainer to gracefully terminate @frahugo.

## [0.10.1] - 2018-02-11

### Fixed
- Fix retry for Sidekiq job format using retry => true by @deepfryed.

## [0.10.0] - 2018-02-11

### Fixed
- Remove Password logging by @akira.

### Added
- Redis Sentinel support by @ananthakumaran.
- Make redis module name and start_link args configurable @ananthakumaran.


