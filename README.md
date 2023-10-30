# StyleLipSync — Unofficial PyTorch Implementation

Unofficial Implementation of StyleLipSync: Style-based Personalized Lip-sync Video Generation. 
Additional explanation.

![image](https://github.com/kyugorithm/StyleLipSync/assets/40943064/b9e2cac7-7740-42f5-a1ed-f9374e50a803)


# TO-DO
The recent item is sorted upper side.  
### <code>On-going</code>   **StyleGAN2 Setting**  
I use pre-trained StyleGAN2 model of [rosinality/stylegan2-pytorch](https://github.com/rosinality/stylegan2-pytorch) which is 550k trained using FFHQ dataset.

### <code>On-going</code>   **StyleLipSync Implementation**  
I implement same architecture of StyleLipSync model follows [original paper](https://stylelipsync.github.io/)  
1) Generator with SaMF
2) Encoders(face, ref, aud)

### <code>On-going</code>   **Unseen Face Adaptation**  
I implement same architecture of StyleLipSync model follows [original paper](https://stylelipsync.github.io/)  

### <code>On-going</code>   **Test for HDTF dataset**  
I test the result using HDTF(Cross-ID) for 300 videos

### <code>2023/10/30</code>   **Pose-aware Masking**  
I use same 3D face reconstruction model but implement different way.  
My pipeline consists of the following steps: Estimate 3D parameters and vertices -> Extract Open/Close mesh by adjusting expression parameters -> Normalize to a neutral pose -> Remove points where (y >= 0) -> Revert to the original estimated pose and project to 2D.
