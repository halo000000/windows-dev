# Page 1

Sure! Here’s a list of useful regular expressions (regex) with their code and explanations. These are practical regex patterns that you can use in many scenarios, from validating user input to extracting data.

***

#### **1. Match an Email Address**

Regex to match a basic email address:

```regex
^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$
```

* **Explanation**:
  * `^[a-zA-Z0-9._%+-]+`: Matches the username part of the email.
  * `@`: Matches the "@" symbol.
  * `[a-zA-Z0-9.-]+`: Matches the domain name part.
  * `\.[a-zA-Z]{2,}$`: Matches the top-level domain (e.g., `.com`, `.org`).

#### **2. Match a URL**

Regex to match a simple URL:

```regex
^(https?|ftp):\/\/[^\s/$.?#].[^\s]*$
```

* **Explanation**:
  * `^(https?|ftp)`: Matches the URL protocol (`http`, `https`, `ftp`).
  * `:\/\/`: Matches the "://" after the protocol.
  * `[^\s/$.?#].[^\s]*$`: Matches the rest of the URL.

#### **3. Match a Phone Number (US format)**

Regex to match a U.S. phone number (e.g., `(123) 456-7890`):

```regex
^\(\d{3}\)\s?\d{3}-\d{4}$
```

* **Explanation**:
  * `^\(\d{3}\)`: Matches the area code in parentheses.
  * `\s?`: Matches an optional space after the closing parenthesis.
  * `\d{3}-\d{4}$`: Matches the phone number in the form `XXX-XXXX`.

#### **4. Match a Date (DD/MM/YYYY format)**

Regex to match a date in `DD/MM/YYYY` format:

```regex
^(0[1-9]|[12][0-9]|3[01])\/(0[1-9]|1[0-2])\/\d{4}$
```

* **Explanation**:
  * `^(0[1-9]|[12][0-9]|3[01])`: Matches the day part, between `01` and `31`.
  * `\/`: Matches the `/` separator.
  * `(0[1-9]|1[0-2])`: Matches the month part, between `01` and `12`.
  * `\/\d{4}$`: Matches the year part, exactly four digits.

#### **5. Match a Hexadecimal Color Code**

Regex to match a 6-character hexadecimal color code:

```regex
^#([A-Fa-f0-9]{6})$
```

* **Explanation**:
  * `^#`: Matches the `#` symbol at the beginning.
  * `([A-Fa-f0-9]{6})$`: Matches exactly six characters that are hexadecimal digits (0-9, a-f, A-F).

#### **6. Match a Strong Password**

Regex to match a strong password (at least 8 characters, with at least one lowercase, one uppercase, one digit, and one special character):

```regex
^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[!@#$%^&*()_+])[A-Za-z\d!@#$%^&*()_+]{8,}$
```

* **Explanation**:
  * `(?=.*[a-z])`: At least one lowercase letter.
  * `(?=.*[A-Z])`: At least one uppercase letter.
  * `(?=.*\d)`: At least one digit.
  * `(?=.*[!@#$%^&*()_+])`: At least one special character.
  * `[A-Za-z\d!@#$%^&*()_+]{8,}$`: Ensures the password is at least 8 characters long.

#### **7. Match a Positive Integer**

Regex to match a positive integer (no leading zeros):

```regex
^[1-9][0-9]*$
```

* **Explanation**:
  * `^[1-9]`: Matches the first digit, which cannot be `0`.
  * `[0-9]*$`: Matches any subsequent digits.

#### **8. Match a Decimal Number**

Regex to match a decimal number (supports both integer and floating point):

```regex
^\d+(\.\d+)?$
```

* **Explanation**:
  * `^\d+`: Matches the integer part (one or more digits).
  * `(\.\d+)?$`: Optionally matches the decimal point followed by one or more digits.

#### **9. Match a Social Security Number (SSN) (US)**

Regex to match a U.S. Social Security Number (e.g., `123-45-6789`):

```regex
^\d{3}-\d{2}-\d{4}$
```

* **Explanation**:
  * `^\d{3}`: Matches the first three digits.
  * `-\d{2}-`: Matches the second part with two digits.
  * `\d{4}$`: Matches the last four digits.

#### **10. Match an IP Address (IPv4)**

Regex to match an IPv4 address:

```regex
^((25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)$
```

* **Explanation**:
  * `((25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}`: Matches the first three octets of the address, each in the range `0-255`.
  * `(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)`: Matches the final octet.

#### **11. Match a Time (HH:MM format)**

Regex to match a time in `HH:MM` format (24-hour clock):

```regex
^([01]?[0-9]|2[0-3]):([0-5][0-9])$
```

* **Explanation**:
  * `([01]?[0-9]|2[0-3])`: Matches the hour part, which can range from `00` to `23`.
  * `([0-5][0-9])`: Matches the minute part, which can range from `00` to `59`.

#### **12. Match a Credit Card Number**

Regex to match a standard credit card number (16 digits with optional spaces or hyphens):

```regex
^(\d{4}[-\s]?)\d{4}[-\s]?\d{4}[-\s]?\d{4}$
```

* **Explanation**:
  * `^(\d{4}[-\s]?)`: Matches the first 4 digits followed by an optional space or hyphen.
  * `\d{4}[-\s]?\d{4}[-\s]?\d{4}$`: Matches the subsequent 3 sets of 4 digits, each optionally followed by a space or hyphen.

#### **13. Match a Time Duration (HH:MM:SS format)**

