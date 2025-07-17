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
<table>
        <thead>
            <tr>
              <th style="width: 16.66%; text-align: center;"><strong>Content</strong></th>
              <th style="width: 16.66%; text-align: center;"><strong>Speaker</strong></th>
              <th style="width: 16.66%; text-align: center;"><strong>Emotion</strong></th>
              <th style="width: 16.66%; text-align: center; border-right: 3px solid black;"><strong>MaestroEVC</strong></th>
              <th style="width: 16.66%; text-align: center;"><strong>ZEST</strong></th>
              <th style="width: 16.66%; text-align: center;"><strong>StyleVC</strong></th>
            </tr>
        </thead>

        <tbody>

            <tr>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/src.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/tgt.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/Ours.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/FreeVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/YourTTS.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p227_044&tgt;p300_388/VQMIVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>

            <tr>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/src.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/tgt.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/Ours.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/FreeVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/YourTTS.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p240_246&tgt;p335_399/VQMIVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>

            <tr>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/src.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/tgt.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/Ours.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/FreeVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/YourTTS.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p246_092&tgt;p241_354/VQMIVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>

            <tr>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/src.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/tgt.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/Ours.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/FreeVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/YourTTS.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/MOS/VCTK/src;p232_410&tgt;p308_187/VQMIVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>
            <tr>
                <td style="width: 300px; text-align: center;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/src.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/tgt.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/Ours.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/FreeVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/YourTTS.wav" controls="" preload="" style="width: 100%;"></audio></td>
                <td style="width: 300px; text-align: center;"><audio src="all/SMOS/VCTK/src;p228_268&tgt;p275_061/VQMIVC.wav" controls="" preload="" style="width: 100%;"></audio></td>
            </tr>

        </tbody>
    </table>
   
### 2. Unseen Emotion
### 3. Unseen Speaker
### 4. Emotion reference variation with consistent content and speaker
