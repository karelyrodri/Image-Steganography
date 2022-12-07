# Image Steganography
Implement and analyze performance metrics of two image steganography algorithms - LSB and F5. The evaluation of processed images will be contingent upon imperceptibility. The unperceivable or undetected change in the image after encrypting and embedding the secret message. The metrics are defined as Mean Square Error (MSE), Peak Signal to Noise Ratio (PSNR), Normalized Cross Correlation (NCC), and Structured Similarity Index Measure (SSIM).

<img width="541" alt="Image Stenography Process_larger" src="https://user-images.githubusercontent.com/106625643/206066130-11f8da49-0fa4-4d9c-af9d-d8e451670814.png">

# LSB
LSB Steganography is a spatial domain technique in which the secret message will be embedded by altering the right most bits of the RBG pixels that make up the image data. By modifying only the least significant bits, we will achieve minimal impact on the overall appearance of the image.

To strengthen the security of the LSB method, AES encryption will be applied to the secret message before embedding into the image.

![aes lsb](https://user-images.githubusercontent.com/106625643/206065509-66f77849-b949-4037-ac91-d879d91e532d.png)

# F5
F5 Image Steganography algorithm is a transform domain technique incorporating matrix encoding of the secret message. This method follows JPEG compression techniques (DCT and Quantization) to reach the frequency domain for the encoding process. The algorithm produces a new shuffling key based off the original inputted key in which generates the pseudo-random path of the shuffled coefficients. F5 relies on shuffling to achieve Permutation Straddling which scatters the image changes of the secret message uniformly throughout. The message bits get embedded by following the matrix encoding algorithm in which results in the least changes to the non-zero DCT coefficients. F5 completes the JPEG compression step and promptly uncompresses the image to output the final steganographic image.
### F5 Encryption 
![F5_encryption](https://user-images.githubusercontent.com/106625643/206066350-c8965791-f251-429b-bba9-3b286af61c36.png)

### F5 Decryption
![F5_decryption](https://user-images.githubusercontent.com/106625643/206066423-0085470e-148f-45ba-a8b8-cab773497124.png)


## Metrics

![Metrics](https://user-images.githubusercontent.com/106625643/206067026-81398f36-ae65-4040-a60c-d4608acfcdac.png)