Regex to match a time duration in the `HH:MM:SS` format:

```regex
^([01]?[0-9]|2[0-3]):([0-5][0-9]):([0-5][0-9])$
```

* **Explanation**:
  * `([01]?[0-9]|2[0-3])`: Matches the hours part, ranging from `00` to `23`.
  * `([0-5][0-9])`: Matches the minutes and seconds part, both ranging from `00` to `59`.

#### **14. Match a Zip Code (US)**

Regex to match a U.S. ZIP code (either `12345` or `12345-6789`):

```regex
^\d{5}(-\d{4})?$
```

* **Explanation**:
  * `^\d{5}`: Matches exactly five digits.
  * `(-\d{4})?`: Optionally matches the ZIP+4 format, which consists of a hyphen followed by four digits.

#### **15. Match HTML Tag**

Regex to match an HTML tag:

```regex
<([a-zA-Z][a-zA-Z0-9]*)\b[^>]*>(.*?)<\/\1>
```

* **Explanation**:
  * `<([a-zA-Z][a-zA-Z0-9]*)`: Matches the opening HTML tag.
  * `\b[^>]*>`: Matches attributes within the tag.
  * `(.*?)<\/\1>`: Matches the content inside the tag and the corresponding closing tag.

***

#### **16. Match Whitespace**

Regex to match any whitespace (spaces, tabs, newlines):

```regex
\s+
```

* **Explanation**:
  * `\s+`: Matches one or more whitespace characters (spaces, tabs, or line breaks).

#### **17. Match Non-Alphanumeric Characters**

Regex to match non-alphanumeric characters:

```regex
[^a-zA-Z0-9]
```

* **Explanation**:
  * `[^a-zA-Z0-9]`: Matches any character that is **not** a letter or digit.

***



Absolutely! Here are additional useful regular expressions for various scenarios.

***

#### **18. Match a Single Word**

Regex to match a single word (no spaces or special characters):

```regex
^\w+$
```

* **Explanation**:
  * `^\w+$`: Matches one or more word characters (letters, digits, and underscores). The `^` and `$` anchors ensure the match is for the entire string.

#### **19. Match a Non-Empty String**

Regex to match any non-empty string:

```regex
^.+$
```

* **Explanation**:
  * `^.+$`: Matches one or more characters (except newlines) in a string. The `^` and `$` anchors ensure the match is for the entire string.

#### **20. Match Only Digits**

Regex to match a string that contains only digits (integer numbers):

```regex
^\d+$
```

* **Explanation**:
  * `^\d+$`: Matches one or more digits from start to end.

#### **21. Match a Floating Point Number**

Regex to match a floating-point number (optional leading sign, digits, optional decimal point):

```regex
^[+-]?(\d+(\.\d*)?|\.\d+)$
```

* **Explanation**:
  * `^[+-]?`: Matches an optional sign (`+` or `-`).
  * `(\d+(\.\d*)?|\.\d+)`: Matches either a whole number with an optional decimal part or a decimal number starting with a dot.

#### **22. Match a Date (MM/DD/YYYY format)**

Regex to match a date in `MM/DD/YYYY` format:

```regex
^(0[1-9]|1[0-2])\/(0[1-9]|[12][0-9]|3[01])\/\d{4}$
```

* **Explanation**:
  * `(0[1-9]|1[0-2])`: Matches the month part, between `01` and `12`.
  * `(0[1-9]|[12][0-9]|3[01])`: Matches the day part, between `01` and `31`.
  * `\d{4}$`: Matches the year part (exactly four digits).

#### **23. Match a Valid IPv6 Address**

Regex to match an IPv6 address:

```regex
^([0-9a-fA-F]{1,4}:){7}([0-9a-fA-F]{1,4})$
```

* **Explanation**:
  * `([0-9a-fA-F]{1,4}:){7}`: Matches 7 blocks of 1 to 4 hexadecimal digits followed by a colon.
  * `([0-9a-fA-F]{1,4})`: Matches the final block of 1 to 4 hexadecimal digits.

#### **24. Match a Word with Hyphens (e.g., "hello-world")**

Regex to match a word that can contain hyphens:

```regex
^[a-zA-Z0-9-]+$
```

* **Explanation**:
  * `^[a-zA-Z0-9-]+$`: Matches any combination of letters, digits, and hyphens from start to end.

#### **25. Match a Time in 12-Hour Format (with AM/PM)**

Regex to match a time in `hh:mm AM/PM` format:

```regex
^(0[1-9]|1[0-2]):([0-5][0-9]) (AM|PM)$
```

* **Explanation**:
  * `(0[1-9]|1[0-2])`: Matches the hour part (01-12).
  * `([0-5][0-9])`: Matches the minutes part (00-59).
  * `(AM|PM)$`: Matches either "AM" or "PM".

#### **26. Match a Word that Contains Only Letters**

Regex to match a string containing only alphabetic characters:

```regex
^[a-zA-Z]+$
```

* **Explanation**:
  * `^[a-zA-Z]+$`: Matches one or more letters from start to end.

#### **27. Match a String of Fixed Length (n characters)**

Regex to match a string with exactly `n` characters (replace `n` with the desired length):

```regex
^.{n}$
```

* **Explanation**:
  * `^.{n}$`: Matches exactly `n` characters (of any type). Replace `n` with the desired length.

#### **28. Match Any Character Except Line Breaks**

Regex to match any character except line breaks:

```regex
[^\r\n]+
```

