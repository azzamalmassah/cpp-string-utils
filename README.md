
---

#  clsString – C++ String Utility Library (OOP)

`clsString` is a lightweight, header-only C++ utility class that provides a rich set of **string manipulation** functions using both:

*  **Static utility methods** (functional style)
*  **Object-oriented methods** (work on an internal string)

It’s designed for **learning, practice, and real console projects**, with features like trimming, splitting, case conversion, counting letters, replacing words, and more.

---

##  Features

*  Convert to **upper / lower case**
*  Change **first letter** of each word (upper/lower)
*  **Invert** letter cases
*  Get **length** and **count letters** (small, capital, all)
*  Count:

  * Specific letters
  * Vowels
  * Words
*  **Trim** (left, right, both)
*  **Split** strings by delimiter
*  **Join** strings
*  **Reverse** words in a sentence
*  **Replace** words (case-sensitive or insensitive)
*  **Remove punctuation**
*  Print vowels
*  Works as:

  * Static utility class: `clsString::toUpper("text")`
  * OOP wrapper: `clsString s("text"); s.toUpper();`

---

## 🛠️ Requirements

* C++11 or newer
* Standard headers:

  * `<string>`
  * `<vector>`
  * `<iostream>`
  * `<cctype>`

---

##  Installation

Just copy **`clsString.h`** into your project and include it:

```
#include "clsString.h"
```

This is a **header-only** library — no `.cpp` file needed.

---

##  Usage Examples

### 1️⃣ Object-Oriented Style

```
clsString s("  Hello world from C++!  ");

cout << "Original: [" << s.getValue() << "]\n";

s.trim();
cout << "Trimmed: [" << s.getValue() << "]\n";

s.toUpper();
cout << "Upper: " << s.getValue() << endl;

s.toLower();
cout << "Lower: " << s.getValue() << endl;

s.firstLetterToUpper();
cout << "First letters upper: " << s.getValue() << endl;

cout << "Vowels count: " << s.countVowels() << endl;
```

---

### 2️⃣ Static Utility Style

```
string text = "  hello world  ";

cout << clsString::toUpper(text) << endl;
cout << clsString::trim(text) << endl;
cout << clsString::countWordsInString("one two three") << endl;

vector<string> parts = clsString::split("C++ is awesome", " ");
string joined = clsString::joinString(parts, "-");

cout << joined << endl;  // C++-is-awesome
```

---

##  Example `main()`

```
#include <iostream>
#include "clsString.h"

using namespace std;

int main()
{
    clsString s("  Hello world from C++ Programming!  ");

    cout << "Original: [" << s.getValue() << "]\n";
    cout << "Trimmed: [" << s.trim() << "]\n";

    s.toUpper();
    cout << "Upper: " << s.getValue() << endl;

    s.toLower();
    cout << "Lower: " << s.getValue() << endl;

    s.firstLetterToUpper();
    cout << "First letters upper: " << s.getValue() << endl;

    cout << "Vowels count: " << s.countVowels() << endl;

    vector<string> words = s.split(" ");
    cout << "Words:\n";
    for (auto& w : words)
        cout << "[" << w << "]\n";

    cout << "Joined: " << clsString::joinString(words, "_") << endl;

    return 0;
}
```

---
---

##  Notes

* This library is mainly for **learning and practice**
* Some functions focus on clarity over maximum performance


---

