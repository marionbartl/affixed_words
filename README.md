# Words with Gender-marking Affixes
Repository to extract gender-exclusive words based on their affixes.

As outlined in our paper _From Showgirls to Performers: Fine-tuning with Gender-inclusive
Language for Bias Reduction in LLMs_, there are three rounds of extraction & verification. 

## Round 1 - Word Extraction
Use `word_extraction.ipynb` to extract words with gender-marking affixes from the 200M words OpenWebText corpus.

The files created are 
1. `words/prefixes.json`
2. `words/suffixes.txt`

## Round 2 - Verification with BabelNet
The second round of verification uses the BabelNet Lexical Resource to verify whether the words are commonly used. For this step, use `word_verification.ipynb`. 

The files created are 
1. `words/verified_prefixes.csv`
2. `words/verified_suffixes.csv` 
3. `words/verified_affixes.csv` (1. and 2. combined)

## Round 3 - Adding gender-neutral replacements
Round three was a round of manual verification and adding of gender-neutral replacements, which was done manually. The file that contains the words left after Round 3 is:

`words/replacements.csv`

## Round 4 - Adding plurals

Finally, plural versions were added with the following notebook:

`word_extension.ipynb`

This created the file: 

`words/replacements+plural.csv`

## Final List 
The final version of words with gender-marking affixes and gender-neutral replacements, after one last round of manual checks, is: 

`words/replacements+plural-final.csv`