* **Explanation**:
  * `[^\r\n]+`: Matches any character except a carriage return or newline.

#### **29. Match Multiple Spaces**

Regex to match one or more consecutive spaces:

```regex
\s+
```

* **Explanation**:
  * `\s+`: Matches one or more whitespace characters (spaces, tabs, newlines).

#### **30. Match Tags with Attributes (HTML-style)**

Regex to match HTML tags with attributes:

```regex
<([a-zA-Z][a-zA-Z0-9]*)\b[^>]*>
```

* **Explanation**:
  * `<([a-zA-Z][a-zA-Z0-9]*)`: Matches the tag name.
  * `\b[^>]*>`: Matches any attributes and the closing tag bracket.

#### **31. Match an HTML Comment**

Regex to match an HTML comment:

```regex
<!--[\s\S]*?-->
```

* **Explanation**:
  * `<!--`: Matches the opening `<!--` of the comment.
  * `[\s\S]*?`: Matches any character, including newlines, in a non-greedy way.
  * `-->`: Matches the closing `-->` of the comment.

#### **32. Match an Integer in Scientific Notation**

Regex to match numbers in scientific notation (e.g., `1e10`, `1.23e-10`):

```regex
^[+-]?\d+(\.\d+)?([eE][+-]?\d+)?$
```

* **Explanation**:
  * `^[+-]?`: Matches an optional leading sign (`+` or `-`).
  * `\d+(\.\d+)?`: Matches an integer or decimal number.
  * `([eE][+-]?\d+)?$`: Matches the scientific notation part (`e` or `E` followed by an optional sign and digits).

#### **33. Match a Valid HTML Attribute Value**

Regex to match a valid HTML attribute value (e.g., `src="image.jpg"`):

```regex
=\s*"(.*?)"\s*
```

* **Explanation**:
  * `=\s*`: Matches the equal sign followed by optional spaces.
  * `"(.*?)"`: Matches a quoted string and captures its content (non-greedy).
  * `\s*`: Matches optional spaces after the closing quote.

#### **34. Match a Roman Numeral**

Regex to match Roman numerals (I, II, III, IV, etc.):

```regex
^M{0,4}(CM|CD|D?C{0,3})(XC|XL|L?X{0,3})(IX|IV|V?I{0,3})$
```

* **Explanation**:
  * Matches Roman numerals from `I` to `MMMCMXCIV` (up to 3999).

#### **35. Match a Word Boundary**

Regex to match a word boundary (where a word ends or begins):

```regex
\bword\b
```

* **Explanation**:
  * `\b`: Matches a word boundary, ensuring the pattern matches only the word `word` and not part of another word (e.g., `keyword`).

#### **36. Match a Digit Group with Comma (e.g., `1,000`, `12,345`)**

Regex to match a digit group with commas:

```regex
^\d{1,3}(?:,\d{3})*$
```

* **Explanation**:
  * `^\d{1,3}`: Matches one to three digits at the start.
  * `(?:,\d{3})*`: Matches groups of exactly three digits preceded by a comma, optionally multiple times.

***





Certainly! Here are even more useful regular expressions for a variety of tasks:

***

#### **37. Match a Word with Optional Apostrophe (e.g., `it's`, `John's`)**

Regex to match words with an optional apostrophe:

```regex
^[a-zA-Z]+(?:'[a-zA-Z]+)?$
```

* **Explanation**:
  * `^[a-zA-Z]+`: Matches one or more letters at the beginning.
  * `(?:'[a-zA-Z]+)?`: Optionally matches an apostrophe followed by one or more letters.

#### **38. Match a Floating Point Number (with optional exponent)**

Regex to match a floating-point number with an optional exponent (e.g., `1.23`, `1.23e10`, `1E-10`):

```regex
^[+-]?(\d+(\.\d*)?|\.\d+)([eE][+-]?\d+)?$
```

* **Explanation**:
  * `^[+-]?`: Matches an optional sign (`+` or `-`).
  * `(\d+(\.\d*)?|\.\d+)`: Matches an integer or decimal part.
  * `([eE][+-]?\d+)?$`: Matches an optional scientific notation part.

#### **39. Match a String that Starts with a Specific Word**

Regex to match strings that start with a specific word (e.g., strings starting with "start"):

```regex
^start.*
```

* **Explanation**:
  * `^start`: Matches the word "start" at the beginning of the string.
  * `.*`: Matches any characters following the word "start".

#### **40. Match a Non-Capturing Group**

Regex to match a non-capturing group (useful for grouping without capturing for back-references):

```regex
(?:pattern)
```

* **Explanation**:
  * `(?: ...)`: Groups part of the regex pattern without capturing the match. It's useful when you want to apply quantifiers or other operations to a group but don’t need to refer to it later.

#### **41. Match a Digit or Hyphen (e.g., `123-456`)**

Regex to match digits or a hyphen:

```regex
^[\d-]+$
```

* **Explanation**:
  * `^[\d-]+$`: Matches one or more digits or hyphens from start to end.

#### **42. Match a Set of Digits with Exactly Three Decimal Places**

Regex to match a decimal number with exactly three digits after the decimal point:

```regex
^\d+\.\d{3}$
```

* **Explanation**:
  * `^\d+`: Matches one or more digits before the decimal point.
  * `\.\d{3}$`: Matches exactly three digits after the decimal point.

#### **43. Match a Valid MAC Address**

Regex to match a MAC address (e.g., `00:1A:2B:3C:4D:5E`):

