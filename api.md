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


## Groq

```python
import streamlit as st
from groq import Groq

st.title("🤖 Groq Chatbot")

client = Groq(api_key="YOUR_GROQ_API_KEY")

if prompt := st.chat_input("Ask something..."):
    st.chat_message("user").write(prompt)

    response = client.chat.completions.create(
        model="llama-3.3-70b-versatile",
        messages=[
            {"role": "user", "content": prompt}
        ]
    )

    st.chat_message("assistant").write(
        response.choices[0].message.content
    )

```


