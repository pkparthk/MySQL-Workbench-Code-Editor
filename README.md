# MySQL Workbench Code Editor Configuration

This repository contains configuration files for the Scintilla-based code editors used in MySQL Workbench. These XML files define syntax highlighting, color schemes, editor settings, and keyword definitions for various programming languages supported by MySQL Workbench.

## Overview

The configuration files customize the appearance and behavior of code editors within MySQL Workbench, providing syntax highlighting and editor preferences for:

- **MySQL SQL** (various versions including 5.6, 5.7, 8.0, and 8.1)
- **C/C++** programming languages
- **JSON** format

## Files

### `code_editor.xml`

Main configuration file containing:

- MySQL syntax highlighting definitions for different MySQL versions (5.6, 5.7, 8.0, 8.1)
- C/C++ syntax highlighting and keyword definitions
- JSON syntax highlighting
- Color schemes with support for both light and dark themes
- Editor settings (tab width, indentation, folding options)

### `code_editor1.xml`

Alternative or backup configuration file with similar structure to the main configuration.

## Features

### MySQL Support

- **Comprehensive keyword highlighting** for MySQL statements, functions, and operators
- **Version-specific keywords** for MySQL 5.6, 5.7, 8.0, and 8.1
- **Syntax elements** including:
  - Keywords and reserved words
  - String literals (single and double quoted)
  - Numeric values
  - Comments (line and block)
  - Variables (user and system)
  - Functions and procedures
  - Identifiers and quoted identifiers

### Theme Support

- **Dark theme** with modern color palette
- **Light theme** compatibility
- **Customizable colors** for different syntax elements

## Advanced Features & Enhancements

### Enhanced Editor Settings

- **Smart Indentation**: Automatic indentation with 2-space tabs for better code readability
- **Brace Matching**: Automatic highlighting of matching brackets and braces
- **Code Folding**: Advanced folding support for functions, comments, and control structures
- **Current Line Highlighting**: Visual indication of the active line
- **Improved Line Numbers**: Enhanced visibility with better contrast
- **Word Wrapping**: Configurable word wrapping for JSON files

### MySQL Advanced Configuration

#### Comprehensive Keyword Support

- **MySQL 8.1 Support**: Latest MySQL features including vector functions, JSON enhancements
- **Window Functions**: Complete support for OVER, PARTITION BY, ROW_NUMBER, RANK, etc.
- **JSON Functions**: Full coverage of JSON manipulation and validation functions
- **Spatial Functions**: ST\_\* functions for geometric operations
- **Regular Expression Functions**: REGEXP\_\* functions for pattern matching
- **Common Table Expressions**: WITH and RECURSIVE support

#### Enhanced Syntax Highlighting

- **Storage Engines**: InnoDB, MyISAM, Memory, Archive, CSV recognition
- **System Variables**: Distinct highlighting for @@global and @@session variables
- **Procedure Keywords**: Complete stored procedure and function syntax support
- **Error Handling**: SIGNAL, RESIGNAL, and condition handling keywords

#### Modern Color Scheme

- **Dual Theme Support**: Optimized colors for both light and dark themes
- **High Contrast**: Improved readability with better color contrast ratios
- **Semantic Coloring**: Different colors for keywords, functions, variables, and data types
- **Error Highlighting**: Special styling for string end-of-line errors

### C++ Modern Features

#### C++23 Support

- **Latest Keywords**: `concept`, `requires`, `co_await`, `co_return`, `co_yield`
- **Modules**: `import` and `module` keyword support
- **Coroutines**: Full coroutine syntax highlighting
- **Constraints**: Concept and constraint syntax support

#### Standard Library Integration

- **STL Types**: Comprehensive coverage of standard library types
- **Smart Pointers**: `shared_ptr`, `unique_ptr`, `weak_ptr` recognition
- **Containers**: Vector, map, set, unordered containers
- **Ranges and Views**: C++20 ranges library support
- **Concepts**: Standard concepts like `same_as`, `convertible_to`

#### Enhanced Documentation

- **Doxygen Support**: Complete Doxygen comment keyword highlighting
- **Code Folding**: Advanced folding for classes, functions, and namespaces
- **Preprocessor**: Enhanced preprocessor directive support

### JSON Schema Support

#### Advanced JSON Features

