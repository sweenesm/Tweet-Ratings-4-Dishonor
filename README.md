# Tweet-Ratings-4-Dishonor
Python code that uses machine learning to rate politicians' tweets for dishonorable speech

Project Description
===================
Python code that takes downloaded tweet text plus embedded links, and processes them into dishonorable speech ratings using machine learning models. 

The dishonorable speech ratings are for misrepresenting reality, promoting entitlement, negativity, and blame (a subset of promoting entitlement). (See https://dishonorablespeechinpolitics.com/blog2/#3NewRatingsUpdated for more info.) 

Embedded links include those for pictures, videos, news articles, websites, etc. The text of linked news articles, linked statements, etc. are not currently captured for input to the ratings predictions. Optical character recognition (OCR) is used to extract text from pictures. Spoken words in videos are transcribed into text. The code currently handles .jpg, .png, and .mp4 files; it doesn’t handle .gif files. Transcribed text is pre-processed, such as by translating it into English if need be. Transcribed text of less than 140 characters is added to the text of the corresponding tweet for rating. Other pre-processed transcribed text is split into sections of generally 280 characters or less (the max length on Twitter for tweets) before being loaded into machine learning models to predict dishonorable speech ratings. 

Hugging Face ConvBERT-based models are used for ratings predictions. Textblob is also applied to extract subjectivity and polarity values from tweets, for comparison. Results of transcriptions and text pre-treatments are outputted to files, as are ratings for each politician’s Twitter account or accounts. The transcription and ratings operations are typically performed on batches of 9 politicians’ Twitter accounts. Summary files of the ratings for each batch of politicians are also saved. 

A separate Python program is used to tabulate results, capture them as .png files, and tweet them out at @DishonorP.

This code will likely need to be updated periodically to run properly as Twitter evolves, such as when new tweet features are added. 

Check the requirements.txt file for the required third-party dependencies for running the code.


How You Can Help
================
Please follow the Twitter account @DishonorP (https://twitter.com/DisonorP), and like and retweet its tweets.


Contact
=======
sean@dishonorablespeechinpolitics.com


License
=======
GNU Lesser General Public License v2.1 (https://www.gnu.org/licenses/old-licenses/lgpl-2.1.en.html)
