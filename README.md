# easy_localization_generator_2

<!-- [![Pub](https://img.shields.io/pub/v/easy_localization_generator.svg)](https://pub.dev/packages/easy_localization_generator)
![GitHub contributors](https://img.shields.io/github/contributors/rinlv/easy_localization_generator?style=flat-square)
![GitHub license](https://img.shields.io/github/license/rinlv/easy_localization_generator?style=flat-square) -->

Download CSV file and generates the localization keys from an online Google Sheet to working with [easy_localization](https://pub.dev/packages/easy_localization) and [easy_localization_loader](https://pub.dev/packages/easy_localization_loader)

This tool is optimized version for [easy_localization_generator](https://github.com/rinlv/easy_localization_generator)

## Installation

``` yaml
easy_localization_generator:
  git:
    url: https://github.com/YoungEii/easy_localization_generator.git
    ref: main
```

## Usage
### 1. Generate your localizations

Use command to generate a `lib/zzz/xxx.g.dart` file.

``` bash
flutter pub run build_runner build --delete-conflicting-outputs
```

Sample: [strings.g.dart](https://github.com/YoungEii/easy_localization_generator/blob/main/example/lib/localization/strings.g.dart)

### 2. Development
#### Simple text
``` dart
Text(Strings.title)
```
#### Text with args
``` dart
Text(
  Strings.msg(
    name: 'Jack',
    type: 'Hot',
  ),
),
```
#### Text with plural

``` dart
Text(Strings.amount(counter))
```

``` dart
Text(
  Strings.clicked(
    counter,
    count: counter.toString(),
  ),
),
```