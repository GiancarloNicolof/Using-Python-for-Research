# Case study 02: Language Processing

- **What is Project Gutenberg?**
  > An online repository of publically available books in many languages.
	
- **The function `count_words` is as defined in Video 3.2.2.
  Consider the following code:**
  ```python
  len(count_words("This comprehension check is to check for comprehension."))
  ```
  What does this return?
  > 6
	
- **The functions `count_words` and `count_words_fast`are as defined in Video 3.2.2. Consider the following code:**
  ```python
  count_words(text) is count_words_fast(text)
  ```
  What does this return?
  > False

- **As defined in Video 3.2.4, which of the following does the function `word_stats` return?**
  > The number of unique words
  > A list of the word counts

- **Which of the two versions of Romeo and Juliet from Project Gutenberg contains more unique words, the original or the German translation?**
  > The German Translation

- **What type of object does `os.listdir` return?**
  > `list`

- **What `pandas` method allows you to insert a row to a dataframe?**
  > `loc`

- **How can you retrieve the first and last few rows of a `pandas` dataframe called `stats`?**
  > `stats.head()` and `stats.tail()`

- **`stats` is a Pandas dataframe as defined in Video 3.2.6. Which of the following options are valid ways to access the column `"length"` in this dataframe? (Select *all* that apply.)**
  > `stats.length`
  > `stats["length"]`

- **`stats` is a Pandas dataframe as defined in Video 3.2.6. How can you select only the rows where the language is French?**
  > `stats[stats.language == "French"]`