# dart-lsp-plugin

A Claude Code plugin that integrates the Dart Language Server Protocol (LSP) for intelligent Dart and Flutter development.

## Features

- **Code Navigation**: Go to definition, find references, find implementations
- **Code Intelligence**: Hover information, completions, signature help
- **Diagnostics**: Real-time error and warning detection
- **Code Actions**: Quick fixes, refactoring, organize imports
- **Flutter Support**: Widget outline, Flutter-specific fixes and refactoring

## Requirements

- [Dart SDK](https://dart.dev/get-dart) installed and available in PATH
- For Flutter projects: [Flutter SDK](https://flutter.dev/docs/get-started/install)

## Installation

In Claude Code, run `/plugins` and then:

### 1. Add the marketplace (one-time setup)

```
add marketplace https://raw.githubusercontent.com/pmatheus/dart-lsp-plugin/main
```

### 2. Install the plugin

```
install dart-lsp
```

## Usage

Once installed, the plugin automatically activates when you work with Dart files (`.dart`).

### Available LSP Features

The Dart LSP provides these capabilities through Claude Code:

| Feature | Description |
|---------|-------------|
| Definition | Jump to symbol definitions |
| References | Find all usages of a symbol |
| Hover | View type info and documentation |
| Completion | Smart code completions with auto-import |
| Diagnostics | Error and warning detection |
| Formatting | Apply Dart formatter |
| Code Actions | Quick fixes and refactoring |

### Example Queries

- "Analyze this Dart file for errors"
- "Find all references to the UserService class"
- "Go to the definition of this method"
- "What does this Flutter widget do?"
- "Refactor this code to extract a method"

## Configuration

The plugin comes with sensible defaults. The following options are pre-configured:

```json
{
  "onlyAnalyzeProjectsWithOpenFiles": true,
  "suggestFromUnimportedLibraries": true,
  "closingLabels": true,
  "outline": true,
  "flutterOutline": true,
  "dart.enableSdkFormatter": true,
  "dart.lineLength": 80,
  "dart.completeFunctionCalls": true,
  "dart.showTodos": true
}
```

## Troubleshooting

### Dart not found

Ensure the Dart SDK is installed and `dart` is in your PATH:

```bash
dart --version
```

### LSP not starting

1. Verify Dart installation: `which dart`
2. Test the language server: `dart language-server --help`
3. Check for SDK updates: `dart pub upgrade`

### Missing Flutter features

Flutter-specific features require the Flutter SDK:

```bash
flutter doctor
```

## License

MIT

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.
