# Serial Generator and Word Finder

## Overview

This project features two key functionalities implemented in Python: a serial number generator and a word finder. The SerialGenerator class enables the creation of unique serial numbers, while the WordFinder class reads words from a text file and returns random selections. Additionally, the SpecialWordFinder class extends this functionality by filtering out comments and blank lines from the file, ensuring that only meaningful words are retrieved.

## Project Structure

- **`complex.txt`**: A text file containing a categorized list of items (fruits and vegetables), with comments.
- **`simple.txt`**: A text file containing a simple list of animals.
- **`serial.py`**: Contains the `SerialGenerator` class, which generates unique serial numbers starting from a specified value.
- **`wordfinder.py`**: Contains the `WordFinder` class for retrieving random words from a file, and the `SpecialWordFinder` class, which ignores comments and blank lines.

## Classes and Usage

### SerialGenerator

A class to generate unique serial numbers.

**Example:**
```python
from serial import SerialGenerator

serial = SerialGenerator(start=100)
print(serial.generate())  # Output: 100
print(serial.generate())  # Output: 101
serial.reset()
print(serial.generate())  # Output: 100
```

### WordFinder

A class to read words from a file and return a random word.

**Example:**
```python
from wordfinder import WordFinder

wf = WordFinder("simple.txt")
print(wf.random())  # Randomly outputs one of the words in simple.txt
```

### SpecialWordFinder

An extension of `WordFinder` that ignores comments and blank lines.

**Example:**
```python
from wordfinder import SpecialWordFinder

swf = SpecialWordFinder("complex.txt")
print(swf.random())  # Randomly outputs one of the words in complex.txt (ignoring comments)
```

## Getting Started

### Prerequisites

- Python 3.x

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Run the Python scripts as shown in the usage examples.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
