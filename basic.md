# My First Streamlit App

```python
import streamlit as st

st.title("My First Streamlit App")

name = st.write("Enter your name")
```

# 1. Display content
```python
st.title("My App")
st.header("Users")
st.subheader("Details")

st.write("Hello!")

st.markdown("**Hello World**")

st.code("print('Hello')")

```
# 2. User input
```python
name = st.text_input("Name")

age = st.number_input("Age")

gender = st.selectbox(
    "Gender",
    ["Male", "Female", "Other"]
)

agree = st.checkbox("I agree")

if st.button("Submit"):
    st.success("Submitted!")
```

# 3. Layout

```python
col1, col2 = st.columns(2)

with col1:
    st.write("Left side")

with col2:
    st.write("Right side")
```


# 4. State
```python
import streamlit as st

count = st.number_input("Count", value=0)

if st.button("Increase"):
    count += 1

st.write(count)

```

# Forms
``` python
import streamlit as st

with st.form("my_form"):
    name = st.text_input("Name")
    age = st.number_input("Age")
    submit = st.form_submit_button("Submit")

if submit:
    st.write("Name:", name)
    st.write("Age:", age)
```
# 6. Data
```python
import pandas as pd
import streamlit as st

df = pd.DataFrame({
    "Name": ["A", "B", "C"],
    "Age": [20, 25, 30]
})

st.dataframe(df)

```

```python
import streamlit as st
import plotly.express as px

data = {
    "Product": ["Laptop", "Phone", "Tablet", "Watch"],
    "Sales": [50, 80, 30, 40]
}

# Bar Chart
fig = px.bar(data, x="Product", y="Sales", title="Product Sales")
st.plotly_chart(fig)

# Pie Chart
fig = px.pie(data, names="Product", values="Sales", title="Sales Distribution")
st.plotly_chart(fig)

# Line Chart
fig = px.line(data, x="Product", y="Sales", title="Sales Trend")
st.plotly_chart(fig)

# Scatter Plot
fig = px.scatter(data, x="Product", y="Sales", title="Sales Relationship")
st.plotly_chart(fig)
```
