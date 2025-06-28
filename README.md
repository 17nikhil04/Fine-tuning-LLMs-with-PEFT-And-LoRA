#PEFT & LoRA Fine-Tuning on LLaMA-2 using Hugging Face Transformers

This repository showcases an implementation of Parameter-Efficient Fine-Tuning (PEFT) using LoRA (Low-Rank Adaptation) on the LLaMA-2-7b large language model. It is designed for NLP practitioners and ML enthusiasts interested in fine-tuning large models with limited compute resources.

Project Objectives

Demonstrate the use of PEFT to efficiently fine-tune LLaMA-2

Apply LoRA adapters to reduce memory usage while maintaining performance

Generate text using the fine-tuned model

Project Workflow

1. Environment Setup

Imported essential libraries: transformers, datasets, peft, bitsandbytes, accelerate

Utilized 4-bit model loading for memory efficiency

2. Dataset Preparation

Loaded timdettmers/openassistant-guanaco from Hugging Face

Tokenized and processed inputs with EOS tokens for sequence completion

3. Model Loading

Loaded meta-llama/Llama-2-7b-hf with quantized 4-bit weights

Customized tokenizer for padding and special tokens

4. LoRA Configuration

Applied LoRA using the peft library with the following setup:

r = 16

lora_alpha = 16

target_modules = ["q_proj", "v_proj"]

lora_dropout = 0.05

5. Training

Used Hugging Face Trainer API

Optimized using AdamW8bit

Performed lightweight fine-tuning on limited dataset samples

6. Evaluation & Generation

Used the fine-tuned model to generate and evaluate text responses

Demonstrated task-specific learning using LoRA without full model tuning

Technologies & Libraries

Python 3.10+

Hugging Face Transformers

PEFT

BitsAndBytes (bnb)

Accelerate

Datasets

Skills Demonstrated

LLM Fine-tuning

Parameter-efficient modeling (PEFT)

Low-resource NLP training using LoRA

4-bit quantization & optimization

NLP pipeline engineering using Hugging Face tools

Use Cases

Fine-tuning LLMs for domain-specific applications

Resource-efficient model training in academic or startup settings

Prototyping AI assistants, chatbots, or content generation systems

📁 Project Structure

├── peft_and_loRA.ipynb          # Colab Notebook demonstrating the workflow
├── requirements.txt             # Required packages (optional)
└── README.md                    # Project overview

Author

Nikhil NegiData Analyst 
