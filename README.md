# ChartQAPro: A More Diverse and Challenging Benchmark for Chart Question Answering

🤗[Dataset](https://huggingface.co/datasets/ahmed-masry/ChartQAPro) | 🖥️[Code](https://github.com/vis-nlp/ChartQAPro) | 📄[Paper](https://arxiv.org/abs/2504.05506v2)

![question_types_crop_3-1](https://github.com/user-attachments/assets/30449812-1efd-4947-ac44-80b52485a1db)
![Screenshot 2025-04-17 205316](https://github.com/user-attachments/assets/8d54da53-48bc-429b-ae6a-9116e7f42838)

# Evaluation Results
![Screenshot 2025-04-17 205443](https://github.com/user-attachments/assets/f8c8c71f-a1a7-48bf-b25a-adfc63902a68)


## ✅ Evaluation Instructions

To evaluate your model on **ChartQAPro**, follow the steps below:

### 1. Format Your Predictions

Save your model's predictions in a `.json` file that contains a **list of dictionaries**.  
Each dictionary should include the following keys (first three keys taken from the original huggingface dataset):

- `"Answer"`: the ground truth answer  
- `"Question Type"`: the type of the question (e.g., Factoid, MCQ, etc.)  
- `"Year"`: useful for evaluating year-based answers  
- `"prediction"`: your model’s predicted answer

#### 📝 Example Format

```json
[
  {
    "Answer": ["2016"]
    "Question Type": "Factoid",
    "Year": ["YES"]
    "prediction": "2016"
  },
  ...
]
```
### 2. Install Required Dependencies

```bash
pip install anls pandas
```

### 3. Run the Evaluation Script

```bash
python evaluate_predictions.py --predictions-file path/to/your/predictions.json
```
This will print your model’s performance across different question types and the overall score, following the official evaluation metrics used in the paper. 📊

# 💬 Contact
If you have any questions about this work, please contact **[Ahmed Masry](https://ahmedmasryku.github.io/)** using the following email addresses: **amasry17@ku.edu.tr**,  **ahmed.elmasry24653@gmail.com**, or **masry20@yorku.ca**.

# 📚 Citation
If you use ChartQAPro in your research, please cite:
```
@misc{masry2025chartqaprodiversechallengingbenchmark,
      title={ChartQAPro: A More Diverse and Challenging Benchmark for Chart Question Answering}, 
      author={Ahmed Masry and Mohammed Saidul Islam and Mahir Ahmed and Aayush Bajaj and Firoz Kabir and Aaryaman Kartha and Md Tahmid Rahman Laskar and Mizanur Rahman and Shadikur Rahman and Mehrad Shahmohammadi and Megh Thakkar and Md Rizwan Parvez and Enamul Hoque and Shafiq Joty},
      year={2025},
      eprint={2504.05506},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2504.05506}, 
}
```
