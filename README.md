# BrainHemoAid-
HemoAssist is an innovative intelligent assistance system designed specifically for patients suffering from cerebral hemorrhage. Leveraging the latest advancements in artificial intelligence, it offers real-time monitoring, diagnostic support, and treatment recommendations to enhance the therapeutic outcomes and quality of life for patients.

In this project, we have implemented the following steps to achieve intelligent assistance for the diagnosis and treatment of cerebral hemorrhage:

1. **Image Preprocessing and Hemorrhage Detection**:
   - Initially, we convert CQ500 images into a format with a slice thickness and interval of 5mm.
   - Subsequently, the bone window, brain window, and brain tissue window are merged and input into the hemorrhage detection model of Baidu's XXX project.
   - The model analyzes each layer of images to identify the probabilities of different types of hemorrhages.
   - Considering that each case comprises up to 25,035 images, we select the maximum probability value of each type of hemorrhage within a single case as the hemorrhage probability for that case.
   - Ultimately, we output the probability of each type of hemorrhage for each case.

2. **Image Segmentation and Hemorrhage Volume Calculation**:
   - The segmentation model brain-seg, trained with the hs dataset, is used to process images from cases that exceed a specific probability threshold.
   - These images are converted into nii format and input into the brain-seg model for precise segmentation.
   - The model can output the specific location and volume of each type of hemorrhage.

3. **Generation of Treatment Recommendations**:
   - The location and volume data of the hemorrhage for the specified cases, generated by the aforementioned models, are input into the GPT model.
   - The GPT model generates detailed examination and treatment recommendations.
   - The specific prompt words and parameter settings are referenced from the relevant literature.

Through this series of steps, we can provide physicians with accurate hemorrhage detection results, precise information on the location and volume of hemorrhages, and treatment recommendations based on the latest research, thereby improving the efficiency and accuracy of the diagnosis and treatment of cerebral hemorrhage.

