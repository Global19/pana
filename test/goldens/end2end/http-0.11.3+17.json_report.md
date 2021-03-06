## 10/20 Follow Dart file conventions

### [x] 0/10 points: Provide a valid `pubspec.yaml`

<details>
<summary>
The package description is too short.
</summary>

Add more detail to the `description` field of `pubspec.yaml`. Use 60 to 180 characters to describe the package, what it does, and its target use case.
</details>

### [*] 5/5 points: Provide a valid `README.md`


### [*] 5/5 points: Provide a valid `CHANGELOG.md`


## 0/10 Provide documentation

### [x] 0/10 points: Package has an example

<details>
<summary>
No example found.
</summary>

See [package layout](https://dart.dev/tools/pub/package-layout#examples) guidelines on how to add an example.
</details>

## 10/20 Support multiple platforms

### [~] 10/20 points: Supports 1 of 2 possible platforms (**native**, js)

Consider supporting multiple platforms:

<details>
<summary>
Package not compatible with runtime js
</summary>

Because:
* `package:http/http.dart` that imports:
* `package:http/src/streamed_response.dart` that imports:
* `package:http/src/base_request.dart` that imports:
* `package:http/src/client.dart` that imports:
* `package:http/src/io_client.dart` that imports:
* `dart:io`
</details>

## 20/30 Pass static analysis

### [~] 20/30 points: code has no errors, warnings, lints, or formatting issues

Found 202 issues. Showing the first 2:

<details>
<summary>
INFO: Use collection literals when possible.
</summary>

`lib/browser_client.dart:30:17`

```
   ╷
30 │   final _xhrs = new Set<HttpRequest>();
   │                 ^^^^^^^^^^^^^^^^^^^^^^
   ╵
```

To reproduce make sure you are using [pedantic](https://pub.dev/packages/pedantic#using-the-lints) and run `dartanalyzer lib/browser_client.dart`
</details>
<details>
<summary>
INFO: Unnecessary new keyword.
</summary>

`lib/browser_client.dart:30:17`

```
   ╷
30 │   final _xhrs = new Set<HttpRequest>();
   │                 ^^^^^^^^^^^^^^^^^^^^^^
   ╵
```

To reproduce make sure you are using [pedantic](https://pub.dev/packages/pedantic#using-the-lints) and run `dartanalyzer lib/browser_client.dart`
</details>

## 0/20 Support up-to-date dependencies

### [x] 0/10 points: All of the package dependencies are supported in the latest version

* Could not run pub outdated: `pub get` failed: 

 ```
The current Dart SDK version is {{sdk-version}}.

Because http depends on unittest >=0.2.8+2 which requires SDK version <2.0.0, version solving failed.
```

### [x] 0/10 points: Package supports latest stable Dart and Flutter SDKs

* Found no Flutter in your PATH. Could not determine the current Flutter version.

## 0/0 Support sound null-safety

### [~] 0/0 points: Package does not opt in to null-safety.

Packages with full null-safety support will be awarded additional points in a planned future revision of the pub.dev points model.

<details>
<summary>
Package language version (indicated by the sdk constraint `>=2.0.0-dev.61.0 <3.0.0`) is less than 2.12.
</summary>

Consider [migrating](https://dart.dev/null-safety/migration-guide).
</details>