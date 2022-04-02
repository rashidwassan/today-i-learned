## Add these following lines in settings json file to make flutter project directory look simpler.

```json
"explorer.experimental.fileNesting.enabled": true,
"explorer.experimental.fileNesting.expand": false,
"explorer.experimental.fileNesting.patterns": {
    "pubspec.yaml": ".flutter-plugins, .packages, .dart_tool, .flutter-plugins-dependencies, .metadata, .packages, pubspec.lock, build.yaml, analysis_options.yaml, all_lint_rules.yaml",
    ".gitignore": ".gitattributes, .gitmodules, .gitmessage, .mailmap, .git-blame*",
    "readme.*": "authors, backers.md, changelog*, citation*, code_of_conduct.md, codeowners, contributing.md, contributors, copying, credits, governance.md, history.md, license*, maintainers, readme*, security.md, sponsors.md",
    "*.dart": "$(capture).g.dart, $(capture).freezed.dart",
},
```

## Add these lines to fix dart lints and imports on every save.
```json
    "editor.codeActionsOnSave": {
        "source.fixAll.dart": true,
        "source.organizeImports": true,
        "source.organizeDirectives": true, 
    },
```

## If you want to call two different methods from the same class, you can do it simply:
```dart
    // traditional approach
    ExampleClass().hello();
    ExampleClass().hi();
    // easy approach
    ExampleClass()..hello()..hi();
```