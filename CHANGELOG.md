# Changelog

The repo is versioned based on [SemVer 2.0](https://semver.org/spec/v2.0.0.html) using the tiny-but-mighty [MinVer](https://github.com/adamralph/minver) from [@adamralph](https://github.com/adamralph). [See here](https://github.com/adamralph/minver#how-it-works) for more information on how it works.

All notable changes to this project will be documented in this file. The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

The `Unreleased` section name is replaced by the expected version of next release. A stable version's log contains all changes between that version and the previous stable version (can duplicate the prereleases logs).

## [Unreleased]

### Added
### Changed
### Removed
### Fixed

<a name="1.0.1-rc8"></a>
## [1.0.1-rc8] - 2019-07-05

### Changed

- `Kafka`/`Kafka0`: Tuned stream producer params

<a name="1.0.1-rc7"></a>
## [1.0.1-rc7] - 2019-07-04

### Added

- `Kafka`: Log `Producer` exceptions
- `Kafka`: `StreamsProducerSink` Enable control of `maxEvents`, `maxBytes`

### Fixed

- `Propulsion`/`Propulsion.Kafka`/`Propulsion.Kafka0`: Removed `IEvent` on `StreamEvent`, `IEnumerable<IEvent>` on `StreamEventSpan`

<a name="1.0.1-rc6"></a>
## [1.0.1-rc6] - 2019-07-03

### Changed

- `Kafka`/`Kafka0`: Rename `Producers` to `Producer`, add deprecation not to [renamed] `degreeOfParallelism` parameter

### Fixed

- `Kafka0` - added missing error check on produce [#14](https://github.com/jet/propulsion/pull/14)

<a name="1.0.1-rc5"></a>
## [1.0.1-rc5] - 2019-07-02

### Added

- `Propulsion`: Implement `IEvent` on `StreamEvent`, `IEnumerable<IEvent>` on `StreamEventSpan`
- `Propulsion.Kafka`: Implemented `IEnumerable<IEvent>` on `RenderedSpan`
- `Propulsion.Kafka`: Added `Parse`, `parseStreamEvents` helpers to `RenderedSpan`

<a name="1.0.1-rc4"></a>
## [1.0.1-rc4] - 2019-07-01

### Changed

- `.Kafka`: Targeted `Jet.ConfluentKafka.FSharp` v `1.1.0`

### Fixed

- Idling logic bug [#13](https://github.com/jet/propulsion/pull/13)
- `EventStoreSource`: Gorging -> Tailing transition [#10](https://github.com/jet/propulsion/issues/10) [#13](https://github.com/jet/propulsion/pull/13)

<a name="1.0.1-rc3"></a>
## [1.0.1-rc3] - 2019-06-18

### Added

- `Core`: Average Streams latency measurements/loggging for `StreamsConsumer` [#3](https://github.com/jet/propulsion/pull/3)
- `Kafka`: `customize` option for `ParallelConsumer` and `StreamsConsumer`'s `.Create` methods [#3](https://github.com/jet/propulsion/pull/3)
- `Kafka`: `producerParallelism` option [#3](https://github.com/jet/propulsion/pull/3)
- `Kafka0`: Provides source-compatibility with `Propulsion.Kafka` targeting `Jet.ConfluentKafka.FSharp` v `0.9.1` / `Confluent.Kafka` v `1.0.1` [#4](https://github.com/jet/propulsion/pull/4)
- `Kafka`/`Kafka0`: `Producers` - Common Kafka producer wrapper with metrics [#9](https://github.com/jet/propulsion/pull/9)
- `Kafka`/`Kafka0`: `StreamsConsumerStats` - Consumer outcome / statistics / logging support [#9](https://github.com/jet/propulsion/pull/9)

### Changed

- `Propulsion.Cosmos`: Tidied Cosmos ingester lag breakdown
- Moved `RenderedSpan` et al to `Propulsion.Codec.NewtonsoftJson` [#5](https://github.com/jet/propulsion/pull/5)
- Targeted `Jet.ConfluentKafka.FSharp` v `1.0.1` [#3](https://github.com/jet/propulsion/pull/3)
- Targeted `Equinox`.* v `2.0.0-rc1` [#3](https://github.com/jet/propulsion/pull/7)

<a name="1.0.1-rc2"></a>
## [1.0.1-rc2] - 2019-06-07

### Added

- `Propulsion.EventStore.EventStoreSource` (productized from `Equinox.Templates`'s `eqxsync`) [#1](https://github.com/jet/propulsion/pull/1)

### Changed

- Targets `Microsoft.Azure.DocumentDB.ChangeFeedProcessor` v `2.2.7`, which includes critical lease management improvements

<a name="1.0.1-rc1"></a>
## [1.0.1-rc1] - 2019-06-03

### Added

- `Propulsion.Kafka.Codec.RenderedSpan` (nee `Equinox.Projection.Codec.RenderedSpan`, which is deprecated and is being removed)
- `Propulsion.EventStore`, `Propulsion.Cosmos` (productized from `Equinox.Templates`'s `eqxsync` and `eqxprojector`)

### Changed

- Targets `Jet.ConfluentKafka.FSharp` v `1.0.1`

<a name="1.0.0-rc13"></a>
## [1.0.0-rc13] - 2019-06-01

### Added

- `StreamsConsumer` and `StreamsProducer` [#35](https://github.com/jet/Jet.ConfluentKafka.FSharp/pull/35)
- `ParallelProducer` [#36](https://github.com/jet/Jet.ConfluentKafka.FSharp/pull/36)

### Changed

- Split reusable components of `ParallelConsumer` out into independent `Propulsion` and `Propulsion.Kafka` libraries [#34](https://github.com/jet/Jet.ConfluentKafka.FSharp/pull/34)

## 1.0.0-rc12 - 2019-05-31

### Fixed

- Significant tuning / throughput improvements for `ParallelConsumer` 

## 1.0.0-rc11 - 2019-05-27

### Added

- `ParallelConsumer` [#33](https://github.com/jet/Jet.ConfluentKafka.FSharp/pull/33)

## squashed prior to initial relevant commit

(Stripped down repo for history purposes, see [`master` branch of Jet.ConfluentKafka.FSharp for complete history prior to 1.0.0-rc13](https://github.com/jet/Jet.ConfluentKafka.FSharp/blob/master/CHANGELOG.md))

[Unreleased]: https://github.com/jet/propulsion/compare/1.0.1-rc8...HEAD
[1.0.1-rc8]: https://github.com/jet/propulsion/compare/1.0.1-rc7...1.0.1-rc8
[1.0.1-rc7]: https://github.com/jet/propulsion/compare/1.0.1-rc6...1.0.1-rc7
[1.0.1-rc6]: https://github.com/jet/propulsion/compare/1.0.1-rc5...1.0.1-rc6
[1.0.1-rc5]: https://github.com/jet/propulsion/compare/1.0.1-rc4...1.0.1-rc5
[1.0.1-rc4]: https://github.com/jet/propulsion/compare/1.0.1-rc3...1.0.1-rc4
[1.0.1-rc3]: https://github.com/jet/propulsion/compare/1.0.1-rc2...1.0.1-rc3
[1.0.1-rc2]: https://github.com/jet/propulsion/compare/1.0.1-rc1...1.0.1-rc2
[1.0.1-rc1]: https://github.com/jet/propulsion/compare/1.0.0-rc13...1.0.1-rc1
[1.0.0-rc13]: https://github.com/jet/propulsion/compare/d2caf9a007a137994e91ab709c87eb29fe32489b...1.0.0-rc13