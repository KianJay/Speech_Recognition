# Speech_Recognition
## Executive Summary
This is the final report of the project: build a speaker recognition and mood analysis system. The purpose of the system is to find a speaker in a given dataset and performing text-independent mood analysis. We employed AWS services, JSON, Python (an open-source programming language), and other tools. Initially, we were planning to use a couple of AWS services for machine learning, but we decided to use Colab after all. Fast Fourier Transform (FFT) is used for speaker recognition and the result of each speaker shows the difference in the frequency-domain representation. The accuracy in both speaker recognition and mood analysis is high 0.95% and 0.89% respectively. There are some of the limitations: only 30-second .wav format audio files are available and the model for speaker recognition is trained with 1-second audio files and when it comes the different length of audio files, the model often fails to predict the correct speaker, and the sound of the audio files converted from video files is not equal. The results of FFT are not equal even though the speaker is the same. This leads the model to the wrong prediction. For the recommendations, the system should take different types and length of audio files and normalise audio files used for training the model to produce the same results of FFT and to improve the prediction of the model. 

### Exclusions
- Recognise other people's voices except voices in a dataset
- Currently Only five speakers available: Benjamin Netanyahu,Jens, Julia, Margare and Nelson
- Accept people's voices in real time
### Assumptions
- Speaker recognition: listening to the speech and find the speaker
- Speech recognition: transferring the speech into a text form
- Emotion detection: based on the text form, analysing speaker's emotion
- Display the speaker, speech and emotion all together
### Constraints
- Accept only 30 sec WAV file formats 
- English
- Two emotion: Positive and Negative 
### Data Pre-Processing
After the selected audio files were downloaded, we used a video editor software Movavi Video Suite 18 to convert the sample rate and download the outputs audio files removed unnecessary sounds, such as applause and silence without a speaker’s voice. the Benjamin_Netanyau.wav (565MB) file edited and containing all the five video files. We conducted the same process for the other four speakers’ files.  
The length of each audio file is about 2-hour long. Before divided into 1-second-long audio files, we firstly checked how many 1-second-long audio files can be generated with the soundfile (sf) library with the code shown. After the calculation, the smallest number in the number of divided files is printed out and this number is used later to generate the number of audio files. For example, the smallest number , in this case, is 7752 from Julia_Gillard.

## Stacks
- AWS
- Python 3 / Tensorflow, NLP, SpeechRecognition
- Javascript
- HTML5 & CSS

![Group_01_Project_Final_System_Poster](https://user-images.githubusercontent.com/54985943/123898748-dcf57280-d9a0-11eb-889b-cf93df5abe3a.png)

![KakaoTalk_Photo_2021-06-30-12-48-54-1](https://user-images.githubusercontent.com/54985943/123899237-c0a60580-d9a1-11eb-863e-b3eef05cbf33.png)

## Conclusion
The aim of the project is to implement the speaker recognition and mood analysis system based on the previous proposal. The main investigated points are to understand the basics of audio and deep learning how they work and to develop the server and website so that we can display our result on the website. The achievements and results are quite successful as our system provides and displays the output we intended properly and we have obtained the high accuracy in both speaker recognition and mood analysis models: 0.95% and 0.89% respectively. Although the accuracy is high enough, we have experienced some difficulties in prediction, especially in speaker recognition, due to the lack of pre-processing and knowledge of AI. We enumerated the limitations of the system, such as only 30-second WAV files are available. The recommendations for such issues are that the system should take different types and length of audio files and normalise audio files used for training the model to produce the same results of FFT and to improve the prediction of the model.  


@Contributed by Duyoung Jang (Kian), Insub Kim and Sohwa Lee
