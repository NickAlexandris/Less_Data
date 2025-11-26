The following project demonstrates how to convert a STRING data type into an array of words, and how to reconstruct the STRING back from the array.

In many PLC applications, a STRING occupies a fixed buffer that is much larger than the actual text being stored. This means that a significant number of bytes remain unused. To optimize memory usage and retain only the active part of the data, this project shows a method to compress the STRING by splitting it into smaller segments and storing only the necessary bytes.

The array of of charactes is retained DB_LEARN.array_chars.
The DB_Learn.Result is being used to display the the array.chars but not to be retained
