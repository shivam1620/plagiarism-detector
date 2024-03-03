# plagiarism-detector


The plagiarism detector implemented using Counting Bloom Filters (CBF) is designed to identify identical sequences of words in text documents. The CBF, an enhanced version of the standard Bloom Filter, uses an array of multi-bit counters instead of a binary array. This allows the CBF to count occurrences and support element deletions, making it suitable for dynamic data sets.

The detector defines plagiarism as the occurrence of five consecutive identical words between two texts. It operates by breaking the text into five-word strings, inserting these strings into the CBF, and then searching for these strings in another text. The number of matches is counted, and the extent of plagiarism is determined by comparing this count with the length of the second text. This approach is space-efficient, handles large datasets effectively, and scales well with data size, offering a fast preliminary check for plagiarism. However, it cannot detect paraphrased content and may miss extended plagiarized sentences beyond the five-word threshold.
