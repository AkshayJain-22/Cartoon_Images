# Cartoon_Images
This project was teeny tiny attempt to generate cartoon face images from real images using encoder-decoder architecture.
#### Try this [Demo App](https://huggingface.co/spaces/Akshay-2211/face-cartoonizer)
## About the dataset
- We took 20k real images and toonified it using a commercially available tool which gave satisfactory results.
- The datset required cleaning as some images were not up to the standards and some required appropriate cropping.
- Since Deep learning models are data hungry, we used image augmentations to genrate 1 Lakh real-cartoon pairs.
- Below is a sample of a few such augmented pairs

<img width="256" height="256" alt="yuzvendra_chahal_aug_1" src="https://github.com/user-attachments/assets/61ba4843-e8a2-4ed5-8642-bfad87498f79" /><img width="256" height="256" alt="yuvraj_singh_1_aug_5" src="https://github.com/user-attachments/assets/937b5e70-34bb-471d-8100-ecf599249e78" /><img width="256" height="256" alt="yusuf_pathan_aug_3" src="https://github.com/user-attachments/assets/388fd29e-4d20-4337-b1a9-aa6ff93446cf" />
<img width="256" height="256" alt="yuzvendra_chahal_aug_1 (1)" src="https://github.com/user-attachments/assets/1942ef1b-84d4-44c9-acc5-68a846fd98f9" />
<img width="256" height="256" alt="yuvraj_singh_1_aug_5 (1)" src="https://github.com/user-attachments/assets/7f10ca9c-68a3-434a-9c7b-62ecf021f877" />
<img width="256" height="256" alt="yusuf_pathan_aug_3 (1)" src="https://github.com/user-attachments/assets/9244c467-dd64-4b4d-82f7-1a2f6ab24e53" />

## About the model
- We trained a simple encoder-decoder model using skip connections.
- The model started showing good results even at early epochs.
- Here is a growth sample after 400 epochs.

<img width="384" height="322" alt="epoch_3" src="https://github.com/user-attachments/assets/43123ac5-2943-4389-b1c2-30fbada8cb2c" /><img width="390" height="328" alt="epoch_382" src="https://github.com/user-attachments/assets/a4af7ddf-a2cd-4de4-ac57-0fed3cdea948" />

## The Loss Graph
- The generator loss kept decreasing with increasing epoch and the quality of images improved linearly.
- The model was trained further after adjusting the hyperparameters for production applications.

<img width="693" height="425" alt="Generator Loss vs  Epoch" src="https://github.com/user-attachments/assets/6fcbaed7-1cd5-48fe-81d1-b496cdf5f589" />
