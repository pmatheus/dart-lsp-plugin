---
name: dart-lsp-usage
description: >-
  This skill should be used when the user asks about "Dart code analysis",
  "Flutter development", "Dart LSP features", "code navigation in Dart",
  or mentions analyzing, refactoring, or understanding Dart/Flutter code.
version: 0.1.0
---

# Dart LSP Integration

## Purpose

This skill provides guidance on using the Dart Language Server Protocol (LSP) integration with Claude Code for intelligent Dart and Flutter development.

## When to Use

- Analyzing Dart or Flutter code
- Navigating Dart codebases
- Finding references, definitions, or implementations
- Getting code completions and diagnostics
- Refactoring Dart code
- Understanding Flutter widget trees

## Available LSP Features

### Code Navigation
- **Go to Definition**: Jump to where a symbol is defined
- **Find References**: Find all usages of a symbol
- **Go to Implementation**: Find implementations of abstract members
- **Document Symbols**: List all symbols in a file
- **Workspace Symbols**: Search symbols across the project

### Code Intelligence
- **Hover Information**: Type info and documentation on hover
- **Code Completion**: Smart completions with auto-imports
- **Signature Help**: Parameter hints for functions
- **Diagnostics**: Real-time error and warning detection

### Code Actions
- **Quick Fixes**: Automatic fixes for common issues
- **Refactoring**: Rename, extract method, extract widget
- **Organize Imports**: Sort and remove unused imports
- **Format Document**: Apply Dart formatter

## Quick Reference

### Common LSP Operations

```
# Get symbol definition
LSP goToDefinition on file.dart at line:column

# Find all references
LSP findReferences on file.dart at line:column

# Get hover information
LSP hover on file.dart at line:column

# Get document symbols
LSP documentSymbol on file.dart
```

### Flutter-Specific Features

The Dart LSP includes Flutter-specific enhancements:

- **Flutter Outline**: Widget tree structure
- **Closing Labels**: Virtual labels for closing brackets
- **Flutter Fixes**: Flutter-specific quick fixes
- **Widget Refactoring**: Extract widget, wrap with widget

## Best Practices

1. **Use LSP over grep**: For semantic code understanding, prefer LSP tools
2. **Check diagnostics first**: Before modifying code, check for existing errors
3. **Leverage auto-imports**: Let the LSP suggest imports automatically
4. **Use refactoring tools**: For renaming and restructuring, use LSP refactoring

## Troubleshooting

### Server Not Starting
- Ensure `dart` is in your PATH
- Run `dart --version` to verify installation
- Check that Dart SDK is properly installed

### Missing Features
- Some features require a `pubspec.yaml` in the project
- Run `dart pub get` to resolve dependencies
- Flutter features require Flutter SDK

### Performance Issues
- Large projects may need `onlyAnalyzeProjectsWithOpenFiles: true`
- Close unused files to reduce memory usage
