```python
import streamlit as st
from google import genai

st.title("🤖 Gemini Chatbot")

client = genai.Client(api_key="")

if prompt := st.chat_input("Ask something..."):
    st.chat_message("user").write(prompt)

    response = client.models.generate_content(
        model="gemini-2.5-flash",
        contents=prompt
    )

    st.chat_message("assistant").write(response.text)
```
