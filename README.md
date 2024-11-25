# fba_demo

## 1. Flutter create project

Create a new project `fba_demo`

## 2. Flutter add firebase_analytics and firebase_core

Add the following to pubspec.yaml

```
dependencies:
  firebase_analytics: ^11.3.5
  firebase_core: ^3.8.0
```

## 3. Flutter run macos

Fails with 

> Error: The pod "Firebase/Analytics" required by the plugin "firebase_analytics" requires a higher minimum macOS deployment version than the plugin's reported minimum version.

```
$ flutter run -d macOS

Launching lib/main.dart on macOS in debug mode...
Running pod install...
CocoaPods' output:
↳
Preparing

    Analyzing dependencies

    Inspecting targets to integrate
      Using `ARCHS` setting to build architectures of target `Pods-Runner`: (``)
      Using `ARCHS` setting to build architectures of target `Pods-RunnerTests`: (``)

    Fetching external sources
    -> Fetching podspec for `FlutterMacOS` from `Flutter/ephemeral`
    -> Fetching podspec for `firebase_analytics` from `Flutter/ephemeral/.symlinks/plugins/firebase_analytics/macos`
    firebase_analytics: Using Firebase SDK version '11.4.0' defined in 'firebase_core'
    -> Fetching podspec for `firebase_core` from `Flutter/ephemeral/.symlinks/plugins/firebase_core/macos`
    firebase_core: Using Firebase SDK version '11.4.0' defined in 'firebase_core'

    Resolving dependencies of `Podfile`
      CDN: trunk Relative path: CocoaPods-version.yml exists! Returning local because checking is only performed in repo update
      CDN: trunk Relative path: all_pods_versions_0_3_5.txt exists! Returning local because checking is only performed in repo update
      CDN: trunk Relative path: Specs/0/3/5/Firebase/11.5.0/Firebase.podspec.json exists! Returning local because checking is only performed in repo update
      CDN: trunk Relative path: Specs/0/3/5/Firebase/11.4.0/Firebase.podspec.json exists! Returning local because checking is only performed in repo update
      CDN: trunk Relative path: Specs/0/3/5/Firebase/11.4.0/Firebase.podspec.json exists! Returning local because checking is only performed in repo update
      CDN: trunk Relative path: Specs/0/3/5/Firebase/11.4.1/Firebase.podspec.json exists! Returning local because checking is only performed in repo update
      CDN: trunk Relative path: Specs/0/3/5/Firebase/11.4.2/Firebase.podspec.json exists! Returning local because checking is only performed in repo update
      CDN: trunk Relative path: Specs/0/3/5/Firebase/11.4.0/Firebase.podspec.json exists! Returning local because checking is only performed in repo update
    [!] CocoaPods could not find compatible versions for pod "Firebase/Analytics":
      In Podfile:
        firebase_analytics (from `Flutter/ephemeral/.symlinks/plugins/firebase_analytics/macos`) was resolved to 11.3.5, which depends on
          Firebase/Analytics (= 11.4.0)

    Specs satisfying the `Firebase/Analytics (= 11.4.0)` dependency were found, but they required a higher minimum deployment target.

    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/molinillo-0.8.0/lib/molinillo/resolution.rb:317:in `raise_error_unless_state'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/molinillo-0.8.0/lib/molinillo/resolution.rb:299:in `block in unwind_for_conflict'
    <internal:kernel>:90:in `tap'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/molinillo-0.8.0/lib/molinillo/resolution.rb:297:in `unwind_for_conflict'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/molinillo-0.8.0/lib/molinillo/resolution.rb:682:in `attempt_to_activate'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/molinillo-0.8.0/lib/molinillo/resolution.rb:254:in `process_topmost_state'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/molinillo-0.8.0/lib/molinillo/resolution.rb:182:in `resolve'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/molinillo-0.8.0/lib/molinillo/resolver.rb:43:in `resolve'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/cocoapods-1.16.2/lib/cocoapods/resolver.rb:94:in `resolve'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/cocoapods-1.16.2/lib/cocoapods/installer/analyzer.rb:1082:in `block in resolve_dependencies'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/cocoapods-1.16.2/lib/cocoapods/user_interface.rb:64:in `section'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/cocoapods-1.16.2/lib/cocoapods/installer/analyzer.rb:1080:in `resolve_dependencies'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/cocoapods-1.16.2/lib/cocoapods/installer/analyzer.rb:125:in `analyze'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/cocoapods-1.16.2/lib/cocoapods/installer.rb:422:in `analyze'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/cocoapods-1.16.2/lib/cocoapods/installer.rb:244:in `block in resolve_dependencies'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/cocoapods-1.16.2/lib/cocoapods/user_interface.rb:64:in `section'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/cocoapods-1.16.2/lib/cocoapods/installer.rb:243:in `resolve_dependencies'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/cocoapods-1.16.2/lib/cocoapods/installer.rb:162:in `install!'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/cocoapods-1.16.2/lib/cocoapods/command/install.rb:52:in `run'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/claide-1.1.0/lib/claide/command.rb:334:in `run'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/cocoapods-1.16.2/lib/cocoapods/command.rb:52:in `run'
    /Users/kaye375751/.rbenv/versions/3.2.2/lib/ruby/gems/3.2.0/gems/cocoapods-1.16.2/bin/pod:55:in `<top (required)>'
    /Users/kaye375751/.rbenv/versions/3.2.2/bin/pod:25:in `load'
    /Users/kaye375751/.rbenv/versions/3.2.2/bin/pod:25:in `<main>'

Error: The pod "Firebase/Analytics" required by the plugin "firebase_analytics" requires a higher minimum macOS deployment version than the plugin's reported minimum version.
To build, remove the plugin "firebase_analytics", or contact the plugin's developers for assistance.
Error: Error running pod install
```
