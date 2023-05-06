# YTSummarizer

This code is used to summarize YouTube video subtitles using two different methods: TF-IDF Vectorization and BART Model.

Libraries Used:

youtube_transcript_api
nltk
re
sklearn
transformers

Summarization Using TF-IDF Vectorization:
In this method, the subtitles of a YouTube video are first retrieved using the YouTubeTranscriptApi library. The subtitles are then preprocessed by
removing line breaks and tokenized into sentences using the sent_tokenize method from the nltk library.

After the sentences are tokenized, the TfidfVectorizer method from the sklearn library is used to convert the text into vectors. The sentences are then 
scored using the tf-idf algorithm and the top N sentences with the highest scores are selected.

Finally, the selected sentences are ordered based on their position in the original subtitle file and joined together to create a summary of the video.

Summarization Using BART Model:
In this method, the BartTokenizer and BartForConditionalGeneration classes from the transformers library are used to perform summarization.

The subtitles of the YouTube video are first retrieved and encoded using the BartTokenizer. The encoded text is then passed to the BartForConditionalGeneration
model to generate a summary of the video.

The output of the BartForConditionalGeneration model is a tensor, which is then decoded into text using the BartTokenizer.

Conclusion
This code can be used to generate summaries of YouTube videos using two different methods. The TF-IDF vectorization method is a simple and effective way to
generate summaries, while the BART model provides more advanced summarization capabilities.
