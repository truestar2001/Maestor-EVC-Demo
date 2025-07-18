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
The content, speaker, and emotion reference were randomly selected, and thus each may contain different content, speakers, and emotions.
### 1. Compare with Baseline Models
<table>
        <thead>
            <tr>
              <th style="width: 16.66%; text-align: center;"><strong>Content</strong></th>
              <th style="width: 16.66%; text-align: center;"><strong>Speaker</strong></th>
              <th style="width: 16.66%; text-align: center; border-right: 3px double lightgray;"><strong>Emotion</strong></th>
              <th style="width: 16.66%; text-align: center;"><strong>MaestroEVC</strong></th>
              <th style="width: 16.66%; text-align: center;"><strong>ZEST</strong></th>
              <th style="width: 16.66%; text-align: center;"><strong>StyleVC</strong></th>
            </tr>
        </thead>

        <tbody>

            <tr>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample1/Happy_0012_000934.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample1/Sad_0019_001161.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center; border-right: 3px double lightgray;"><audio src="./audio/sample1/Surprise_0020_001552.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample1/src_Happy_0012_000934.wav_spk_Sad_0019_001161.wav_emo_Surprise_0020_001552.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample1/" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample1/" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>

            <tr>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample2/Neutral_0012_000338.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample2/Surprise_0015_001565.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center; border-right: 3px double lightgray;"><audio src="./audio/sample2/Sad_0020_001310.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample2/src_Neutral_0012_000338.wav_spk_Surprise_0015_001565.wav_emo_Sad_0020_001310.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample1/" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample1/" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>
            <tr>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample3/Surprise_0014_001746.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample3/Angry_0011_000612.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center; border-right: 3px double lightgray;"><audio src="./audio/sample3/Angry_0012_000435.wav
" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample3/src_Surprise_0014_001746.wav_spk_Angry_0011_000612.wav_emo_Angry_0012_000435.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample1/" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample1/" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>
            <tr>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample4/Surprise_0015_001743.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample4/Neutral_0017_000326.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center; border-right: 3px double lightgray;"><audio src="./audio/sample4/Neutral_0017_000326
.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample4/src_Surprise_0015_001743.wav_spk_Happy_0018_001030.wav_emo_Neutral_0017_000326.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample1/" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample1/" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>
            <tr>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample5/Angry_0019_000361.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample5/Neutral_0014_000246.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center; border-right: 3px double lightgray;"><audio src="./audio/sample5/Sad_0015_001295
.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample5/src_Angry_0019_000361.wav_spk_Neutral_0014_000246.wav_emo_Sad_0015_001295.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample1/" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="./audio/sample1/" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>

        </tbody>
    </table>
   
### 2. Unseen Emotion
The inference results for three emotions not observed during training (fear, disgust, and excitement) are presented.
<table>
        <thead>
            <tr>
              <th style="width: 16.66%; text-align: center;"><strong>Content</strong></th>
              <th style="width: 16.66%; text-align: center;"><strong>Speaker</strong></th>
              <th style="width: 16.66%; text-align: center; border-right: 3px double lightgray;"><strong>Emotion</strong></th>
              <th style="width: 16.66%; text-align: center;"><strong>MaestroEVC</strong></th>
              <th style="width: 16.66%; text-align: center;"><strong>ZEST</strong></th>
              <th style="width: 16.66%; text-align: center;"><strong>StyleVC</strong></th>
            </tr>
        </thead>

        <tbody>

            <tr>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/src.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/tgt.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center; border-right: 3px double lightgray;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/Ours.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/FreeVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/YourTTS.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/VQMIVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>

            <tr>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/src.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/tgt.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center; border-right: 3px double lightgray;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/Ours.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/FreeVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/YourTTS.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/VQMIVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>

            <tr>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/src.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/tgt.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center; border-right: 3px double lightgray;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/Ours.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/FreeVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/YourTTS.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/VQMIVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>

            <tr>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/src.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/tgt.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center; border-right: 3px double lightgray;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/Ours.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/FreeVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/YourTTS.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/VQMIVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>
            <tr>
                <td style="width: 300px; text-align: center;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/src.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center; "><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/tgt.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center; border-right: 3px double lightgray;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/Ours.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/FreeVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/YourTTS.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/VQMIVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>

        </tbody>
    </table>


