# General Description
This respitory contains a folder with 20 song lyrics of Coldplay in the format of txt, a corpus in CSV, a most-played list of Coldplay on Spotify in CSV, and a Jupyter Notebook file regarding the data scraping, cleaning, and annotating processes, aiming to display the process of creating a corpus.

# Purpose of the corpus
This corpus is desinged for the exploration of the language style and emotional characteristics of the lyrics of Coldplay's top 20 most-played songs on Spotify until December 18, 2023 from the perspective of part-of-speech and lemmas.

# Criteria for Text Selection:
- **Why Spotify and Kworb**: 
Kworb is a data-centric website providing up-to-date charts and analytics on music trends across major streaming platforms like Spotify, Apple Music, and YouTube. The top 20 songs on Spotify were chosen because Spotify is one of the world's largest music streaming service providers, with a broad user base. 
  
- **Where to Scrape the Text**: 
The texts were extracted from LyricsFreak, a free platform allowing lyric enthusiasts to search, consult, and study lyrics from various songs.

# Scraping (Collecting) Process
- **Scraping the most-played list from Kworb**: Pandas, Requests in Python was used to send requests to Kworb for ranked, structured data with song names, total streaming counting, and daily streaming counting of Coldplay's songs on Spotify until December 18, 2023. The structured data is saved as CSV format. 

- **Scraping Lyrics**: BeautifulSoup, Requests in Python was used to send requests to the LyricsFreak for lyrics of the top 20, and lyrics of each song is saved as a txt file.

# Cleaning Process
- Removing noise and irrelavent information in brackets [ ]
- Lowercasing
- Removing punctuation
- Removing stopwords 
- Tokenization

# Tagging Process:
- Utilizing the POS function in Spacy to get the POS of tokens.
- Utilizing the lemma function in Spacy to get the lemmas of tokens.

# Format of Corpus 
CSV

# Varibles of Corpus
| Variables       | Description            | Data Type    |
|-----------------|------------------------|--------------|
| filename        | name of the song       | string       |
| original_text   | original text          | string       |
| tokens          | tokens of the text      | string       |
| POS             | part of speech of tokens| string       |
| lemmas          | lemmas of tokens        | string       |