```regex
^([0-9A-Fa-f]{2}[:.-]){5}[0-9A-Fa-f]{2}$
```

* **Explanation**:
  * `([0-9A-Fa-f]{2}[:.-]){5}`: Matches the first five groups of two hexadecimal digits followed by a colon, dot, or hyphen.
  * `[0-9A-Fa-f]{2}$`: Matches the last two hexadecimal digits.

#### **44. Match a Sentence Ending with a Period, Question Mark, or Exclamation Mark**

Regex to match a sentence that ends with a period, question mark, or exclamation mark:

```regex
^[A-Za-z0-9\s,;:'\"!?()\-]+[.?!]$
```

* **Explanation**:
  * `^[A-Za-z0-9\s,;:'\"!?()\-]+`: Matches a sentence that consists of letters, numbers, spaces, and common punctuation marks.
  * `[.?!]$`: Ensures the sentence ends with a period, question mark, or exclamation mark.

#### **45. Match a String that Contains Only Letters and Numbers (Alphanumeric)**

Regex to match a string containing only alphanumeric characters:

```regex
^[a-zA-Z0-9]+$
```

* **Explanation**:
  * `^[a-zA-Z0-9]+$`: Matches one or more letters or digits.

#### **46. Match a Sequence of Digits or Letters**

Regex to match a string that contains only digits or letters (but not both):

```regex
^[a-zA-Z]+$|^\d+$
```

* **Explanation**:
  * `^[a-zA-Z]+$`: Matches one or more letters.
  * `^\d+$`: Matches one or more digits.
  * The `|` operator allows either of the two conditions to match.

#### **47. Match a Word with Only Lowercase Letters**

Regex to match a word that contains only lowercase letters:

```regex
^[a-z]+$
```

* **Explanation**:
  * `^[a-z]+$`: Matches one or more lowercase letters from start to end.

#### **48. Match an HTML Tag Without Attributes**

Regex to match an HTML tag without any attributes (e.g., `<div>`, `<span>`):

```regex
<([a-zA-Z]+)[^>]*>.*<\/\1>
```

* **Explanation**:
  * `<([a-zA-Z]+)`: Matches the tag name (only letters).
  * `[^>]*`: Matches any optional attributes inside the tag.
  * `.*<\/\1>`: Matches the content inside the tag and ensures the closing tag corresponds to the opening tag.

#### **49. Match a String Containing Only Whitespace Characters**

Regex to match a string consisting only of whitespace (spaces, tabs, etc.):

```regex
^\s+$
```

* **Explanation**:
  * `^\s+$`: Matches one or more whitespace characters from start to end.

#### **50. Match a Word that Doesn't Contain Digits**

Regex to match a word that doesn’t contain digits:

```regex
^[^\d]+$
```

* **Explanation**:
  * `^[^\d]+$`: Matches a string of characters that contains no digits.

#### **51. Match a URL with HTTP or HTTPS Only**

Regex to match a URL that starts with `http` or `https`:

```regex
^https?:\/\/[^\s/$.?#].[^\s]*$
```

* **Explanation**:
  * `^https?`: Matches `http` or `https`.
  * `:\/\/`: Matches the `://` after the protocol.
  * `[^\s/$.?#].[^\s]*$`: Matches the rest of the URL.

#### **52. Match a String Containing Only Digits and Hyphens**

Regex to match a string that contains only digits and hyphens:

```regex
^[\d-]+$
```

* **Explanation**:
  * `^[\d-]+$`: Matches one or more digits or hyphens from start to end.

#### **53. Match an ASCII Character**

Regex to match a single ASCII character:

```regex
^[\x00-\x7F]$
```

* **Explanation**:
  * `^[\x00-\x7F]$`: Matches a character in the ASCII range (`0x00` to `0x7F`).

#### **54. Match a Whole Number with Optional Leading Zeros**

Regex to match a whole number that may have leading zeros (e.g., `00123`, `123`):

```regex
^0*\d+$
```

* **Explanation**:
  * `^0*`: Matches any leading zeros.
  * `\d+$`: Matches one or more digits.

#### **55. Match Any Word Except a Specific Word**

Regex to match any word except a specific word (e.g., match any word except "exclude"):

```regex
^(?!exclude$)\w+$
```

* **Explanation**:
  * `^(?!exclude$)`: Uses a negative lookahead to ensure that the word "exclude" is not matched.
  * `\w+$`: Matches one or more word characters.

#### **56. Match a Time with Optional Leading Zeros**

Regex to match time in `HH:MM` format, allowing leading zeros (e.g., `03:05`, `10:30`):

```regex
^(0[0-9]|1[0-9]|2[0-3]):([0-5][0-9])$
```

* **Explanation**:
  * `(0[0-9]|1[0-9]|2[0-3])`: Matches hours from `00` to `23`.
  * `([0-5][0-9])`: Matches minutes from `00` to `59`.

***





Sure! Here are even more useful regular expressions for various purposes:

***

#### **57. Match a Zip Code (5-digit US)**

Regex to match a 5-digit US zip code:

```regex
^\d{5}$
```

* **Explanation**:
  * `^\d{5}$`: Matches exactly five digits from start to end.

#### **58. Match a Zip Code with Optional 4-digit Extension (ZIP+4)**

Regex to match a 5-digit or ZIP+4 US zip code (e.g., `12345` or `12345-6789`):

```regex
^\d{5}(-\d{4})?$
```

* **Explanation**:
  * `^\d{5}`: Matches five digits.
  * `(-\d{4})?$`: Optionally matches a hyphen followed by four digits.

