# Java Syntax Highlighting Attributes Reference

Based on analysis of **Trash Panda Theme Moonlight** and **One Dark Islands** plugins.

## Core Java Attributes (Used for Java highlighting)

| Attribute Name | Color (Hex) | Description |
|---------------|-------------|-------------|
| `DEFAULT_KEYWORD` | #A07CF1 | Keywords (public, class, void, etc.) |
| `DEFAULT_STRING` | #dcc37c | String literals |
| `DEFAULT_NUMBER` | #E8886D | Numeric literals |
| `DEFAULT_CLASS_NAME` | #8ec475 | Class names |
| `DEFAULT_FUNCTION_DECLARATION` | #8ec475 | Method/function declarations |
| `DEFAULT_FUNCTION_CALL` | #8ec475 | Method/function calls |
| `DEFAULT_LINE_COMMENT` | #7f8688 | Single-line comments |
| `DEFAULT_BLOCK_COMMENT` | #7f8688 | Multi-line comments |
| `DEFAULT_LOCAL_VARIABLE` | #a9afb0 | Local variables |
| `DEFAULT_GLOBAL_VARIABLE` | (inherited) | Global variables |
| `DEFAULT_CONSTANT` | #DC6096 | Constants |
| `DEFAULT_INSTANCE_METHOD` | #8ec475 | Instance methods |
| `DEFAULT_STATIC_METHOD` | #8ec475 | Static methods |
| `DEFAULT_IDENTIFIER` | (default) | Generic identifiers |
| `DEFAULT_PARAMETER` | (inherited) | Method parameters |
| `DEFAULT_OPERATOR` | (default) | Operators |
| `DEFAULT_BRACES` | (default) | Braces and brackets |
| `DEFAULT_DOC_COMMENT` | #7f8688 | Documentation comments |
| `DEFAULT_DOC_COMMENT_TAG` | (from theme) | Doc tags (@param, @return) |
| `DEFAULT_DOC_COMMENT_TAG_VALUE` | (from theme) | Doc tag values |

## Annotation Attributes

| Attribute Name | Color (Hex) | Description |
|---------------|-------------|-------------|
| `ANNOTATION_NAME_ATTRIBUTES` | (theme specific) | Annotation names (@Override) |
| `ANNOTATION_ATTRIBUTE_NAME_ATTRIBUTES` | (theme specific) | Annotation attributes |

## Java-Specific Alternative Names

Some themes also support these alternative names with underscores:

| Alternative Name | Same As | Notes |
|-----------------|---------|-------|
| `JAVA_KEYWORD` | `DEFAULT_KEYWORD` | Common alternative naming |
| `JAVA_CLASS` | `DEFAULT_CLASS_NAME` | Java-specific class name |
| `JAVA_INTERFACE` | ❌ **NOT WORKING** | Use `DEFAULT_INTERFACE_NAME` instead |
| `JAVA_ENUM` | `DEFAULT_CLASS_NAME` | Enum names |
| `JAVA_ABSTRACT_CLASS` | `DEFAULT_CLASS_NAME` | Abstract class names |
| `JAVA_STRING` | `DEFAULT_STRING` | Java strings |
| `JAVA_VALID_STRING_ESCAPE` | `DEFAULT_STRING` | Valid escape sequences |

### Interface Name Fix (Important)

**Problem:** `JAVA_INTERFACE` does not work in IntelliJ IDEA syntax highlighting.

**Solution:** Use `DEFAULT_INTERFACE_NAME` instead. This is confirmed by analyzing Trash Panda Theme (Moonlight) which uses `DEFAULT_INTERFACE_NAME` with color `#50cae5` and works correctly.

**Action Required:** In all theme XML files, replace or add `DEFAULT_INTERFACE_NAME` for interface highlighting:
```xml
<option name="DEFAULT_INTERFACE_NAME">
    <value>
        <option name="FOREGROUND" value="#8be9fd" />
        <option name="FONT_TYPE" value="2" />
    </value>
</option>
```

## Color Palette from Trash Panda Moonlight

```json
{
  "keyword": "#A07CF1",
  "string": "#dcc37c",
  "number": "#E8886D",
  "class": "#8ec475",
  "function": "#8ec475",
  "comment": "#7f8688",
  "variable": "#a9afb0",
  "constant": "#DC6096"
}
```

## From Dracula-darker-contrast-new-color Source

The VS Code source theme uses these colors for reference:

| Token Type | Color (Hex) |
|------------|-------------|
| `keyword` / `punctuation.definition.keyword` | #ff42b3 |
| `string` | #eac394 |
| `number` | #91b4d5 |
| `entity.name.function` | #40dc99 |
| `entity.name.type` / `entity.name.class` | #17b5ff |
| `comment` | #6272a4 |
| `variable` | #ced9f7 |
| `constant` | #91b4d5 |

