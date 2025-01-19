The code processes Hindi Wikipedia articles by reading and cleaning text files, removing non-Hindi characters, and then applying Byte Pair Encoding (BPE) for tokenization. It first 
tokenizes the text using regex patterns to capture words and punctuation, cleans it to retain only valid Hindi characters, and shuffles the resulting list. It then trains a BPE model 
by counting the frequency of consecutive character pairs, merges the most frequent pairs into new tokens, and iteratively builds a vocabulary. After training, the BPE model is used to 
encode the text, and a decoding function is provided to reverse the tokenization process. This approach efficiently reduces vocabulary size for use in machine learning models, particularly 
for languages with complex morphology like Hindi.

The dataset is picked up from this source :https://www.kaggle.com/datasets/disisbig/hindi-wikipedia-articles-55k

total_tokens:2287
vocab_size:5549
compression_ratio:4.3

# Example:

hindi_sentence = "जो कि पक्षपाती हैं और बेतरतीबी नतीज़ें देती हैं।"

Encoded: ['ज', 'ो', ' ', 'क', 'ि', ' ', 'प', 'क', '्', 'ष', 'प', 'ा', 'त', 'ी', ' ', 'ह', 'ै', 'ं', ' ', 'औ', 'र', ' ', 'ब', 'े', 'त', 'र', 'त', 'ी', 'ब', 'ी', ' ', 'न', 'त', 'ी', 'ज', '़', 'े', 'ं', ' ', 'द', 'े', 'त', 'ी', ' ', 'ह', 'ै', 'ं', '।']
Decoded: जो कि पक्षपाती हैं और बेतरतीबी नतीज़ें देती हैं।