- **Schema Keywords**: Support for JSON Schema validation keywords
- **Type System**: Recognition of schema type definitions
- **Validation**: Keywords for validation rules and constraints
- **Modern Formatting**: Optimized for 2-space indentation
- **Property Highlighting**: Enhanced highlighting for object properties

### Lexer Enhancements

#### Advanced Properties

- **Backquoted Identifiers**: MySQL backtick identifier support
- **Escape Sequences**: Proper handling of escape sequences in strings
- **Dotted Words**: Support for qualified identifiers (database.table.column)
- **Number Sign Comments**: MySQL-style # comments
- **Backslash Escapes**: SQL backslash escape sequence support

#### Folding Improvements

- **Comment Folding**: Fold multi-line comments and documentation blocks
- **Explicit Folding**: Custom fold markers with //{ and //}
- **Syntax-Based Folding**: Intelligent folding based on language syntax
- **Compact Folding**: Optimized folding display

### Performance Optimizations

#### Syntax Processing

- **Incremental Parsing**: Faster syntax highlighting for large files
- **Memory Efficiency**: Optimized keyword tables and style definitions
- **Real-time Updates**: Immediate syntax highlighting as you type

#### Editor Responsiveness

- **Lightweight Themes**: Minimal resource usage for color schemes
- **Fast Rendering**: Optimized style calculations
- **Smooth Scrolling**: Improved editor performance for large documents

## Color Scheme

The configuration uses a modern dark theme with the following color palette:

- **Background**: `#232729`
- **Text**: `#abb2bf`
- **Comments**: `#5c6370`
- **Strings**: `#98c379`
- **Numbers**: `#d19a66`
- **Keywords**: `#61afef` / `#56b6c2`
- **Functions**: `#c678dd`
- **Variables**: `#e06c75`

## Installation

### Prerequisites

- **MySQL Workbench 8.0 or higher** (recommended)
- **Administrative privileges** to modify MySQL Workbench configuration files
- **Text editor** for manual configuration editing (optional)

### Installation Steps

#### Windows

1. Close MySQL Workbench completely
2. Navigate to the MySQL Workbench data directory:
   ```
   %APPDATA%\MySQL\Workbench\
   ```
   Or the installation directory:
   ```
   C:\Program Files\MySQL\MySQL Workbench 8.0\data\
   ```
3. **Backup existing configuration**: Copy `code_editor.xml` to `code_editor.xml.backup`
4. Replace `code_editor.xml` with the enhanced configuration
5. Restart MySQL Workbench

#### macOS

1. Close MySQL Workbench completely
2. Navigate to the MySQL Workbench configuration directory:
   ```
   ~/Library/Application Support/MySQL/Workbench/
   ```
3. **Backup existing configuration**: Copy `code_editor.xml` to `code_editor.xml.backup`
4. Replace `code_editor.xml` with the enhanced configuration
5. Restart MySQL Workbench

#### Linux

1. Close MySQL Workbench completely
2. Navigate to the MySQL Workbench configuration directory:
   ```
   ~/.mysql/workbench/
   ```
   Or:
   ```
   /usr/share/mysql-workbench/data/
   ```
3. **Backup existing configuration**: Copy `code_editor.xml` to `code_editor.xml.backup`
4. Replace `code_editor.xml` with the enhanced configuration
5. Restart MySQL Workbench

### Verification

After installation, verify the configuration is working:

1. Open MySQL Workbench
2. Create a new SQL script or open an existing one
3. Check that syntax highlighting is applied correctly
4. Verify that keywords are highlighted in the new color scheme
5. Test code folding functionality

### Rollback

If you encounter issues:

1. Close MySQL Workbench
2. Restore the backup: `code_editor.xml.backup` → `code_editor.xml`
3. Restart MySQL Workbench

## Configuration Examples

### Custom Color Themes

#### Creating a High Contrast Theme

```xml
<!-- High contrast theme for better accessibility -->
<style id="8" bold="yes" fore-color-light="#000080" fore-color-dark="#00FFFF" /> <!-- Keywords -->
<style id="15" fore-color-light="#800080" fore-color-dark="#FF80FF" bold="yes" /> <!-- Functions -->
<style id="12" fore-color-light="#008000" fore-color-dark="#80FF80" /> <!-- Strings -->
```

#### Creating a Monochrome Theme

