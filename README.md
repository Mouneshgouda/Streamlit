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