## One Dark Islands Format

One Dark Islands uses the standard format with these Java attributes:

```xml
<option name="JAVA_KEYWORD">
  <value>
    <option name="FOREGROUND" value="#c678dd"/>
  </value>
</option>
<option name="JAVA_STRING">
  <value>
    <option name="FOREGROUND" value="#98c379"/>
  </value>
</option>
<option name="JAVA_VALID_STRING_ESCAPE">
  <value>
    <option name="FOREGROUND" value="#98c379"/>
  </value>
</option>
```

## JS/TS Language Attributes

| Attribute Name | Color (Hex) | Description |
|---------------|-------------|-------------|
| `JS.KEYWORD` | (from theme) | JavaScript keywords |
| `JS.GLOBAL_FUNCTION` | (from theme) | Global functions |
| `JS.GLOBAL_VARIABLE` | (from theme) | Global variables |
| `JS.INSTANCE_MEMBER_FUNCTION` | (from theme) | Instance methods |
| `JS.INSTANCE_MEMBER_VARIABLE` | (from theme) | Instance fields |
| `JS.LOCAL_VARIABLE` | (from theme) | Local variables |
| `JS.MODULE_NAME` | (from theme) | Module names |
| `JS.REGEXP` | (from theme) | Regular expressions |
| `JS.PARAMETER` | (from theme) | Function parameters |
| `JS.PROPERTY` | (from theme) | Object properties |
| `JS.OBJECT_PROPERTY` | (from theme) | Object property access |
| `JS.STATIC_MEMBER_FUNCTION` | (from theme) | Static methods |
| `JS.STATIC_MEMBER_VARIABLE` | (from theme) | Static fields |

## Python Language Attributes

| Attribute Name | Color (Hex) | Description |
|---------------|-------------|-------------|
| `PY.KEYWORD` | (from theme) | Python keywords |
| `PY.BUILTIN_NAME` | (from theme) | Built-in functions |
| `PY.DECORATOR` | (from theme) | Decorators |
| `PY.CLASS_DEFINITION` | (from theme) | Class definitions |
| `PY.FUNC_DEFINITION` | (from theme) | Function definitions |
| `PY.PREDEFINED_DEFINITION` | (from theme) | Predefined definitions |
| `PY.PREDEFINED_USAGE` | (from theme) | Predefined usage |
| `PY.SELF_PARAMETER` | (from theme) | Self parameter |
| `PY.STRING.B` | (from theme) | Byte strings |
| `PY.ANNOTATION` | (from theme) | Type annotations |
| `PY.TYPE_PARAMETER` | (from theme) | Type parameters |
| `PY.LOCAL_VARIABLE` | (from theme) | Local variables |

## JSON/YAML Attributes

| Attribute Name | Description |
|---------------|-------------|
| `JSON.KEYWORD` | JSON keywords (true, false, null) |
| `JSON.PROPERTY_KEY` | JSON property keys |
| `JSON.STRING_LITERAL` | JSON string values |
| `JSON.NUMBER_LITERAL` | JSON numbers |
| `YAML_SCALAR_KEY` | YAML scalar keys |
| `YAML_SCALAR_VALUE` | YAML scalar values |
| `YAML_TEXT` | YAML text |

## CSS/HTML Attributes

| Attribute Name | Description |
|---------------|-------------|
| `CSS.ATKEYWORD` | CSS at-keywords (@media, @import) |
| `CSS.CLASS_NAME` | CSS class selectors |
| `CSS.FUNCTION` | CSS functions |
| `CSS.ID_SELECTOR` | CSS ID selectors |
| `CSS.IMPORTANT` | CSS !important |
| `CSS.NUMBER` | CSS numbers |
| `CSS.PROPERTY_NAME` | CSS property names |
| `CSS.PROPERTY_VALUE` | CSS property values |
| `CSS.PSEUDO` | CSS pseudo-selectors |
| `CSS.TAG_NAME` | CSS tag selectors |
| `CSS.UNIT` | CSS units |
| `CSS.URL` | CSS URLs |
| `HTML_TAG` | HTML tag names |
| `HTML_ATTRIBUTE_NAME` | HTML attribute names |
| `HTML_ATTRIBUTE_VALUE` | HTML attribute values |

## Regex/RegExp Attributes