#### **59. Match a Credit Card Number (Visa, MasterCard, AmEx, etc.)**

Regex to match a credit card number (Visa, MasterCard, American Express):

```regex
^4[0-9]{12}(?:[0-9]{3})?$|^5[1-5][0-9]{14}$|^3[47][0-9]{13}$
```

* **Explanation**:
  * `^4[0-9]{12}(?:[0-9]{3})?$`: Matches Visa card numbers (13 or 16 digits).
  * `^5[1-5][0-9]{14}$`: Matches MasterCard card numbers (16 digits).
  * `^3[47][0-9]{13}$`: Matches American Express card numbers (15 digits).

#### **60. Match an Email Address (Basic)**

Regex to match a basic email address (e.g., `user@example.com`):

```regex
^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$
```

* **Explanation**:
  * `^[a-zA-Z0-9._%+-]+`: Matches the local part (before the `@` symbol).
  * `@[a-zA-Z0-9.-]+`: Matches the domain name.
  * `\.[a-zA-Z]{2,}$`: Matches the top-level domain (TLD).

#### **61. Match a URL with Query Parameters**

Regex to match a URL with optional query parameters (e.g., `http://example.com?key=value`):

```regex
^https?:\/\/[^\s/$.?#].[^\s]*\?[^\s]*$
```

* **Explanation**:
  * `^https?:\/\/`: Matches the protocol (`http` or `https`).
  * `[^\s/$.?#].[^\s]*`: Matches the domain and path.
  * `\?[^\s]*$`: Matches the query string starting with `?`.

#### **62. Match a Valid File Path (Windows)**

Regex to match a Windows file path (e.g., `C:\Users\Documents\file.txt`):

```regex
^[A-Za-z]:\\(?:[^\\\n\r]+\\)*[^\\\n\r]*$
```

* **Explanation**:
  * `^[A-Za-z]:\\`: Matches the drive letter followed by a backslash.
  * `(?:[^\\\n\r]+\\)*`: Matches directory names followed by backslashes.
  * `[^\\\n\r]*$`: Matches the file name at the end.

#### **63. Match a Valid File Path (Unix/Linux)**

Regex to match a Unix/Linux file path (e.g., `/home/user/file.txt`):

```regex
^\/(?:[^\/\n\r]+\/)*[^\/\n\r]*$
```

* **Explanation**:
  * `^\/`: Matches the starting forward slash (`/`).
  * `(?:[^\/\n\r]+\/)*`: Matches directory names followed by forward slashes.
  * `[^\/\n\r]*$`: Matches the file name at the end.

#### **64. Match a Single Word Without Numbers or Special Characters**

Regex to match a word that contains only alphabetic characters (no digits, no special characters):

```regex
^[a-zA-Z]+$
```

* **Explanation**:
  * `^[a-zA-Z]+$`: Matches one or more letters from start to end.

#### **65. Match a String with Exactly 6 Characters**

Regex to match a string of exactly 6 characters:

```regex
^.{6}$
```

* **Explanation**:
  * `^.{6}$`: Matches exactly six characters of any kind.

#### **66. Match a String with Multiple Words Separated by Spaces**

Regex to match a string that contains multiple words separated by spaces (e.g., `hello world`):

```regex
^\w+(\s+\w+)+$
```

* **Explanation**:
  * `^\w+`: Matches the first word.
  * `(\s+\w+)+`: Matches one or more additional words, each preceded by one or more spaces.

#### **67. Match a Hexadecimal Color Code (with optional `#`)**

Regex to match a hexadecimal color code (e.g., `#ff5733` or `ff5733`):

```regex
^#?([a-fA-F0-9]{6}|[a-fA-F0-9]{3})$
```

* **Explanation**:
  * `^#?`: Matches an optional `#` symbol.
  * `([a-fA-F0-9]{6}|[a-fA-F0-9]{3})$`: Matches either a 6-digit or 3-digit hexadecimal color code.

#### **68. Match a Decimal Number with Optional Negative Sign**

Regex to match a decimal number with an optional negative sign (e.g., `-3.14`, `0.5`, `42`):

```regex
^[+-]?\d*\.?\d+$
```

* **Explanation**:
  * `^[+-]?`: Matches an optional leading `+` or `-`.
  * `\d*\.?\d+$`: Matches the digits before and after the decimal point.

#### **69. Match a Valid Date (YYYY-MM-DD format)**

Regex to match a date in `YYYY-MM-DD` format:

```regex
^\d{4}-(0[1-9]|1[0-2])-(0[1-9]|[12][0-9]|3[01])$
```

* **Explanation**:
  * `^\d{4}`: Matches the year part (4 digits).
  * `-(0[1-9]|1[0-2])`: Matches the month part (01-12).
  * `-(0[1-9]|[12][0-9]|3[01])$`: Matches the day part (01-31).

#### **70. Match a String Containing a Specific Substring (e.g., `test`)**

Regex to match a string that contains a specific substring (e.g., `test`):

```regex
.*test.*
```

* **Explanation**:
  * `.*test.*`: Matches any string that contains the substring "test" anywhere in the string.

#### **71. Match Multiple Spaces or Tabs**

Regex to match one or more spaces or tabs:

```regex
[ \t]+
```

* **Explanation**:
  * `[ \t]+`: Matches one or more space or tab characters.

#### **72. Match a String with Mixed Case (Both Upper and Lower)**

