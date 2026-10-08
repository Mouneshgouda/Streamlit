https://meet.google.com/xpq-swch-bsq

# Streamlit

```python
import streamlit as st
from gtts import gTTS

st.title("Tamil Text to Speech")

text = st.text_input("Enter text:")

if st.button("Convert"):
    tts = gTTS(text=text, lang="ta", tld="co.in", slow=True)
    tts.save("output.mp3")
    st.audio("output.mp3")

```

```python

!pip install gradio
!pip install langchain-google-genai

import os
import getpass
import gradio as gr
from langchain_google_genai import ChatGoogleGenerativeAI

# Set API Key (Colab safe input)
if not os.environ.get("GOOGLE_API_KEY"):
    os.environ["GOOGLE_API_KEY"] = getpass.getpass("Enter Google Gemini API Key: ")

# Initialize Gemini model
model = ChatGoogleGenerativeAI(model="gemini-2.5-flash")

# Chat function
def chat_with_gemini(message, history):
    response = model.invoke(message)
    return response.content

# Create Gradio interface
demo = gr.ChatInterface(
    fn=chat_with_gemini,
    title="Gemini Chatbot",
    description="Chat with Google Gemini using LangChain + Gradio"
)

demo.launch(share=True)



```

