# @rhynel/camote

A comprehensive TypeScript utility library featuring advanced string and number formatting functions.

> Last updated: 2024-12-11T03:32:49+08:00

## Installation

```bash
npm install @rhynel/camote
```

## Usage

### Number Formatting

```typescript
import {
  humanReadableNumber,
  formatWithCommas,
  formatPercentage,
  formatOrdinal,
  formatFileSize,
  formatCurrency,
  formatDecimals
} from '@rhynel/camote';

// Human readable numbers
console.log(humanReadableNumber(1234));     // "1.2K"
console.log(humanReadableNumber(1500000));  // "1.5M"
console.log(humanReadableNumber(1000000000)); // "1.0B"

// Numbers with commas
console.log(formatWithCommas(1234567));  // "1,234,567"

// Percentages
console.log(formatPercentage(0.1234));    // "12%"
console.log(formatPercentage(0.1234, 1)); // "12.3%"

// Ordinal numbers
console.log(formatOrdinal(1));  // "1st"
console.log(formatOrdinal(2));  // "2nd"
console.log(formatOrdinal(3));  // "3rd"
console.log(formatOrdinal(4));  // "4th"

// File sizes
console.log(formatFileSize(1024));        // "1.00 KB"
console.log(formatFileSize(1234567));     // "1.18 MB"
console.log(formatFileSize(1024 * 1024)); // "1.00 MB"

// Currency
console.log(formatCurrency(1234.56));                    // "$1,234.56"
console.log(formatCurrency(1234.56, 'EUR', 'de-DE'));   // "1.234,56 €"

// Decimal places with rounding
console.log(formatDecimals(1.2345, 2));           // "1.23"
console.log(formatDecimals(1.2345, 2, 'ceil'));   // "1.24"
console.log(formatDecimals(1.2345, 2, 'floor'));  // "1.23"
```

### String Formatting

```typescript
import {
  capitalize,
  truncate,
  toCamelCase,
  toKebabCase,
  toSnakeCase,
  slugify,
  wordCount,
  pad,
  format,
  reverse,
  clean
} from '@rhynel/camote';

// Capitalize strings
console.log(capitalize("hello"));  // "Hello"

// Truncate strings
console.log(truncate("Hello World", 8));  // "Hello..."
console.log(truncate("Hello World", 8, '!'));  // "Hello W!"

// Case conversions
console.log(toCamelCase("hello-world"));   // "helloWorld"
console.log(toKebabCase("helloWorld"));    // "hello-world"
console.log(toSnakeCase("Hello World"));   // "hello_world"

// URL-friendly slugs
console.log(slugify("Hello World!"));      // "hello-world"
console.log(slugify("What's Up?"));        // "whats-up"

// Word counting
console.log(wordCount("Hello world"));     // 2

// String padding
console.log(pad("hello", 8));              // "hello   "
console.log(pad("hello", 8, "*", "start")); // "***hello"
console.log(pad("hello", 8, "*", "both"));  // "*hello**"

// Template formatting
console.log(format("Hello {name}!", { name: "World" }));  // "Hello World!"
console.log(format("{greeting} {name}!", { 
  greeting: "Hi",
  name: "User"
}));  // "Hi User!"

// String reversal
console.log(reverse("hello"));  // "olleh"

// Clean whitespace
console.log(clean("  hello   world  "));  // "hello world"
```

## Features

- Comprehensive number formatting utilities:
  - Human-readable numbers (K, M, B suffixes)
  - Comma-separated numbers
  - Percentage formatting
  - Ordinal numbers (1st, 2nd, 3rd)
  - File size formatting (KB, MB, GB)
  - Currency formatting with locale support
  - Decimal place formatting with rounding options

- Advanced string manipulation functions:
  - Case conversions (camelCase, kebab-case, snake_case)
  - URL-friendly slug generation
  - Word counting
  - String padding with flexible positioning
  - Template string formatting
  - String reversal
  - Whitespace cleaning

- Development features:
  - Written in TypeScript with full type definitions
  - Comprehensive test suite with 58+ unit tests
  - Zero dependencies
  - Modern ES2018+ compatible
  - Well-documented with examples

## License

MIT
