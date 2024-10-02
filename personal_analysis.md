# Personal Analysis

In this project, I worked with a small, optimized dataset that had **400 rows and 8 numerical columns**. Given the dataset size, I expected the model to perform well, but I faced difficulties, especially because it was my first time building an **Artificial Neural Network (ANN)**. I wasn’t sure how to design the model in terms of **how many layers or neurons to use**, or **which activation functions or features** would be most effective. I also had trouble with **training the neural network** and getting good results.

## Initial Problems:
At first, the results were disappointing. I thought **multicollinearity** between the **TOEFL Score** and **GRE Score** might be causing issues, so I combined them into a single feature. This didn’t improve the results. Next, I thought the problem might be due to the **Chance of Admit** values, so I multiplied them by 100 to show them as percentages. However, this also didn’t help.

## Key Adjustments for Improvement:
After trying different things, I made several key changes that significantly improved the model's performance:

- **Simplified the Neural Network**: 
  - Since the dataset was small, I reduced the number of neurons. A smaller network is better suited for a small dataset because it helps prevent overfitting, allowing the model to learn from the data more effectively.

- **Removed Regularization (L1 and L2)**: 
  - Initially, I added L1 and L2 regularization to reduce overfitting. However, with a small dataset, this actually made the model perform worse. Removing the regularization helped improve the performance.

- **Used MinMaxScaler for Normalization**: 
  - I applied **MinMaxScaler** to normalize the dataset. This made a significant difference because normalization helps the ANN process the data more effectively.

- **Adjusted the Train-Test Split**: 
  - I set the test set size to **10%** instead of the usual 20-30%. With such a small dataset, a larger test set left too little data for training, which affected the model’s learning. Using 10% for the test set gave the model enough data to train on and improved its learning capability.

## Design Considerations:
Since this was my first ANN, I learned a lot about what I should consider when designing such models. I now realize that:
1. **Choosing the right number of layers and neurons** is critical. For small datasets, simpler models tend to work better.
2. **Choosing the right activation function** is important. I used ReLU, which worked well, but other functions like Leaky ReLU could also be worth testing.
3. **Regularization isn’t always necessary** for small datasets and can sometimes hurt model performance.
4. **Optimization**: The Adam optimizer performed well, but I could explore other optimizers or fine-tune the learning rate for better results.

## Resources I Used:
- I referred to the **lecture notes** posted on **peke.lab.fi**.
- I also used **ChatGPT** for specific coding questions and consulted **online documentation** like StackOverflow.
- For one part of the code, I asked a **friend** for advice and reached out to my **Tutor (Tuomas)** to clear up some concepts.

## Conclusion:
This project taught me a lot about building and optimizing ANN models, especially for small datasets. Although I faced difficulties in the beginning, through trial and error, I managed to improve the model by simplifying its structure, adjusting the preprocessing steps, and tuning the parameters. The experience gave me a better understanding of how to approach similar problems in the future.
