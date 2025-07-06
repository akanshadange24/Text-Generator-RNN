🛍️ Shopping Ad Detector with RNN (PyTorch)
Ever wondered how to detect whether a piece of text sounds like an ad or not? This project does exactly that! Using a simple Recurrent Neural Network (RNN) built with PyTorch, it classifies short snippets of text into either ads or non-ads.
🔍 What It Does
This project:

Takes in short text messages (like “Buy now and save big!”)

Uses character-level patterns to learn the “language of ads”

Trains a neural network to recognize ad-like writing

Outputs predictions: Is it an ad or just regular content?

🧠 How It Works
Here’s a high-level idea of the model:

Input: Characters in the sentence (not words!)

Encoding: One-hot vectors for each character

Model: A basic RNN with 128 hidden units

Output: A probability between 0 and 1 (closer to 1 = ad)

Loss Function: Binary Cross Entropy (yes/no classification)

✨ Example Use Cases
Filter out promotional content from user comments

Detect ad-spam in scraped web pages

Preprocess data before sentiment analysis

Just for fun, see if your sentence sounds too sales-y 😉

📦 What’s in the Dataset?
We’ve created a small labeled dataset with 30 sample lines of text:

✅ 15 labeled as ads

❌ 15 labeled as non-ads

Examples:

Ad: "Limited time offer! Don’t miss out!"

Non-Ad: "This is a recipe for chocolate chip cookies."

🧪 How Well Does It Work?
After training on this tiny dataset, here’s how it performs:

makefile
Copy
Edit
Accuracy: 0.83
Precision: 0.80
Recall: 1.00
F1-score: 0.89
Pretty decent for such a small example set!

🚀 Getting Started
1. Clone this repo
bash
Copy
Edit
git clone https://github.com/yourusername/shopping-ad-rnn.git
cd shopping-ad-rnn
2. Install dependencies
bash
Copy
Edit
pip install torch scikit-learn
3. Run the model
bash
Copy
Edit
python Text_Generator_RNN.py
💬 Try It With Your Own Text
Just add this line to the script:

python
Copy
Edit
website_text = "Free shipping on all orders above $50!"
Then re-run the script. The model will tell you if your message sounds like an ad.

🔮 What’s Next?
Here’s how this could be made even cooler:

Swap RNN with LSTM or GRU for better memory

Switch to word-level input instead of characters

Train on a larger dataset (scraped ad copy, emails, etc.)

Add a frontend for real-time ad detection

📄 License
This project is open-source and licensed under the MIT License. Feel free to use, share, or tweak it for your own projects!

🙌 Credits
Made with ❤️ using PyTorch. Inspired by the idea that even ads have their own language—and we can teach machines to spot it.