Regex to match a string that contains both uppercase and lowercase letters:

```regex
^(?=.*[a-z])(?=.*[A-Z]).+$
```

* **Explanation**:
  * `^(?=.*[a-z])(?=.*[A-Z])`: Uses positive lookaheads to ensure the string contains at least one lowercase letter and one uppercase letter.
  * `.+$`: Matches the rest of the string.

#### **73. Match a String of Words with Dashes (e.g., `word-word-word`)**

Regex to match a string that contains words connected by dashes:

```regex
^[a-zA-Z]+(-[a-zA-Z]+)+$
```

* **Explanation**:
  * `^[a-zA-Z]+`: Matches the first word.
  * `(-[a-zA-Z]+)+$`: Matches subsequent words, each prefixed by a hyphen.

#### **74. Match HTML Tags Without Closing Tag (Self-Closing)**

Regex to match self-closing HTML tags (e.g., `<img />`, `<br />`):

```regex
<([a-zA-Z]+)[^>]*\/>
```

* **Explanation**:
  * `<([a-zA-Z]+)`: Matches the tag name.
  * `[^>]*`: Matches any attributes.
  * `\/>`: Matches the closing `/>` for self-closing tags.

#### **75. Match a Non-Alphanumeric Character**

Regex to match any non-alphanumeric character (excluding spaces):

```regex
[^a-zA-Z0-9\s]
```

* **Explanation**:
  * `[^a-zA-Z0-9\s]`: Matches any character that is not a letter, number, or space.

***





Sure! Here are more regular expressions that cover a variety of use cases:

***

#### **76. Match a Social Security Number (SSN) (US format)**

Regex to match a valid U.S. Social Security Number (e.g., `123-45-6789`):

```regex
^\d{3}-\d{2}-\d{4}$
```

* **Explanation**:
  * `^\d{3}-`: Matches the first three digits followed by a hyphen.
  * `\d{2}-`: Matches the next two digits followed by a hyphen.
  * `\d{4}$`: Matches the last four digits.

#### **77. Match a 24-hour Time Format (HH:MM:SS)**

Regex to match a time in `HH:MM:SS` format (e.g., `14:30:45`):

```regex
^(?:[01]?\d|2[0-3]):[0-5]?\d:[0-5]?\d$
```

* **Explanation**:
  * `^(?:[01]?\d|2[0-3])`: Matches hours (`00`-`23`).
  * `:[0-5]?\d`: Matches minutes (`00`-`59`).
  * `:[0-5]?\d$`: Matches seconds (`00`-`59`).

#### **78. Match a String Containing Only Lowercase Letters and Spaces**

Regex to match a string that contains only lowercase letters and spaces:

```regex
^[a-z ]+$
```

* **Explanation**:
  * `^[a-z ]+$`: Matches one or more lowercase letters or spaces.

#### **79. Match a String with Any Number of Digits and a Decimal Point (e.g., `123.45`)**

Regex to match a string that contains digits and an optional decimal point:

```regex
^\d+(\.\d+)?$
```

* **Explanation**:
  * `^\d+`: Matches one or more digits.
  * `(\.\d+)?$`: Optionally matches a decimal point followed by one or more digits.

#### **80. Match a URL with Optional Fragment**

Regex to match a URL that optionally includes a fragment (e.g., `http://example.com#section`):

```regex
^https?:\/\/[^\s/$.?#].[^\s]*#?[^\s]*$
```

* **Explanation**:
  * `^https?:\/\/`: Matches the protocol (`http` or `https`).
  * `[^\s/$.?#].[^\s]*`: Matches the domain and path.
  * `#?[^\s]*$`: Optionally matches the fragment identifier after `#`.

#### **81. Match a Positive Integer (without leading zeros)**

Regex to match a positive integer (without leading zeros):

```regex
^[1-9]\d*$
```

* **Explanation**:
  * `^[1-9]`: Matches a non-zero digit at the beginning.
  * `\d*$`: Matches any number of digits following the first digit.

#### **82. Match a Valid IPv6 Address**

Regex to match a valid IPv6 address:

```regex
^([0-9a-fA-F]{1,4}:){7}[0-9a-fA-F]{1,4}$
```

* **Explanation**:
  * `^([0-9a-fA-F]{1,4}:){7}`: Matches the first seven groups of 1 to 4 hexadecimal digits, each followed by a colon.
  * `[0-9a-fA-F]{1,4}$`: Matches the last group of 1 to 4 hexadecimal digits.

#### **83. Match a String with an Even Number of Characters**

Regex to match a string with an even number of characters:

```regex
^(..)*$
```

* **Explanation**:
  * `^(..)*$`: Matches any even-length string, as it matches pairs of characters.

#### **84. Match a String that Starts with a Specific Word and Ends with Another (e.g., "start" and "end")**

Regex to match a string that starts with "start" and ends with "end":

```regex
^start.*end$
```

* **Explanation**:
  * `^start`: Matches the word "start" at the beginning of the string.
  * `.*end$`: Matches any characters and ensures the string ends with "end".

#### **85. Match a Valid Time in 12-hour Format (AM/PM)**

Regex to match a time in 12-hour format with AM/PM (e.g., `02:30 PM`, `11:59 AM`):

```regex
^(0[1-9]|1[0-2]):[0-5]?[0-9] (AM|PM)$
```

* **Explanation**:
  * `^(0[1-9]|1[0-2])`: Matches hours from `01` to `12`.
  * `:[0-5]?[0-9]`: Matches minutes from `00` to `59`.
  * `(AM|PM)$`: Matches either `AM` or `PM`.

