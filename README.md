**Hate Speech Auto-Deletion System**

A smart, real-time comment moderation system using AI — automatically detects
and removes hate or offensive comments from any live chat or comment section without disturbing users.

**Project Overview**

1.In many online platforms like YouTube Live, Instagram, or public chatrooms, users may post offensive or hateful comments.
2.Manually deleting such messages is difficult and time-consuming.
3.This project solves that problem by using AI-based toxicity detection to automatically filter
  and remove such comments in real time — while ensuring that normal comments remain visible to everyone.
4.It behaves just like modern social platforms:
5.If a user posts a toxic or offensive comment, it is silently deleted (not shown to others).
6.The deleted comments are privately stored in a log file (deleted_log.json) for moderator review.
7.The user is not banned or restricted, and can continue commenting.
8.The system does not print any “deleted” messages publicly — ensuring a clean and natural chat experience

🧩 Features

✅ AI-Powered Moderation — Detects toxic, obscene, hateful, or insulting language using a fine-tuned BERT model.
✅ Silent Deletion — Removes hate comments instantly, with no visible alerts or messages.
✅ Privacy Preserved — Deleted comments are logged privately for moderator access.
✅ No Usernames Needed — Works with any chat/comment input (YouTube-style behavior).
✅ Universal Use Case — Can be integrated into live chatrooms, social platforms, or feedback portals.
✅ Lightweight & Portable — Runs easily in Google Colab, Jupyter Notebook, or a local Python environment.


🧠 Model Used

The system uses the unitary/toxic-bert model from Hugging Face.
This model was trained on the Jigsaw Toxic Comment Classification Dataset, and it can detect six toxicity categories:

Label	Description

**toxic**           	General toxicity or aggression
**severe_toxic**	    Strongly toxic language
**obscene**          	Use of profanity or explicit content
**threat**            Threatening or violent content
**insult**	          Personal attacks or insults
**identity_hate**   	Hate speech toward identity group

🧠 How It Works (Step-by-Step Explanation)

1. Model Initialization
The unitary/toxic-bert model and tokenizer are loaded.
The model predicts toxicity probabilities for each of the six labels.

2. Real-Time Comment Input
Users can continuously type comments (just like a chat or comment box).
No usernames or login steps are needed.

3. Toxicity Detection
Each new comment is passed through the model.
If the probability of any toxic label exceeds the threshold (default 0.5), it’s marked as offensive.

4. Silent Moderation
Offensive comments are immediately deleted (not printed or shown to the user).
The deleted message is privately stored with a timestamp and toxicity scores in deleted_log.json.

5. Visible Comments Display
Only clean comments are displayed to the public feed (visible_comments list).
The chat updates automatically after every new comment.

📈 Possible Future Improvements

Integration with web-based UI (Gradio / Streamlit) for live visualization.

Automatic warning system to notify repeat offenders privately.

Support for multilingual toxicity detection (Hindi, Spanish, etc.).

Integration into real chat APIs or websites (YouTube Live, Discord bots, etc.).

Dashboard for moderators to analyze deleted comments and trends.



---

🧑‍💻 Author

Developed by: M.Vasudha Rani
GitHub: vasudharani.mukku06@gmail.com
