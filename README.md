# Audio Syllable Segmentation

## Overview

This project is designed to segment audio into syllables. It follows a series of steps from transcription to segmentation and concatenation, resulting in a syllable-segmented audio file.

## Steps

- **Audio Transcription**: Uses OpenAI's Whisper model to transcribe audio.
- **Audio Preprocessing**: Sets boundaries for audio metrics such as sample rate, bit rate, and padding.
- **Time Alignment**: Utilizes Montreal Forced Aligner to align orthographic and phonological forms with audio.
- **Phoneme Extraction**: Extracts time-stamped phonemes from the audio using Parselmouth.
- **Syllable Detection**: Identifies syllables based on phoneme vowels and language logic.
- **Audio Segmentation**: Segments audio into syllables and exports them as separate files.
- **Audio Concatenation**: Adds silence between each syllable and concatenates the segmented audio files into one.

## Steps

### 1. Transcribe the Audio
The audio is transcribed using OpenAI's Whisper, a Transformer-based encoder-decoder model. Whisper is trained on 680k hours of labeled speech data annotated using large-scale weak supervision.

### 2. Set Audio Metrics Boundaries
Set boundaries for audio metrics such as sample rate, bit rate, and padding to ensure consistency and quality.

### 3. Time Alignment with Montreal Forced Aligner (MFA)
Use MFA to align orthographic and phonological forms from a pronunciation dictionary to orthographically transcribed audio files. This step involves using both the transcribed text and the audio file.

### 4. Extract Phonemes with Parselmouth
With the time-stamped transcription file, use Parselmouth to extract time-stamped phonemes from the audio file.

### 5. Determine Syllables
Create a program to identify syllables by analyzing phoneme vowels and applying language logic. Export these syllables into separate audio files.

### 6. Concatenate Segmented Audio
Add silence between each syllable and concatenate the segmented audio files to create one syllable-segmented audio file.

## Requirements

- Python 3.7+
- OpenAI Whisper
- Montreal Forced Aligner
- Parselmouth
- Pydub
