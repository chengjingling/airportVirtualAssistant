# Airport Virtual Assistant

## About

This application is a speech recognition system designed to assist with passenger enquiries at an airport. It aims to recognise spoken commands from passengers in English, Spanish and Italian as accurately as possible. This application is tested on 20 given audio files and 2 self-recorded audio files, and the accuracy is calculated using the word error rate (WER). Various audio features were implemented on some of the audio files to improve the WER.

## Software used

The software used for speech recognition was Mozilla DeepSpeech. To configure Mozilla DeepSpeech, I installed it using the command "pip install deepspeech".

**Note:** This notebook cannot be run anymore as Mozilla DeepSpeech no longer works with newer versions of Python. To view the full code, please refer to the video attached.

## Audio features implemented

After experimenting with different solutions such as gain, low-pass filter and high-pass filter, I concluded that there is no solution that works for all of the audio files. As a result, I decided to do what is best for the WER, and implement solutions only for specific audio files.

For checkin.wav, checkin_child.wav and suitcase_child.wav, I lowered the frequency of the audio files by 2 semitones by performing a pitch shift using linear interpolation.

For what_time_it.wav, I increased the gain by 10 decibels using PyDub.

## Analysis of results

After implementing the audio features, I obtained the following results:

| **Language** | **File** | **WER** |
| English | checkin.wav | 0% |
| English | checkin_child.wav | 50% |
| English | parents.wav | 20% |
| English | parents_child.wav | 20% |
| English | suitcase.wav | 0% |
| English | suitcase_child.wav | 16.66% |
| English | what_time.wav | 20% |
| English | what_time_child.wav | 20% |
| English | where.wav | 0% |
| English | where_child.wav | 0% |
| Spanish | checkin_es.wav | 25% |
| Spanish | parents_es.wav | 0% |
| Spanish | suitcase_es.wav | 0% |
| Spanish | what_time_es.wav | 0% |
| Spanish | where_es.wav | 14.28% |
| Italian | checkin_it.wav | 0% |
| Italian | parents_it.wav | 20% |
| Italian | suitcase_it.wav | 14.28% |
| Italian | what_time_it.wav | 16.66% |
| Italian | where_it.wav | 0% |
| English | your_sentence1.wav | 20% |
| English | your_sentence2.wav | 12.5% |
