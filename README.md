# Spell Checker Using Dynamic Programming

This program implements a spell checker that takes a string (a sentence or paragraph) as input and corrects all the misspelled words. It utilizes the concept of dynamic programming and the Levenshtein distance algorithm to suggest the most probable correct words.

## How it Works

1. **Dictionary Collection**: The program starts by collecting a dictionary of around 200K words along with the frequency of usage of each word. This dictionary is stored in a text file.

2. **Word Hashing**: The words in the dictionary, along with their frequencies, are hashed into an unordered map for efficient retrieval and lookup during the spell checking process.

3. **Spell Correction**: When a string (sentence or paragraph) is entered as input, the program breaks it into individual words and analyzes each word for possible misspellings.

4. **Dictionary Lookup**: The program first checks if the word exists in the dictionary map. If it does, the word is considered correct and returned as is.

5. **Correction Memoization**: The program also maintains a map to store previously corrected words. If a word is already corrected, the corresponding correct word is retrieved from the map and returned. This helps reduce computation time.

6. **Edit Distance Calculation**: If the word is not found in the dictionary or the correction map, the program calculates the edit distance (Levenshtein distance) between the current word and each word in the dictionary. It uses a bottom-up/iterative dynamic programming approach, considering three possible operations on the string: replace, erase, and add character.

7. **Nearest Correct Words**: The program identifies the words with the lowest edit distance, assuming these are the nearest correct words that the author intended to type.

8. **Most Probable Word**: Among the words with the lowest edit distance, the program selects the word with the highest frequency of usage in English. It assumes that the word with the highest usage frequency is the most probable correct word.

9. **Spell Correction Output**: The program returns the corrected word to the user. If no correction is found, the original word is returned.

You can also find a screenshot of the program's output below:
![image](https://github.com/Sanky18/Spell-Checker/assets/119156783/4f3603fb-326b-45e2-a6e9-43fd3b031c49)