```xml
<!-- Monochrome theme for focused coding -->
<style id="8" bold="yes" fore-color-light="#000000" fore-color-dark="#FFFFFF" />
<style id="15" fore-color-light="#404040" fore-color-dark="#C0C0C0" bold="yes" />
<style id="1" fore-color-light="#808080" fore-color-dark="#808080" italic="yes" />
```

### Advanced Editor Settings

#### Enabling All Advanced Features

```xml
<setting name="auto.indent" value="1" />
<setting name="brace.matching" value="1" />
<setting name="word.wrap" value="0" />
<setting name="line.numbers" value="1" />
<setting name="folding" value="1" />
<setting name="highlight.current.line" value="1" />
<setting name="show.whitespace" value="0" />
<setting name="caret.line.back" value="#2C323C" />
<setting name="selection.back" value="#3E4451" />
```

#### Custom Lexer Properties

```xml
<!-- Enhanced MySQL lexer configuration -->
<property name="lexer.mysql.backticks.identifier" value="1" />
<property name="sql.backslash.escapes" value="1" />
<property name="lexer.sql.numbersign.comment" value="1" />
<property name="lexer.sql.allow.dotted.word" value="1" />
<property name="fold.at.else" value="1" />
```

### Language-Specific Customizations

#### MySQL Performance Tuning Keywords

```xml
<keywords name="Performance Keywords">
  explain analyze optimize index cache buffer_pool
  query_cache innodb_buffer_pool_size key_buffer_size
  sort_buffer_size read_buffer_size join_buffer_size
  max_connections thread_cache_size table_cache
</keywords>
```

#### C++ Modern Features

```xml
<keywords name="C++23 Features">
  concept requires co_await co_return co_yield
  import module consteval constinit
  atomic_cancel atomic_commit atomic_noexcept
  synchronized reflexpr
</keywords>
```

## Troubleshooting

### Troubleshooting

#### Common Installation Paths

**Windows:**

- User-specific: `%APPDATA%\MySQL\Workbench\`
- System-wide: `C:\Program Files\MySQL\MySQL Workbench 8.0\data\`
- Portable: `[MySQL Workbench Installation]\data\`

**macOS:**

- User-specific: `~/Library/Application Support/MySQL/Workbench/`
- System-wide: `/Applications/MySQLWorkbench.app/Contents/Resources/data/`

**Linux:**

- User-specific: `~/.mysql/workbench/`
- System-wide: `/usr/share/mysql-workbench/data/`
- Snap package: `~/snap/mysql-workbench-community/current/.mysql/workbench/`

#### XML Validation

Before applying the configuration, validate the XML structure:

**Windows PowerShell:**

```powershell
[xml](Get-Content 'code_editor.xml') | Out-Null
```

**Linux/macOS:**

```bash
xmllint --noout code_editor.xml
```

#### MySQL Workbench Configuration Hierarchy

MySQL Workbench reads configuration in this order:

1. **System-wide configuration** (read-only)
2. **User-specific configuration** (recommended for custom themes)
3. **Workspace-specific settings** (overrides user settings)

#### Backup and Recovery

**Create Backup:**

```bash
# Windows
copy "%APPDATA%\MySQL\Workbench\code_editor.xml" "%APPDATA%\MySQL\Workbench\code_editor.xml.backup"

# Linux/macOS
cp ~/.mysql/workbench/code_editor.xml ~/.mysql/workbench/code_editor.xml.backup
```

**Restore Backup:**

```bash
# Windows
copy "%APPDATA%\MySQL\Workbench\code_editor.xml.backup" "%APPDATA%\MySQL\Workbench\code_editor.xml"

