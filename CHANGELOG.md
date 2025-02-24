# Changelog

All notable changes to eww will be listed here, starting at changes since version 0.1.2.


## [Unreleased]

### BREAKING CHANGES
- Change the onclick command API to support multiple placeholders.
  This changes. the behaviour of the calendar widget's onclick as well as the onhover and onhoverlost
  events. Instead of providing the entire date (or, respecively, the x and y mouse coordinates) in
  a single value (`day.month.year`, `x y`), the values are now provided as separate placeholders.
  The day can now be accessed with `{0}`, the month with `{1}`, and the year with `{2}`, and
  similarly x and y are accessed with `{0}` and `{1}`.

### Features
- Add `eww inspector` command
- Add `--no-daemonize` flag
- Add support for displaying marks on `scale`-widget (By: druskus20)
- Add `children`-widget that allows custom widgets to make use of children
- Add support for `:hover` css selectors for eventbox (By: druskus20)
- Add `eww get` subcommand (By: druskus20)
- Add circular progress widget (By: druskus20)
- Add graph widget (By: druskus20)
- Add `>=` and `<=` operators to simplexpr (By: viandoxdev)
- Add `desktop` window type (By: Alvaro Lopez)
- Add `scroll` widget (By: viandoxdev)
- Add `notification` window type
- Add drag and drop functionality to eventbox
- Add `search`, `captures`, `stringlength`, `arraylength` and `objectlength` functions for expressions (By: MartinJM, ElKowar)
- Add `matches` function
- Add transform widget (By: druskus20)

### Notable Internal changes
- Rework state management completely, now making local state and dynamic widget hierarchy changes possible.

### Notable fixes and other changes
- Fix `onscroll` gtk-bug where the first event is emitted incorrectly (By: druskus20)
- Allow windows to get moved when windowtype is `normal`
- Added more examples
- List system-level dependencies in documentation
- Document structure of magic variables (By: legendofmiracles)
