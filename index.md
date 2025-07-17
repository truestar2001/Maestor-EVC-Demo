---
layout: default
---

## Abstract
Emotional voice conversion (EVC) aims to modify the emotional style of speech while preserving its linguistic content. In practical EVC, controllability, the ability to independently control speaker identity and emotional style using distinct references, is crucial. However, existing methods often struggle to fully disentangle these attributes and lack the ability to model fine-grained emotional expressions such as temporal dynamics. We propose Maestro-EVC, a controllable EVC framework that enables independent control of content, speaker identity, and emotion by effectively disentangling each attribute from separate references. We further introduce a temporal emotion representation and an explicit prosody modeling with prosody augmentation to robustly capture and transfer the temporal dynamics of the target emotion, even under prosody mismatched conditions. Experimental results confirm that Maestro-EVC achieves high-quality, controllable, and emotionally expressive speech synthesis.

<div align="center">
  <img src="./image/figure1.png" alt="My Logo" width="500"/>
  <img src="./image/figure2.png" alt="My Logo" width="800"/>
</div>

## Demo
### 1. Compare with Baseline Models
| Col1 | Col2 | Col3 | Col4 | Col5 | Col6 |
|------|------|------|------|------|------|
| <audio controls src="audio/1-1.mp3"></audio> | <audio controls src="audio/1-2.mp3"></audio> | <audio controls src="audio/1-3.mp3"></audio> | <audio controls src="audio/1-4.mp3"></audio> | <audio controls src="audio/1-5.mp3"></audio> | <audio controls src="audio/1-6.mp3"></audio> |
| <audio controls src="audio/2-1.mp3"></audio> | <audio controls src="audio/2-2.mp3"></audio> | <audio controls src="audio/2-3.mp3"></audio> | <audio controls src="audio/2-4.mp3"></audio> | <audio controls src="audio/2-5.mp3"></audio> | <audio controls src="audio/2-6.mp3"></audio> |
| <audio controls src="audio/3-1.mp3"></audio> | <audio controls src="audio/3-2.mp3"></audio> | <audio controls src="audio/3-3.mp3"></audio> | <audio controls src="audio/3-4.mp3"></audio> | <audio controls src="audio/3-5.mp3"></audio> | <audio controls src="audio/3-6.mp3"></audio> |
| <audio controls src="audio/4-1.mp3"></audio> | <audio controls src="audio/4-2.mp3"></audio> | <audio controls src="audio/4-3.mp3"></audio> | <audio controls src="audio/4-4.mp3"></audio> | <audio controls src="audio/4-5.mp3"></audio> | <audio controls src="audio/4-6.mp3"></audio> |
### 2. Unseen Emotion
### 3. Unseen Speaker
### 4. Emotion reference variation with consistent content and speaker
