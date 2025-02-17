# AppSignal for Elixir Phoenix changelog

## 2.3.2

### Changed

- [5496ad2](https://github.com/appsignal/appsignal-elixir-phoenix/commit/5496ad23398e12216f184c6e9913459c3a31f7f1) patch - Switch to router_dispatch events for root spans

## 2.3.1

### Fixed

- [4e4e422](https://github.com/appsignal/appsignal-elixir-phoenix/commit/4e4e422dd9194ba0d8e3afccc955c227eacae9fb) patch - Fix exception handling for unwrapped Phoenix errors

## 2.3.0

### Added

- [2fe4d48](https://github.com/appsignal/appsignal-elixir-phoenix/commit/2fe4d489149e7a343463eb87e3e64be74a4599c1) minor - Add :telemetry-only Phoenix instrumentation to remove the need for includes in Phoenix application endpoints

## 2.2.1

### Fixed

- [25bc948](https://github.com/appsignal/appsignal-elixir-phoenix/commit/25bc948c620c24a2efe330ec76c657d945f25fce) patch - Fix metadata issue for template telemetry

## 2.2.0

### Added

- [3207e18](https://github.com/appsignal/appsignal-elixir-phoenix/commit/3207e18fe98f4dd08c843304590039acda1e3db5) minor - Add automatic template instrumentation for Phoenix 1.7. Phoenix's upcoming release adds telemetry to templates, so using Appsignal.Phoenix.View is no longer needed.

## 2.1.3

### Fixed

- [916db4b](https://github.com/appsignal/appsignal-elixir-phoenix/commit/916db4be845a8f46f293106776a2bf32683e5043) patch - Fix Appsignal.Logger error on AppSignal for Elixir 1.4.0

## 2.1.2

### Added

- [c915a34](https://github.com/appsignal/appsignal-elixir-phoenix/commit/c915a349fc4507c5266bb59130a118b2ca1e3270) patch - Handle live_component events in LiveView integration

## 2.1.1

### Added

- [fcfba2d](https://github.com/appsignal/appsignal-elixir-phoenix/commit/fcfba2dc1457176fc4998259b2d3e0ead86d0729) patch - Add event names to LiveView events

## 2.1.0

### Added

- [108d9dd](https://github.com/appsignal/appsignal-elixir-phoenix/commit/108d9dd33cc9f5465aac63d720f3d445577b9849) minor - Semi-automatic LiveView instrumentation

## 2.0.14

### Fixed

- [42b2cdd](https://github.com/appsignal/appsignal-elixir-phoenix/commit/42b2cdd816b3b54627cd77bdb3a6e87b20d5d38f) patch - Fix application environment warnings on Elixir 1.14

## 2.0.13

- [31a29c2](https://github.com/appsignal/appsignal-elixir-phoenix/commit/31a29c229211ab9e84fec5a5383fae6044c3c628) patch - Fix Telemetry 1.x warning caused by the Phoenix EventHandler

## 2.0.12

- [bd9b88d](https://github.com/appsignal/appsignal-elixir-phoenix/commit/bd9b88d4db6776a631ca59060a5412832c771dbe) patch - Remove unneeded telemetry dependency

## 2.0.11

- [aaa3146](https://github.com/appsignal/appsignal-elixir-phoenix/commit/aaa31460c4120873e45be2da61d64bf5f87ecd47) patch - Allow using phoenix_html 3.0.0 and up

## 2.0.10

- [8a219f9](https://github.com/appsignal/appsignal-elixir-phoenix/commit/8a219f9c213baaaab9cc66471f9307941b586f44) patch - Resolve duplicate view clause warnings from Appsignal.View

## 2.0.9

- [097eeaf](https://github.com/appsignal/appsignal-elixir-phoenix/commit/097eeafc66319771dc300a7bfd5b923947647e9d) patch - `Appsignal.View` returns templates when AppSignal's view instrumentation is disabled.

## 2.0.8

- [af399ef](https://github.com/appsignal/appsignal-elixir-phoenix/commit/af399efc8ad43ab7b93d34f848eb1df6d87c96ad) patch - Handle `root_view`s in phoenix_live_view 0.15.6 and up, which were made private
  in
  https://github.com/phoenixframework/phoenix_live_view/commit/8bb6f44554f22bf580048e20562b62dd6b26e2b5.
- [c19e006](https://github.com/appsignal/appsignal-elixir-phoenix/commit/c19e00695c45c5c50269fa568e550ed95e437408) patch - Don't track Phoenix render template events without root spans. For live view a lot of template events were tracked as separate incidents, causing a lot noise on the incidents overview for an app. This patch makes sure `Appsignal.View` doesn't create root spans anymore, skipping any template renders that can't be added to any existing trace.

## 2.0.7
- [af399efc](https://github.com/appsignal/appsignal-elixir-phoenix/commit/af399efc8ad43ab7b93d34f848eb1df6d87c96ad) patch - Handle `root_view`s in phoenix_live_view 0.15.6 and up, which were made private in https://github.com/phoenixframework/phoenix_live_view/commit/8bb6f44554f22bf580048e20562b62dd6b26e2b5.

## 2.0.6
* Use Appsignal.Logger in Appsignal.Phoenix.View and .EventHandler. PR #12

## 2.0.5
* Exposes live_view_action/5 to help instrument handle_params. PR #11

## 2.0.4
* Allow :appsignal_plug versions between 2.0.4 and 3.0.0

## 2.0.3
* Use “live_view” namespace for LiveView samples. PR #10

## 2.0.2
* Explicitly ignore returns from Span functions. PR #7

## 2.0.1
* Add clause for non-binary template names in AppsignalPhoenix.View. PR #6

## 2.0.0
* Initial release, extracted from appsignal-elixir 🎉
