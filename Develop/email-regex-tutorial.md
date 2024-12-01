# Matching an Email Address: A Regex Breakdown

Regular expressions, or regex, are powerful tools for searching, matching, and validating text patterns. This tutorial will break down a regex used to validate email addresses, explaining each component in detail. By the end, you'll understand how this regex works and how to modify it for your needs.


## Summary

The regex for matching an email address is:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

This regex ensures a string follows the format of an email address, including:
1. A username (local part) before the `@` symbol.
2. A domain name.
3. A top-level domain like `.com` or `.org`.

We’ll break down its components below.


## Table of Contents
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)


## Regex Components

### Anchors
**Code:** `^` and `$`

- `^` asserts that the match starts at the beginning of the string.
- `$` asserts that the match ends at the end of the string.

**Examples:**
- Matches: `"user@example.com"`
- Does not match: `" Hello user@example.com "` (contains spaces outside the email).

### Quantifiers
**Code:** `+`

- The `+` quantifier matches one or more occurrences of the preceding character or group.
- In this regex, it ensures the username and domain have at least one character.

**Examples:**
- Matches: `"user@example.com"`
- Does not match: `"@example.com"` (no username).


### Character Classes
**Code:** `[a-z0-9_\.-]`

- Matches any of the following characters:
  - Lowercase letters (`a-z`)
  - Digits (`0-9`)
  - Underscore (`_`)
  - Dot (`.`)
  - Hyphen (`-`)

**Examples:**
- Matches: `"user_name"`, `"user.name"`, `"user-name"`
- Does not match: `"user!name"` (contains `!`).

### Grouping and Capturing
**Code:** `([a-z0-9_\.-]+)`

- This creates a capturing group for the username part of the email.
- Similar groups are used for the domain and top-level domain.

**Examples:**
- For `"user@example.com"`, the capturing groups are:
  - Group 1: `"user"`
  - Group 2: `"example"`
  - Group 3: `"com"`

## Author

This tutorial was written by [Your Name](https://github.com/yourusername). I’m a web development student passionate about sharing knowledge. Check out my GitHub for more projects!


A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