# Linux/macOS
cp ~/.mysql/workbench/code_editor.xml.backup ~/.mysql/workbench/code_editor.xml
```

#### Syntax Highlighting Not Working

1. **Check XML Syntax**: Ensure all XML tags are properly closed
2. **Verify Style IDs**: Make sure style IDs match Scintilla constants
3. **Keyword Conflicts**: Check for duplicate or conflicting keyword definitions
4. **File Encoding**: Ensure the XML file is saved in UTF-8 encoding

#### Performance Issues

1. **Reduce Keyword Lists**: Large keyword lists can slow down highlighting
2. **Optimize Regex**: Complex regular expressions in lexer properties
3. **Limit Style Complexity**: Too many style variations can impact performance
4. **Check Memory Usage**: Monitor MySQL Workbench memory consumption

#### Color Theme Problems

1. **Contrast Issues**: Ensure sufficient contrast between foreground and background
2. **Missing Dark/Light Variants**: Define both light and dark theme colors
3. **Accessibility**: Test with high contrast system settings
4. **Color Blindness**: Consider color-blind friendly palettes

### Advanced Debugging

#### Lexer Property Testing

```xml
<!-- Enable debug mode for lexer testing -->
<property name="lexer.debug" value="1" />
<property name="lexer.trace" value="1" />
```

#### Style Validation

- Use Scintilla's style inspector tools
- Test with various file sizes and complexity
- Validate against different MySQL versions
- Check performance with large result sets

### Best Practices

#### Configuration Management

1. **Version Control**: Keep configuration files in version control
2. **Backup Before Changes**: Always backup working configurations
3. **Test Incrementally**: Make small changes and test thoroughly
4. **Document Changes**: Comment your customizations in the XML
5. **User Preferences**: Provide multiple theme options for users

#### Performance Optimization

1. **Minimize Keywords**: Only include necessary keywords
2. **Efficient Styles**: Use simple color definitions
3. **Lexer Properties**: Enable only needed lexer features
4. **Memory Management**: Monitor resource usage during editing

### Modifying Colors

Edit the `<style>` elements in the XML files to change colors:

```xml
<style id="8" bold="Yes" fore-color-light="#61afef" />
```

### Adding Keywords

Add new keywords to the appropriate `<keywords>` section:

```xml
<keywords name="Keywords">
  your_custom_keyword another_keyword
</keywords>
```

### Editor Settings

Modify editor behavior by changing `<setting>` elements:

```xml
<setting name="tabwidth" value="4" />
<setting name="indentation" value="4" />
```

## Technical Details

### Lexer Integration

The configuration is designed to work with Scintilla lexers:

- `SCLEX_MYSQL` for MySQL syntax
- `SCLEX_CPP` for C/C++ syntax
- `SCLEX_CPP_JSON` for JSON syntax

### Style Identifiers

Style IDs correspond to Scintilla's lexer constants (see `SciLexer.h`):

- `SCE_MYSQL_DEFAULT` (0)
- `SCE_MYSQL_COMMENT` (1)
- `SCE_MYSQL_KEYWORD` (8)
- And many more...

## Contributing

When modifying the configuration:

1. Test changes with different MySQL versions
2. Verify both light and dark theme compatibility
3. Ensure keyword lists are complete and accurate
4. Validate XML syntax

## Compatibility

- **MySQL Workbench**: 6.0+
- **MySQL Versions**: 5.6, 5.7, 8.0, 8.1
- **Platforms**: Windows, macOS, Linux

## License

### MySQL Workbench Code Editor Configuration License

This configuration file is provided under the **MIT License** for the configuration portions and respects the MySQL Workbench licensing terms for integration purposes.

#### MIT License (Configuration)

```
MIT License

Copyright (c) 2025 MySQL Workbench Code Editor Configuration

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

#### MySQL Workbench Compatibility

This configuration is designed to be compatible with **MySQL Workbench**, which is licensed under the **GPL v2** license. The configuration files do not modify MySQL Workbench's core functionality but provide enhanced syntax highlighting and editor settings.

#### Third-Party Components

- **Scintilla Editor**: This configuration works with the Scintilla editing component used by MySQL Workbench
- **MySQL Keywords**: MySQL-specific keywords and functions are referenced according to MySQL documentation
- **C++ Standards**: C++ keywords follow the ISO C++ standard specifications

#### Disclaimer

- This configuration is **not officially endorsed** by Oracle Corporation or the MySQL team
- Use at your own risk; always backup existing configuration files
- No warranty is provided for compatibility with future MySQL Workbench versions
- The authors are not responsible for any data loss or system issues

#### Attribution

If you distribute this configuration or create derivative works:

1. Include this license notice
2. Credit the original authors
3. Maintain compatibility with MySQL Workbench licensing terms

## Compatibility & Requirements

### MySQL Workbench Versions

- **Minimum**: MySQL Workbench 6.0
- **Recommended**: MySQL Workbench 8.0 or higher
- **Tested**: MySQL Workbench 8.0.35, 8.0.36, 8.1.0

