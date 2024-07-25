# Fine-Tuning a Multimodal LLM

## Description
In this project the QLoRA technique is used to fine-tune a pre-trained multimodal LLM from Hugging Face called IDEFICS-9B. The LLM is fine-tuned on a dataset consisting of Pokemon related images and texts. Before, when inferred with Pokemon related text/image prompts the pre-trained model demonstrated a very limited knowledge as it could only give the name of the Pokemon in the image. After training on new data, when inferred with Pokemon related text/image the model demonstrated a much deeper understanding of Pokemon including their type, HP, rarity, etc.

## Fine-tuning
To prepare the pre-trained LLM for training it is quantized to 4-bit precision for efficiency. LoRA (Low Rank Adaptation) is then applied to enhance the models adaptability towards new data.

## Image Pre-Processing
Pre-processing carried out on the image dataset included random resized cropping (to prevent overfitting), normalisation of pixel values, and converting images to RGB format if they are not already in RGB format.

## Output
Before fine-tuning, when inferred with unseen Pokemon related image/text prompts the pre-trained model generated a very limited knowledge as it could only give the name of a Pokemon. After training on the new data, when inferred with unseen prompts the model generated a much deeper understanding of Pokemon including their type, HP, rarity, etc.

## Conclusion
The fine-tuned LLM demonstrates enhanced knowledge of Pokemon compared to its initial state. This project showcases the training of multimodal models on domain-specific datasets to improve their performance in specific tasks. Larger datasets and further fine-tuning will likely yield even better results in the models ability to understand Pokemon.
