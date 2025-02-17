Automatic Music Generation Framework.

This repository presents a framework for Automatic Music Generation using Long Short-Term Memory (LSTM) and Transformer models. This project demonstrates how deep learning can create complex musical compositions by leveraging temporal dependencies in LSTMs and global contextual understanding in Transformers.

Overview

This system generates MIDI sequences and converts them into audio files using synthesizers. It combines LSTM's sequential learning capabilities with the contextual strengths of Transformers to produce musically coherent and high-quality compositions.

Features

Sequence Modeling with LSTM: Captures temporal dependencies in MIDI sequences.
Music Refinement with Transformer: Enhances synthesized music for greater fidelity and expressiveness.
Dataset Preprocessing: Extracts note and chord sequences efficiently.
Audio Synthesis: Converts MIDI files to .wav format using FluidSynth.
Modular Architecture: Designed for scalability and ease of integration.

Dataset

Source: Classical MIDI dataset featuring piano compositions by composers such as Chopin, Schubert, and Beethoven.

Characteristics:

Dataset Size: 152 piano pieces

Format: MIDI files

Temporal Resolution: Captures precise timing information for note events

Methodology

1. Data Preprocessing
Extract notes and chords from MIDI files.
Tokenize sequences to prepare input-output training pairs.

2. Sequence Modeling
Train a Bidirectional LSTM network to learn temporal and harmonic dependencies.
Generate MIDI sequences leveraging a dense latent space.

3. Music Reconstruction
Convert generated sequences back to MIDI format.
Use the music21 library for note and chord processing.

4. Audio Synthesis
Convert MIDI files into high-quality .wav audio using FluidSynth.

5. Music Refinement
Refine synthesized audio using Google’s Music Transformer.
Adds expressive elements.
Smoothens transitions between notes.

Results
Improved Musical Coherence: Produces high-quality compositions blending long-term and short-term musical dependencies.

Metrics:
Increased tempo consistency.
Enhanced Signal-to-Noise Ratio (SNR) for clearer audio.
Dependencies

Ensure you have the following installed:

Python (>= 3.8)
TensorFlow or PyTorch (for model implementation)
music21 (for MIDI processing)
FluidSynth (for audio synthesis)
Google’s Music Transformer (for music refinement)

Usage

1. Preprocess the Data
bash
Copy code
python preprocess.py --input_path data/ --output_path processed_data/  

2. Train the LSTM Model
bash
Copy code
python train_lstm.py --data_path processed_data/ --model_path models/lstm_model.pth  

3. Generate Music
bash
Copy code
python generate_music.py --model_path models/lstm_model.pth --output_path output/  

4. Synthesize Audio
bash
Copy code
python synthesize_audio.py --midi_path output/generated_midi/ --output_path output/audio/  

5. Refine Music with Transformer
bash

Copy code

python refine_transformer.py --audio_path output/audio/ --output_path output/refined_audio/  
Resources

Corpus Notes File : https://drive.google.com/file/d/1fXL3DuiytKMm97wuYn_cmewrQxWpmoxi/view?usp=sharing

BI-LSTM Pretrained Model: https://drive.google.com/file/d/1smfMmE_TxZ0bWu12QzxuHGApnbq2_iur/view?usp=drive_link

Contributions

We welcome contributions from the community! Feel free to open issues or submit pull requests to improve this framework.

Authors

Pratik Gunjal
Prajwal Birwadkar
Vedant Barguje