#### **86. Match a String with a Minimum Length of 5 Characters**

Regex to match a string that has at least 5 characters:

```regex
^.{5,}$
```

* **Explanation**:
  * `^.{5,}$`: Matches any string that has at least 5 characters.

#### **87. Match a Non-Alphanumeric Character (not including spaces)**

Regex to match any non-alphanumeric character (excluding spaces):

```regex
[^a-zA-Z0-9]
```

* **Explanation**:
  * `[^a-zA-Z0-9]`: Matches any character that is not a letter or digit.

#### **88. Match a String Containing Any Digits or Letters (Alphanumeric with Space)**

Regex to match a string containing digits, letters, and spaces:

```regex
^[a-zA-Z0-9 ]+$
```

* **Explanation**:
  * `^[a-zA-Z0-9 ]+$`: Matches one or more alphanumeric characters or spaces.

#### **89. Match a URL (with path and query string)**

Regex to match a URL that includes a path and query string (e.g., `http://example.com/path?query=value`):

```regex
^https?:\/\/[^\s/$.?#].[^\s]*$
```

* **Explanation**:
  * `^https?:\/\/`: Matches `http` or `https` protocols.
  * `[^\s/$.?#].[^\s]*$`: Matches the domain, path, and query string.

#### **90. Match a Valid Hexadecimal Number (including optional sign)**

Regex to match a valid hexadecimal number with optional sign (e.g., `-0x1F`, `0xFF`):

```regex
^[+-]?0x[0-9a-fA-F]+$
```

* **Explanation**:
  * `^[+-]?`: Matches an optional sign (`+` or `-`).
  * `0x`: Matches the prefix for hexadecimal numbers.
  * `[0-9a-fA-F]+$`: Matches one or more hexadecimal digits.

#### **91. Match a String with Multiple Consecutive Spaces**

Regex to match a string with multiple consecutive spaces:

```regex
\s{2,}
```

* **Explanation**:
  * `\s{2,}`: Matches two or more spaces.

#### **92. Match a String with Only Uppercase Letters**

Regex to match a string that contains only uppercase letters:

```regex
^[A-Z]+$
```

* **Explanation**:
  * `^[A-Z]+$`: Matches one or more uppercase letters.

#### **93. Match a Valid Date (MM/DD/YYYY format)**

Regex to match a date in `MM/DD/YYYY` format (e.g., `12/31/2020`):

```regex
^(0[1-9]|1[0-2])\/([0-2][0-9]|3[01])\/\d{4}$
```

* **Explanation**:
  * `^(0[1-9]|1[0-2])`: Matches the month (`01`-`12`).
  * `\/([0-2][0-9]|3[01])`: Matches the day (`01`-`31`).
  * `\/\d{4}$`: Matches the year (`4 digits`).

#### **94. Match a String with Only One Word**

Regex to match a string with only one word (no spaces):

```regex
^\S+$
```

* **Explanation**:
  * `^\S+$`: Matches one or more non-whitespace characters.

#### **95. Match a Valid Phone Number (International)**

Regex to match a phone number with an optional country code (e.g., `+1-800-555-5555`):

```regex
^\+?\d{1,4}?[-.\s]?\(?\d{1,3}?\)?[-.\s]?\d{1,4}[-.\s]?\d{1,4}[-.\s]?\d{1,9}$
```

* **Explanation**:
  * `^\+?\d{1,4}?`: Matches an optional country code.
  * `[-.\s]?\(?\d{1,3}?\)?`: Matches the area code.
  * `[-.\s]?\d{1,4}[-.\s]?\d{1,4}[-.\s]?\d{1,9}$`: Matches the main phone number.

***

Certainly! Here are more useful regular expressions, including some for matching user agents and other common use cases:

***

#### **96. Match a Valid User-Agent String**

Regex to match a basic User-Agent string (e.g., `Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.124 Safari/537.36`):

```regex
^Mozilla\/5\.0 \([^)]+\) AppleWebKit\/[0-9]+\.[0-9]+ \([^)]+\) Chrome\/[0-9]+\.[0-9]+\.[0-9]+\.[0-9]+ Safari\/[0-9]+\.[0-9]+$
```

* **Explanation**:
  * `^Mozilla\/5\.0`: Matches the beginning of the User-Agent, including "Mozilla/5.0".
  * `\([^)]+\)`: Matches the operating system and platform information inside parentheses.
  * `AppleWebKit\/[0-9]+\.[0-9]+`: Matches the WebKit version.
  * `Chrome\/[0-9]+\.[0-9]+\.[0-9]+\.[0-9]+`: Matches the Chrome version number.
  * `Safari\/[0-9]+\.[0-9]+$`: Matches the Safari version number.

#### **97. Match a Simple Web Browser User-Agent**

Regex to match a simple web browser User-Agent like `Mozilla/5.0` or `Chrome/91.0`:

```regex
^(Mozilla\/5\.0|Chrome\/[0-9]+\.[0-9]+\.[0-9]+\.[0-9]+|Safari\/[0-9]+\.[0-9]+)$
```

* **Explanation**:
  * `^(Mozilla\/5\.0|Chrome\/[0-9]+\.[0-9]+\.[0-9]+\.[0-9]+|Safari\/[0-9]+\.[0-9]+)$`: Matches either Mozilla, Chrome, or Safari user agent formats.

#### **98. Match a Valid IPv4 Address (with more validation)**

