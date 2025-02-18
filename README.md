# Sci-Fy Text Generator

The **Sci-Fy Text Generator** is a web-based project that dynamically creates scrolling sci‑fi stories using a Star Wars–style crawl animation. Each story is generated by randomly combining preset paragraph templates with words loaded from an external JSON file.

## Features

- **Dynamic Story Generation:**  
  Combines preset sci‑fi themed paragraph templates with random words drawn from categorized word lists in a JSON file.

- **Star Wars–Style Crawl:**  
  Displays the generated story with a slow, scrolling animation reminiscent of the iconic Star Wars opening crawl.

- **Interactive Design:**  
  Clicking anywhere on the screen regenerates the story and restarts the crawl animation.

- **Animated Starfield Background:**  
  A subtle animated starfield creates the illusion of distant, moving stars, enhancing the space theme.

- **Responsive Header with Recognitions:**  
  The header displays:
  - **Title:** "Sci‑Fy Text Generator"
  - **Original Text Source:** A link to the Project Gutenberg Bookshelf.
  - **Author:** Jonathan Woodall
  - **Additional Credit:** Chatgpt o3 mini-high

## File Structure

- **`index.html`**  
  The main HTML file contains all the markup, styles (CSS), and JavaScript needed for the project. It handles loading the JSON data, generating the story, triggering the animation, and displaying the animated starfield.

- **`categorized_words.json`**  
  An external JSON file containing categorized word lists (e.g., nouns, proper nouns, verbs, adjectives, adverbs, characters). These words are used to fill in the placeholders within the story templates. This file must be located in the same directory as `index.html`.

- **`edited_categorized_words.json`**  
  The final usage JSON, updates original JSON to not include words with non-alphabetical characters.

- **`WebScrape.py`**  
  The Python script responsible for scraping Project Gutenberg’s Science Fiction and Fantasy Bookshelf. It downloads the book texts, cleans them by removing Gutenberg-specific headers and footers, and saves the cleaned texts for further processing.

- **`JSON.py`**  
  The Python script that processes the cleaned Gutenberg texts. It tokenizes the texts, performs part-of-speech tagging to categorize words (nouns, verbs, adjectives, etc.), and outputs the results as a JSON file for use in the web-based story generator.

- **`JSONCleaner.py`**  
  This Python script processes a JSON file containing categorized words and cleans each word by removing any non-alphabetic characters (except for hyphens). It is used to prepare a sanitized version of the JSON file for further processing in the project.

## How It Works

1. **Loading Word Categories:**  
   The project uses the Fetch API to load `categorized_words.json` into a global JavaScript variable. This file provides word lists for categories like `nouns`, `proper_nouns`, `verbs`, `adjectives`, `adverbs`, and `characters`.

2. **Story Templates and Placeholder Replacement:**  
   A set of sci‑fi themed paragraph templates is defined in the script. Each template contains placeholders (e.g., `#nouns#`, `#proper_nouns.capitalize#`). A JavaScript function replaces these placeholders with random words from the corresponding categories in the loaded JSON data. The replacement function also supports simple text transformations such as capitalization.

3. **Crawl Animation:**  
   The generated story is displayed in a `<div>` element with a Star Wars–style crawl animation (implemented with CSS keyframes). The text scrolls upward over 40 seconds, providing a slow, readable effect.

4. **Interactive Story Generation:**  
   An event listener is attached to the document body so that any click triggers the generation of a new story and restarts the crawl animation.

5. **Animated Starfield Background:**  
   A fixed `<div>` with a tiny white dot and multiple CSS `box-shadow` coordinates simulates a field of stars. A CSS animation moves these stars slightly upward, adding to the immersive space atmosphere.

6. **dynamic visual or stylistic component:**
  If you reload the page, the stars change their pattern.

## Recognitions

The header in the project includes:
- **Title:** "Sci‑Fy Text Generator"
- **Original Text Source:**  
  [Project Gutenberg Bookshelf](https://www.gutenberg.org/ebooks/bookshelf/480)
- **Author:** Jonathan Woodall
- **Additional Credit:** Chatgpt o3 mini-high

## How to Use

https://jwoodall1.github.io/TextGenerator/

3. **Click Anywhere on the Screen:**  
   Each click generates a new story with the Star Wars–style scrolling effect.

## License

This project is open source. You are free to modify and distribute it as needed.

---