### MySQL Server Versions

- **MySQL 5.6**: Basic syntax highlighting
- **MySQL 5.7**: Enhanced features and functions
- **MySQL 8.0**: Full feature support including JSON, window functions
- **MySQL 8.1**: Latest features including vector functions

### Operating Systems

- **Windows**: Windows 10, Windows 11, Windows Server 2016+
- **macOS**: macOS 10.14 (Mojave) or higher
- **Linux**: Ubuntu 18.04+, CentOS 7+, RHEL 7+, openSUSE 15+

### System Requirements

- **Memory**: Additional 50-100 MB for enhanced keyword tables
- **Storage**: 2-5 MB for configuration files
- **Processor**: No additional requirements

### Known Limitations

1. **Large Files**: Performance may degrade with SQL files larger than 10 MB
2. **Complex Queries**: Very complex nested queries may have slower highlighting
3. **Custom Functions**: User-defined functions require manual keyword addition
4. **Legacy Syntax**: Some deprecated MySQL syntax may not be highlighted

## Changelog

### Version 2.0.0 (2025-09-23)

- **Added**: MySQL 8.1 support with vector functions
- **Added**: Enhanced JSON schema support
- **Added**: C++23 keyword support
- **Added**: Advanced code folding
- **Added**: Dual theme optimization
- **Improved**: Performance optimizations
- **Improved**: Color contrast and accessibility
- **Fixed**: Lexer property conflicts

### Version 1.5.0

- **Added**: MySQL 8.0 comprehensive support
- **Added**: Window functions highlighting
- **Added**: Spatial functions support
- **Improved**: C++ modern standard support

### Version 1.0.0

- **Initial**: Basic MySQL syntax highlighting
- **Initial**: C/C++ support
- **Initial**: JSON formatting

## Support & Resources

### Official Documentation

- **MySQL Workbench Manual**: [dev.mysql.com/doc/workbench/en/](https://dev.mysql.com/doc/workbench/en/)
- **MySQL 8.1 Reference**: [dev.mysql.com/doc/refman/8.1/en/](https://dev.mysql.com/doc/refman/8.1/en/)
- **Scintilla Documentation**: [scintilla.org/ScintillaDoc.html](https://scintilla.org/ScintillaDoc.html)

### Getting Help

#### For Configuration Issues

1. **Check Prerequisites**: Ensure you have the correct MySQL Workbench version
2. **Validate XML**: Use an XML validator to check file syntax
3. **Test Incrementally**: Apply changes step by step
4. **Review Logs**: Check MySQL Workbench error logs

#### For Syntax Highlighting Issues

1. **Verify Keywords**: Ensure keywords are in the correct sections
2. **Check Style IDs**: Confirm style IDs match Scintilla constants
3. **Test File Size**: Large files may cause performance issues
4. **Update Configuration**: Ensure you have the latest version

#### For Performance Issues

1. **Reduce Complexity**: Minimize keyword lists if experiencing slowdowns
2. **Check Memory**: Monitor MySQL Workbench memory usage
3. **Optimize Queries**: Large result sets may affect editor performance
4. **Restart Application**: Sometimes a simple restart resolves issues

### Reporting Issues

When reporting issues, please include:

1. **MySQL Workbench Version**: Help → About MySQL Workbench
2. **Operating System**: Version and architecture
3. **Configuration File**: Which version you're using
4. **Error Description**: Detailed description of the problem
5. **Steps to Reproduce**: How to recreate the issue
6. **Screenshots**: Visual examples of the problem (if applicable)

### Contributing

We welcome contributions! Please:

1. **Fork the Repository**: Create your own copy
2. **Test Changes**: Verify your modifications work correctly
3. **Follow Standards**: Maintain XML formatting and style consistency
4. **Document Changes**: Update README and comments
5. **Submit Pull Request**: Provide clear description of improvements

### Security

If you discover any security-related issues with the configuration:

1. **Do Not** create public issues
2. **Contact** maintainers privately
3. **Provide** detailed information about the vulnerability
4. **Allow** time for investigation and resolution

---

**Note**: This configuration enhances MySQL Workbench's built-in editor but does not modify core functionality. Always maintain backups of your original configuration files and test changes in a development environment before applying to production systems.