### 3. Unseen Speaker
The inference results for speakers not observed during training are presented.
<table>
        <thead>
            <tr>
              <th style="width: 16.66%; text-align: center;"><strong>Content</strong></th>
              <th style="width: 16.66%; text-align: center;"><strong>Speaker</strong></th>
              <th style="width: 16.66%; text-align: center; border-right: 3px double lightgray;"><strong>Emotion</strong></th>
              <th style="width: 16.66%; text-align: center;"><strong>MaestroEVC</strong></th>
              <th style="width: 16.66%; text-align: center;"><strong>ZEST</strong></th>
              <th style="width: 16.66%; text-align: center;"><strong>StyleVC</strong></th>
            </tr>
        </thead>

        <tbody>

            <tr>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/src.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/tgt.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center; border-right: 3px double lightgray;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/Ours.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/FreeVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/YourTTS.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/VQMIVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>

            <tr>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/src.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/tgt.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center; border-right: 3px double lightgray;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/Ours.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/FreeVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/YourTTS.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/VQMIVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>

            <tr>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/src.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/tgt.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center; border-right: 3px double lightgray;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/Ours.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/FreeVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/YourTTS.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/VQMIVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>

            <tr>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/src.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/tgt.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center; border-right: 3px double lightgray;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/Ours.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/FreeVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/YourTTS.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/VQMIVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>
            <tr>
                <td style="width: 300px; text-align: center;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/src.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center; "><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/tgt.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center; border-right: 3px double lightgray;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/Ours.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/FreeVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/YourTTS.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/VQMIVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>

        </tbody>
    </table>
### 4. Emotion reference variation with consistent content and speaker
The inference results obtained using emotion references that exhibit different prosodic characteristics within the same emotion category.
<table>
  <thead>
    <tr>
      <th style="width: 25%; text-align: center;"><strong>Content</strong></th>
      <th style="width: 25%; text-align: center;"><strong>Speaker</strong></th>
      <th style="width: 25%; text-align: center; border-right: 3px double lightgray;"><strong>Emotion</strong></th>
      <th style="width: 25%; text-align: center;"><strong>MaestroEVC</strong></th>
    </tr>
  </thead>

  <tbody>

    <tr>
      <td style="text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/src.wav" controls preload style="width: 100%;"></audio></td>
      <td style="text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/tgt.wav" controls preload style="width: 100%;"></audio></td>
      <td style="text-align: center; border-right: 3px double lightgray;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/Ours.wav" controls preload style="width: 100%;"></audio></td>
      <td style="text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/FreeVC.wav" controls preload style="width: 100%;"></audio></td>
    </tr>

    <tr>
      <td style="text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/src.wav" controls preload style="width: 100%;"></audio></td>
      <td style="text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/tgt.wav" controls preload style="width: 100%;"></audio></td>
      <td style="text-align: center; border-right: 3px double lightgray;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/Ours.wav" controls preload style="width: 100%;"></audio></td>
      <td style="text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/FreeVC.wav" controls preload style="width: 100%;"></audio></td>
    </tr>

    <tr>
      <td style="text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/src.wav" controls preload style="width: 100%;"></audio></td>
      <td style="text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/tgt.wav" controls preload style="width: 100%;"></audio></td>
      <td style="text-align: center; border-right: 3px double lightgray;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/Ours.wav" controls preload style="width: 100%;"></audio></td>
      <td style="text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/FreeVC.wav" controls preload style="width: 100%;"></audio></td>
    </tr>

    <tr>
      <td style="text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/src.wav" controls preload style="width: 100%;"></audio></td>
      <td style="text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/tgt.wav" controls preload style="width: 100%;"></audio></td>
      <td style="text-align: center; border-right: 3px double lightgray;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/Ours.wav" controls preload style="width: 100%;"></audio></td>
      <td style="text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/FreeVC.wav" controls preload style="width: 100%;"></audio></td>
    </tr>

    <tr>
      <td style="text-align: center;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/src.wav" controls preload style="width: 100%;"></audio></td>
      <td style="text-align: center;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/tgt.wav" controls preload style="width: 100%;"></audio></td>
      <td style="text-align: center; border-right: 3px double lightgray;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/Ours.wav" controls preload style="width: 100%;"></audio></td>
      <td style="text-align: center;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/FreeVC.wav" controls preload style="width: 100%;"></audio></td>
    </tr>

  </tbody>
</table>