Regex to match a valid IPv4 address (e.g., `192.168.0.1`):

```regex
^((25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)$
```

* **Explanation**:
  * `25[0-5]`: Matches numbers between 250 and 255.
  * `2[0-4][0-9]`: Matches numbers between 200 and 249.
  * `[01]?[0-9][0-9]?`: Matches numbers between 0 and 199.
  * `\.`: Matches the dot separator between octets.
  * The pattern is repeated three times for the first three octets and once for the last.

#### **99. Match a Valid Domain Name (with optional subdomains)**

Regex to match a valid domain name, with or without subdomains (e.g., `example.com`, `sub.example.com`):

```regex
^(?:[a-zA-Z0-9-]+\.)+[a-zA-Z]{2,}$
```

* **Explanation**:
  * `^(?:[a-zA-Z0-9-]+\.)+`: Matches the subdomains, if present.
  * `[a-zA-Z]{2,}$`: Matches the top-level domain (TLD), which must contain at least two alphabetic characters.

#### **100. Match a Valid Email Address (Improved Version)**

Regex to match a valid email address with stricter validation:

```regex
^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$
```

* **Explanation**:
  * `^[a-zA-Z0-9._%+-]+`: Matches the local part (before the `@` symbol).
  * `@[a-zA-Z0-9.-]+`: Matches the domain part (after the `@` symbol).
  * `\.[a-zA-Z]{2,}$`: Matches the top-level domain (TLD), which must be at least two alphabetic characters.

#### **101. Match an ISO 8601 Date Format (e.g., `2025-01-24`)**

Regex to match a date in ISO 8601 format (e.g., `2025-01-24`):

```regex
^\d{4}-(0[1-9]|1[0-2])-(0[1-9]|[12][0-9]|3[01])$
```

* **Explanation**:
  * `^\d{4}`: Matches the year (`4 digits`).
  * `-(0[1-9]|1[0-2])`: Matches the month (`01`-`12`).
  * `-(0[1-9]|[12][0-9]|3[01])$`: Matches the day (`01`-`31`).

#### **102. Match a Password with Specific Criteria (e.g., at least 8 characters, one uppercase, one number, one special character)**

Regex to match a password with at least 8 characters, one uppercase letter, one lowercase letter, one digit, and one special character:

```regex
^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[!@#$%^&*])[A-Za-z\d!@#$%^&*]{8,}$
```

* **Explanation**:
  * `^(?=.*[a-z])`: At least one lowercase letter.
  * `(?=.*[A-Z])`: At least one uppercase letter.
  * `(?=.*\d)`: At least one digit.
  * `(?=.*[!@#$%^&*])`: At least one special character from the given set.
  * `[A-Za-z\d!@#$%^&*]{8,}$`: Matches the password with at least 8 characters.

#### **103. Match a Valid Credit Card Number (with Basic Format Check)**

Regex to match a credit card number (e.g., `4111 1111 1111 1111`):

```regex
^(4[0-9]{12}(?:[0-9]{3})?|5[1-5][0-9]{14}|3[47][0-9]{13}|6(?:011|5[0-9]{2})[0-9]{12})$
```

* **Explanation**:
  * `^4[0-9]{12}(?:[0-9]{3})?`: Matches a Visa card number (13 or 16 digits).
  * `5[1-5][0-9]{14}`: Matches a MasterCard number (16 digits).
  * `3[47][0-9]{13}`: Matches an American Express card number (15 digits).
  * `6(?:011|5[0-9]{2})[0-9]{12}$`: Matches a Discover card number (16 digits).

#### **104. Match a Valid International Phone Number (including country code)**

Regex to match a valid international phone number, including optional country code (e.g., `+1-800-555-5555`, `+44 7911 123456`):

```regex
^\+?[1-9]\d{1,14}$
```

* **Explanation**:
  * `^\+?`: Matches an optional `+` symbol.
  * `[1-9]`: Matches a non-zero starting digit for the country code.
  * `\d{1,14}$`: Matches the remaining digits, allowing for up to 15 digits total.

#### **105. Match a Single Digit (0-9)**

Regex to match a single digit between `0` and `9`:

```regex
^\d$
```

* **Explanation**:
  * `^\d$`: Matches exactly one digit.

#### **106. Match a String Containing a Specific Word (e.g., `hello`)**

Regex to match a string that contains the word "hello" (case-sensitive):

```regex
.*\bhello\b.*
```

* **Explanation**:
  * `.*`: Matches any characters before and after the word.
  * `\bhello\b`: Matches the word "hello" as a whole word, with word boundaries.

#### **107. Match a Floating Point Number (with optional negative sign)**

Regex to match a floating-point number, optionally with a negative sign (e.g., `-3.14`, `0.5`, `42.00`):

```regex
^[+-]?\d*\.\d+$
```

* **Explanation**:
  * `^[+-]?`: Matches an optional sign (`+` or `-`).
  * `\d*\.\d+$`: Matches the number with a decimal point and at least one digit after it.

#### **108. Match a Valid URL (General)**

Regex to match a general URL that includes the protocol, domain, and optional path (e.g., `http://example.com/path`):

```regex
^(https?|ftp):\/\/[^\s/$.?#].[^\s]*$
```

* **Explanation**:
  * `^(https?|ftp)`: Matches `http`, `https`, or `ftp` protocols.
  * `:\/\/`: Matches `://`.
  * `[^\s/$.?#].[^\s]*$`: Matches the domain and the path.

***

