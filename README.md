# RecycleRight
RecycleRight is an innovative app powered by cutting-edge AI technology that instantly identifies and provides accurate recycling instructions based on a photo of any waste item. Simply snap a picture of the item, upload your corresponding locale information, and RecycleRight will guide you on how to properly dispose of or recycle it.

## Project Team
This project originates from a capstone project prepared for the Master of Information and Data Science (MIDS) of UC Berkeley. Members of the capstone project team:
- Anne Deforge: adeforge@berkeley.edu
- Ibrahim Shareef: ibrahim.shareef@berkeley.edu
- Jacqueline Lam: jacq@berkeley.edu
- Summer Mcgrogan: summermcgrogan@berkeley.edu

Feel free to contact us if you have any questions or comments. 

## Folder Structure

### 0_dataset
- Train data with 6 classes of waste item images extracted from [Kaggle: Recyclable and Household Waste Classification](https://www.kaggle.com/datasets/alistairking/recyclable-and-household-waste-classification) and [Portland State University: Recycling Dataset](https://web.cecs.pdx.edu/~singh/rcyc-web/index.html).
- Test data with 11 classes of waste item images taken by the project team.
  
### 1_waste_item_classification
- Baseline model on identifying waste item using ResNet
- Multi-modal LLM fine-tuning work on LLaVA 1.5 using LoRA
- Prompt engineering attempts on LLaVA 1.5 and LLaMA 3.2
- RAG approach to retrieve waste item class based on knowledge base

### 2_bin_classification
Based on output from stage 1 waste item classification, binary classification on whether the waste item can be recycled according to the relevant recycling guide.

### 3_instruction_generation
Based on output from stage 1 waste item classification, recycling instruction generation according to the relevant recycling guide.

### 4_web_app
End to end implementation of waste item classification, recycle vs waste bin classification and recycling instruction provision with web user interface. MVP of the capstone project.

## Acknowledgement & Citation
- [Kaggle: Recyclable and Household Waste Classification](https://www.kaggle.com/datasets/alistairking/recyclable-and-household-waste-classification): train data extraction
- [Portland State University: Recycling Dataset](https://web.cecs.pdx.edu/~singh/rcyc-web/index.html): train data extraction
- [Deep Residual Learning for Image Recognition (He et al., 2015)](https://arxiv.org/abs/1512.03385)
- [LLaVA: Large Language and Vision Assistant](https://github.com/haotian-liu/LLaVA): LLaVA 1.5 model and LoRA fine-tuning
- [meta-llama/Llama-3.2-11B-Vision-Instruct](https://huggingface.co/meta-llama/Llama-3.2-11B-Vision-Instruct)
