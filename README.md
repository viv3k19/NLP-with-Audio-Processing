# NLP with Audio Processing [Sainya Ranakshetram 2.0]
**This project focuses on the implementation of natural language processing (NLP) techniques on distorted audio signals containing a mix of English and Hindi (Hinglish) with limited use of local slangs. The problem statement includes the development of a software-based tool capable of ingesting low-quality audio recordings and producing a textual output of extracted transcripts. The paper discusses the unique and challenging task of transcribing and translating noise-filled audio recordings containing multiple languages and dialects, along with the difficulties of providing timestamps for the words in the audio file. The paper proposes using the state-of-the-art machine learning model OpenAI Whisper Large-V2 as the ideal solution to transcribe and translate these audio files, citing its robust zero-shot learning capability and excellent performance in handling audio files with high levels of noise and low signal-to-noise ratios. The research concludes that the large-v2 version of Whisper provides the best balance of accuracy and speed for the task at hand.**

# What is my solution

## Problem statement

**The challenge aims to develop a software-based tool that is able to ingest
radio audio recordings (non HiFi) in common format of (.wav, FLAC, MP3 (high bit
rate) etc.) containing information in a mix of English and Hindi (Hinglish) with limited
use of local slang's and create an extract transcript information output in textual
format. This problem intrinsically contains the task of cleaning of raw audio signals,
shaping of signals and creating algo specific data required by the NLP engine.**

## Transcribing and Translating Noise-filled Audio Recordings Containing Multiple Languages and Dialects: A Unique and Difficult Challenge

**As we embark on the challenge of transcribing and translating audio recordings that are full of noise and contain a
mix
of multiple languages and dialects, we quickly realize that we're facing a unique and difficult task. Not only are the
audio files we're working with low quality, with a high percentage of noise relative to signal, but they also contain
slang's and local words that aren't present in any dataset and can't be easily translated using standard language
models.**

**And even when we are able to translate words, we face the added challenge of context-dependent translations that don't
always have a straightforward one-to-one correspondence. For example, the word "Bhai" could be translated as "Brother"
or "Friend" depending on the context.**

**But that's not all - we also need to provide timestamps for the words in the audio file, a critical feature that will
help users navigate and find the specific parts of the audio file they're looking for. All of these challenges combine
to make this task a truly distinctive and challenging one, but with the right tools and approaches, we're confident we
can
rise to the challenge and deliver the best possible results.**

## Model Selection

**As we set out to solve the challenge of transcribing and translating audio recordings that have been distorted and
compressed for transmission over the airwaves, it quickly becomes apparent that we need a model that is up to the task.
The input audio will be of low quality, with a restricted frequency range and the added complications of channel noise,
dialects and slang's. To successfully extract and transcribe this information, we need a model that is capable of
handling these challenges and producing high-quality results.**

**One of the key challenges we face in this task is the high level of noise and low signal-to-noise ratio in the audio
recordings we're working with. This can make it difficult to accurately transcribe and translate the content of the
audio files, as the noise can obscure the words and make them harder to understand.Since the model is likely to
come across a diverse set of languages and dialects in production,a robust Zero-Shot model is the only feasible
solution. That's where OpenAI Whisper Large-V2
comes in. Whisper Large-V2 is a state-of-the-art machine learning model that has been specifically designed to excel at
handling audio files with high levels of noise and low signal-to-noise ratios. Its extensive training on a dataset of
680,000 hours of audio in 100 languages (as a point of comparison, GigaSpeech , which comes 2nd place to Whisper in
terms of training data is trained on only 44,000 hours of audio ), including non-ideal, noisy samples, has prepared it
to tackle the unique challenges of our task.**

**But the benefits of Whisper Large-V2 don't end there. It is also a zero-shot learning model, meaning that it can
perform tasks and make predictions without the need for any fine-tuning or additional training on specific
datasets.Since the model is likely to
come across a diverse set of languages and dialects in production,a robust Zero-Shot model is the ideal approach.
This makes it a highly efficient and effective choice for our needs, as we can rely on it to deliver reliable results
from the
get-go, without the need to invest time and resources into adapting it to the specifics of our task. In fact, Whisper
Large has a SOTA (state-of-the-art) performance in this type of scenario, making it the ideal model for transcribing and
translating audio files that are full of noise and contain a mix of multiple languages and dialects.**

**Whisper Large-V2 has been trained for 2.5 times more epochs than Whisper Large-V1, with SpecAugment, stochastic depth,
and BPE dropout for regularization. Other than the training procedure, the model architecture and size remained the same
as the original large model**

**Whisper is also the most robust model for dataset with uncommon words as show in the last picture making it the best
choice
for transcribing and translating slang`s. Quoting the official paper "The results show that Whisper performs better than the compared models on most datasets,
especially on the  dataset which are heavy with
uncommon words."**

**But why did we choose the large-v2 version of Whisper instead of the medium or small models? The answer is simple: the
large version provides the best
balance of accuracy and speed for our needs. While the medium and small models may be able to handle some tasks
required for this challenge, they don't offer the same level of proficiency as the large model. Plus, the large model is
able to run efficiently on a GPU, making it a convenient and resource-saving choice. Overall, OpenAI Whisper Large-V2 is
an excellent choice for our task of transcribing and translating audio recordings. Its
extensive training, zero-shot learning capabilities, and proficiency in handling multiple languages make it well-suited
to the novel challenges of this task, and its large size ensures that it delivers the best possible balance of
accuracy and speed. We can trust Whisper Large-V2 to deliver reliable, high-quality results efficiently and effectively,
making
it the ideal model for this challenge**

# Core Features:
* Importing File Type (Supports Mainly .Wav, .mp3 Files)
* Number Of Channels.
* Audio Frame Rate.
* Represent The Audio Wave Form For Both Original And Modified Files.
* Audio File Duration.
* Show A History Of Previous Modified Audio Files.
* The Ability To Play Both Audio Files.
* Text To Speach Functionality [Future Upgradation]
* Convolution Operations For Some Elementary Signals [Softmax Function]
* Support For Stereo Audio Files.
* Support Dark Mode Theme.
* Proper Console ProgressBar for Analyze the Processes.
* Preview Transcript Window [Text Extract from Audio]
* Multi-language Converting Support.
* 9 Types NLP Filters To Apply On Transcript.
* Downloadable Text From Same Window Only.
* Always Access To Previous.
* .exe With CMD Support To Have look On Console Output.

# Project Creators
* Vivek Malam [Designer & Analyst]
* Dhiraj Mepani [Developer]
* Dhrumil Shah [Testing & Presentation]
