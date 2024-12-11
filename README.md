# Automatic-Music-Generation-USING-LSTM-And-Transformers
This repository presents a framework for Automatic Music Generation using Long Short-Term Memory (LSTM) and Transformer models. The project explores how deep learning can produce complex musical compositions by leveraging temporal dependencies in LSTMs and global relations in Transformers.

Overview
The system generates MIDI sequences, which are converted into audio files with the help of synthesizers. It uses a hybrid approach combining the sequential learning capabilities of LSTMs with the contextual understanding of Transformers to produce musically coherent and high-quality compositions.

Features
Sequence Modeling with LSTM: Captures temporal dependencies in MIDI sequences.
Music Refinement with Transformer: Refines synthesized music for enhanced fidelity and expressiveness.
Dataset Preprocessing: Efficient MIDI data processing to extract note and chord sequences.
Audio Synthesis: Converts MIDI files to .wav format for playback using FluidSynth.
Modular Architecture: Designed for scalability and ease of integration.

Dataset
Source: Classical MIDI dataset featuring piano compositions from renowned composers like Chopin, Schubert, and Beethoven.
Characteristics:
Dataset Size: 152 piano pieces
Format: MIDI files
Temporal Resolution: Captures timing information for note events
Methodology
Data Preprocessing:

Extract notes and chords from MIDI files.
Tokenize sequences for input-output training pairs.
Sequence Modeling:

Train a bidirectional LSTM network to learn temporal and harmonic dependencies.
Generate MIDI sequences using a dense latent space.
Music Reconstruction:

Convert generated sequences back to MIDI format.
Use music21 library for note and chord processing.
Audio Synthesis:

Use FluidSynth to convert MIDI files to high-quality .wav audio.
Music Refinement:

Refine synthesized audio with Google's Music Transformer.

Add expressive elements and smooth transitions.

Results
Improved Musical Coherence: High-quality compositions that blend long-term and short-term musical dependencies.
Metrics:

Increased tempo consistency.

Enhanced Signal-to-Noise Ratio (SNR) for clearer audio.

Dependencies

Python (>= 3.8)

TensorFlow / PyTorch (for model implementation)

music21 (for MIDI processing)

FluidSynth (for audio synthesis)

Google’s Music Transformer (for refinement)

Here is a corpus_notes file : https://drive.google.com/file/d/1fXL3DuiytKMm97wuYn_cmewrQxWpmoxi/view?usp=sharing

Here is BI-LSTM Pretrain model : https://drive.google.com/file/d/1smfMmE_TxZ0bWu12QzxuHGApnbq2_iur/view?usp=drive_link


Preprocess the data: python preprocess.py --input_path data/ --output_path processed_data/

Train the LSTM model: python train_lstm.py --data_path processed_data/ --model_path models/lstm_model.pth

Generate music: python generate_music.py --model_path models/lstm_model.pth --output_path output/

Synthesize audio: python synthesize_audio.py --midi_path output/generated_midi/ --output_path output/audio/

Refine music with Transformer: python refine_transformer.py --audio_path output/audio/ --output_path output/refined_audio/







Contributions: 
We welcome contributions from the community. Please feel free to open issues or submit pull requests.

Authors

Pratik Gunjal

Prajwal Birwadkar

Vedant Barguje