| Attribute Name | Description |
|---------------|-------------|
| `REGEXP.BRACES` | Regex braces |
| `REGEXP.BRACKETS` | Regex brackets |
| `REGEXP.CHAR_CLASS` | Character classes |
| `REGEXP.ESC_CHARACTER` | Escape characters |
| `REGEXP.META` | Regex meta characters |
| `REGEXP.PARENTHS` | Regex parentheses |
| `REGEXP.QUOTE_CHARACTER` | Quote characters |

## SQL Attributes

| Attribute Name | Description |
|---------------|-------------|
| `SQL_KEYWORD` | SQL keywords |
| `SQL_TABLE` | Table names |
| `SQL_COLUMN` | Column names |
| `SQL_FUNCTION` | SQL functions |

## Go/Rust/Kotlin Attributes

| Language | Attribute Names |
|----------|----------------|
| Go | `GO_BUILTIN_FUNCTION_CALL`, `GO_EXPORTED_FUNCTION`, `GO_TYPE_REFERENCE`, `GO_BUILTIN_CONSTANT`, `GO_BUILTIN_VARIABLE` |
| Rust | `RUST_MACRO`, `RUST_STRUCT`, `RUST_TRAIT`, `RUST_TYPE_PARAMETER` |
| Kotlin | `KOTLIN_CLASS`, `KOTLIN_INTERFACE`, `KOTLIN_FUNCTION_LITERAL_BRACES_AND_ARROW`, `KOTLIN_LABEL`, `KOTLIN_OBJECT`, `KOTLIN_PROPERTY` |

## Markdown Attributes

| Attribute Name | Description |
|---------------|-------------|
| `MARKDOWN_HEADER` | Markdown headers |
| `MARKDOWN_BOLD` | Bold text |
| `MARKDOWN_ITALIC` | Italic text |
| `MARKDOWN_CODE_FENCE` | Code fences |
| `MARKDOWN_CODE_BLOCK` | Code blocks |
| `MARKDOWN_INLINE_CODE` | Inline code |
| `MARKDOWN_LINK_TEXT` | Link text |
| `MARKDOWN_LINK_DESTINATION` | Link URLs |
| `MARKDOWN_QUOTE` | Block quotes |

## Console/VCS Colors

| Attribute Name | Description |
|---------------|-------------|
| `CONSOLE_RED_OUTPUT` | Red console output |
| `CONSOLE_GREEN_OUTPUT` | Green console output |
| `CONSOLE_YELLOW_OUTPUT` | Yellow console output |
| `CONSOLE_BLUE_OUTPUT` | Blue console output |
| `CONSOLE_CYAN_OUTPUT` | Cyan console output |
| `CONSOLE_MAGENTA_OUTPUT` | Magenta console output |
| `CONSOLE_WHITE_OUTPUT` | White console output |
| `CONSOLE_GRAY_OUTPUT` | Gray console output |
| `CONSOLE_BLACK_OUTPUT` | Black console output |
| `ADDED_LINES_COLOR` | VCS added lines |
| `DELETED_LINES_COLOR` | VCS deleted lines |
| `MODIFIED_LINES_COLOR` | VCS modified lines |

## Error/Warning Attributes

| Attribute Name | Description |
|---------------|-------------|
| `ERROR` | Error highlighting |
| `WARNING` | Warning highlighting |
| `INFO` | Info highlighting |
| `WEAK_WARNING` | Weak warning |
| `NOT_USED_ELEMENT_ATTRIBUTES` | Unused code |
| `MARKED_FOR_REMOVAL_ATTRIBUTES` | Deprecated code |
| `DEPRECATED_ATTRIBUTES` | Deprecated usage |

## Editor UI Attributes

| Attribute Name | Description |
|---------------|-------------|
| `CARET_COLOR` | Caret/cursor color |
| `CARET_ROW_COLOR` | Current line highlight |
| `LINE_NUMBERS_COLOR` | Line numbers |
| `SELECTION_BACKGROUND` | Selection background |
| `SELECTION_FOREGROUND` | Selection text color |
| `INDENT_GUIDE` | Indent guides |
| `RIGHT_MARGIN_COLOR` | Right margin |
| `GUTTER_BACKGROUND` | Gutter background |
| `CONSOLE_BACKGROUND_KEY` | Console background |

## Important Notes

1. **For Java syntax highlighting**, use `DEFAULT_*` attributes as they are inherited by Java language lexer.

2. **Some themes use alternative naming** with underscores (JAVA_KEYWORD) vs dots (JS.KEYWORD) - both can work depending on the theme engine version.

3. **Parent scheme inheritance** - When using `parent_scheme="Darcula"`, many attributes are inherited from Darcula and only need to be overridden if you want different colors.

4. **Islands UI mode** - When using Islands UI, additional UI-specific attributes like `Islands`, `Island`, and `Component.arc` need to be configured for rounded corners.
