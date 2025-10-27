# C++ Input & Validation Library

A comprehensive C++ library providing robust string, date, and input validation utilities for console applications.

## Classes Overview

### clsString

**String manipulation and analysis utilities:**

- **Length & Counting**: `Length()`, `CountWords()`, `CountVowels()`
- **Case Manipulation**: `UpperFirstLetterOfEachWord()`, `InvertAllLettersCase()`
- **Text Analysis**: `CountLetters()`, `CountSpecificLetter()`, `IsVowel()`
- **String Operations**: `Split()`, `Trim()`, `ReverseWordsInString()`, `ReplaceWord()`
- **Text Cleaning**: `RemovePunctuations()`

### clsDate

**Complete date handling with calendar operations:**
- **Multiple Constructors**: From string, components, or day-of-year
- **Date Validation**: `IsValidDate()`, range checking
- **Calendar Display**: `PrintMonthCalendar()`, `PrintYearCalendar()`
- **Date Arithmetic**: Add/subtract days, weeks, months, years
- **Business Logic**: `CalculateBusinessDays()`, `CalculateVacationReturnDate()`
- **Date Comparisons**: `CompareDates()`, `GetDifferenceInDays()`

### clsInputValidate

**Input validation and sanitization:**
- **Range Validation**: `IsNumberBetween()` for all numeric types
- **Date Validation**: `IsDateBetween()`, `IsValideDate()`
- **Safe Input**: `ReadIntNumber()`, `ReadDblNumber()` with error handling
- **Range-bound Input**: `ReadIntNumberBetween()`, `ReadDblNumberBetween()`



## Features

- Dual Interface: Both static and instance methods

- Property Syntax: Clean getter/setter using __declspec(property)

- Error Handling: Robust input validation

- Real-world Utilities: Business day calculations, vacation planning

- Cross-platform: Standard C++ with minimal dependencies

## License

Open source - feel free to use in your projects!

## Quick Start

```cpp
#include "clsString.h"
#include "clsDate.h"
#include "clsInputValidate.h"

// String operations
clsString str("hello world");
str.UpperFirstLetterOfEachWord();
cout << str.GetValue(); // "Hello World"

// Date operations
clsDate today;
clsDate birthday(15, 8, 1990);
short ageInDays = clsDate::CalculateMyAgeInDays(birthday);

// Input validation
int age = clsInputValidate::ReadIntNumberBetween(1, 120, "Enter valid age: ");