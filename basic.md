# 🚀 A Beginner's Guide to Streamlit

> **Last Updated:** 3 October 2026

---

## 📌 What is Streamlit?

Streamlit is an open-source Python framework used to build interactive web applications for **data science, machine learning, and AI**.

It provides Python APIs for:

* Creating user interfaces
* Displaying data
* Visualizing results
* Accepting user input

You can build applications without writing separate frontend code.

### Commonly Used For

* 📊 Data dashboards
* 🤖 Machine learning applications
* 📈 Data visualization tools
* 🧠 AI and LLM applications
* 🔎 Interactive analytical applications

---

# 📦 Installation

Before using Streamlit, make sure **Python** and **pip** are installed on your system.

Install Streamlit using:

```bash
pip install streamlit
```

To check whether Streamlit is installed correctly:

```bash
streamlit hello
```


This starts a sample Streamlit application in the browser.

---

# 🏗️ Creating a Streamlit Application

A Streamlit application is generally written in a Python file.

The `streamlit` package is commonly imported using the alias `st`.

## Example

```python
import streamlit as st

st.title("GeeksforGeeks")
st.write("Welcome to Streamlit!")
```

## ▶️ Run the Application


Run the application using:

```bash
streamlit run file_name.py
```

## Output

<img width="839" height="349" alt="image" src="https://github.com/user-attachments/assets/abf81a1f-ad22-42f1-8890-1250ce06d21d" />


## Explanation

* `st.title()` displays the main heading of the application.
* `st.write()` displays text and other supported Python objects.
* Streamlit converts these function calls into elements displayed in the browser.
* `streamlit run file_name.py` starts the Streamlit application.

---

# 📝 Text Elements in Streamlit

Streamlit provides different functions for displaying text and formatted content.

The most commonly used text elements include:

* Titles
* Headers
* Markdown
* Captions
* Plain text
* Code blocks

---

## 1. `st.title()`

The `st.title()` function is used to display the main title of an application.

### Syntax

```python
st.title(body)
```

### Example

```python
import streamlit as st

st.title("Student Dashboard")
```

### Output

<img width="839" height="349" alt="image" src="https://github.com/user-attachments/assets/c4bc4d1b-fd21-480f-9aef-841e249e6a29" />


### Explanation

* `st.title()` displays the specified text using title formatting.
* It is generally used for the main heading of an application.

---

## 2. `st.header()`

The `st.header()` function is used to create a major section heading.

### Syntax

```python
st.header(body)
```

### Example

```python
import streamlit as st

st.header("Student Information")
```

### Output



### Explanation

* `st.header()` displays text using header formatting.
* It is useful for dividing an application into major sections.

---

## 3. `st.subheader()`

The `st.subheader()` function creates a smaller heading for a subsection.

### Syntax

```python
st.subheader(body)
```

### Example

```python
import streamlit as st

st.subheader("Academic Details")
print("GFG")
```

### Output

<img width="839" height="349" alt="image" src="https://github.com/user-attachments/assets/c6aedfec-d0b7-4662-8e99-de79bb0a8af7" />


### Explanation

* `st.subheader()` creates a subsection heading.
* It is useful for organizing content below a header.

---

## 4. `st.write()`

The `st.write()` function is a general-purpose method for displaying content in a Streamlit application.

It can display:

* Text
* Numbers
* Data structures
* DataFrames
* Supported chart objects

### Syntax

```python
st.write(*args, **kwargs)
```

### Example

```python
import streamlit as st

st.write("Welcome to Streamlit")
st.write(100)
```

### Output

<img width="839" height="349" alt="image" src="https://github.com/user-attachments/assets/b32a993d-a908-4fd3-9ffe-64a82032084c" />


### Explanation

* `st.write()` determines how supported objects should be rendered.
* It can be used for displaying many different types of content.
* More specific functions can be used when a particular display format is required.

---

## 5. `st.markdown()`

The `st.markdown()` function displays text using Markdown formatting.

### Syntax

```python
st.markdown(body)
```

### Example

```python
import streamlit as st

st.markdown("# Streamlit")
st.markdown("**Interactive Python Applications**")
```

### Output

<img width="839" height="349" alt="image" src="https://github.com/user-attachments/assets/ffc24ab7-0cbf-475f-8808-9fe62553fd49" />


### Explanation

* Markdown syntax can be used to format the displayed content.
* It can be used for headings, emphasis, lists, and links.

---

## 6. `st.caption()`

The `st.caption()` function displays smaller supporting text.

### Syntax

```python
st.caption(body)
```

### Example

```python
import streamlit as st

st.caption("Data updated on September 8, 2026")
```

### Output

<img width="839" height="349" alt="image" src="https://github.com/user-attachments/assets/8a664914-cd0e-4498-8d8e-d82f18b03eba" />

### Explanation

* `st.caption()` displays text in a smaller caption style.
* It is useful for descriptions, notes, and supporting information.

---

## 7. `st.code()`

The `st.code()` function displays code in a formatted code block.

### Syntax

```python
st.code(body, language=None)
```

### Example

```python
import streamlit as st

code = """
x = 10
y = 20
print(x + y)
"""

st.code(code, language="python")
```

### Output

<img width="839" height="349" alt="image" src="https://github.com/user-attachments/assets/dcb8a9a5-29cd-4a06-a401-b62bbf48505e" />


### Explanation

* `st.code()` renders the supplied code as a code block.
* The `language` argument can be used for syntax highlighting.

---

# 📊 Displaying Data

Streamlit provides dedicated functions for displaying:

* DataFrames
* Tables
* Metrics
* Structured data

---

## 1. `st.dataframe()`

The `st.dataframe()` function displays data as an interactive table.

### Syntax

```python
st.dataframe(data)
```

### Example

```python
import streamlit as st
import pandas as pd

data = {
    "Name": ["Aman", "Riya", "Karan"],
    "Marks": [85, 92, 78]
}

df = pd.DataFrame(data)

st.dataframe(df)
```

### Output

<img width="839" height="349" alt="image" src="https://github.com/user-attachments/assets/cbeef9bb-807d-48b5-b526-561dccfaff04" />


### Explanation

* A Pandas DataFrame is created using the sample data.
* `st.dataframe()` renders the DataFrame as an interactive table.
* This makes it suitable for exploring tabular data inside the application.

---

## 2. `st.json()`

The `st.json()` function displays a dictionary or JSON-compatible object in a formatted JSON representation.

### Syntax

```python
st.json(body)
```

### Example

```python
import streamlit as st

data = {
    "name": "Aman",
    "age": 22,
    "skills": ["Python", "SQL"]
}

st.json(data)
```

### Output

<img width="851" height="425" alt="image" src="https://github.com/user-attachments/assets/3bd87e4b-d994-46da-a84e-1b0415a518ef" />


### Explanation

* The dictionary is passed directly to `st.json()`.
* Streamlit displays the object in a formatted JSON view.

---

# 📈 Creating Charts

Streamlit includes simple chart functions for quickly visualizing data.

It also supports visualization libraries such as:

* Matplotlib
* Altair
* Plotly
* PyDeck

---

## 1. Line Chart

The `st.line_chart()` function creates a line chart.

### Syntax

```python
st.line_chart(data)
```

### Example

```python
import streamlit as st
import pandas as pd

data = pd.DataFrame({
    "Sales": [100, 150, 130, 200]
})

st.line_chart(data)
```

### Output

<img width="851" height="425" alt="image" src="https://github.com/user-attachments/assets/8d458dc9-bd26-49ed-8c1e-bdbc65bef93b" />


### Explanation

* Sales values are stored in a Pandas DataFrame.
* `st.line_chart()` plots the values as a line chart.
* Line charts are useful for showing changes or trends.

---

## 2. Bar Chart

The `st.bar_chart()` function displays data using bars.

### Syntax

```python
st.bar_chart(data)
```

### Example

```python
import streamlit as st
import pandas as pd

data = pd.DataFrame({
    "Product": ["A", "B", "C"],
    "Sales": [120, 180, 150]
})

st.bar_chart(data, x="Product", y="Sales")
```

### Output

<img width="851" height="425" alt="image" src="https://github.com/user-attachments/assets/a6d88252-37d9-421d-836a-90057c45e709" />


### Explanation

* The DataFrame contains product-wise sales.
* `x="Product"` specifies the categories.
* The chart makes it easier to compare sales between products.

---

## 3. Map

The `st.map()` function displays geographic points on a map.

The input data should contain latitude and longitude information.

### Syntax

```python
st.map(data)
```

### Example

```python
import streamlit as st
import pandas as pd

data = pd.DataFrame({
    "lat": [28.6139, 19.0760],
    "lon": [77.2090, 72.8777]
})

st.map(data)
```

### Output

<img width="869" height="643" alt="image" src="https://github.com/user-attachments/assets/8372cb23-7732-4b84-8e81-3ffb1ad92e93" />


### Explanation

* The DataFrame contains latitude and longitude columns.
* Each row represents a location.
* `st.map()` plots these locations on a map.

---

# 🎛️ Input Widgets

Widgets allow users to interact with a Streamlit application.

A widget returns a value that can be assigned to a Python variable and used by the application.

---

## 1. Button

The `st.button()` function creates a button that users can click.

### Syntax

```python
st.button(label)
```

### Example

```python
import streamlit as st

if st.button("Click Me"):
    st.write("Button clicked!")
```

### Output

<img width="845" height="434" alt="image" src="https://github.com/user-attachments/assets/6a3efdd2-b4fe-4dea-9132-2612f3053b7a" />


### Explanation

* `st.button()` creates a clickable button.
* The function returns a Boolean value.
* A message is displayed when the button is clicked.

---

## 2. Checkbox

The `st.checkbox()` function creates a checkbox widget.

### Syntax

```python
st.checkbox(label)
```

### Example

```python
import streamlit as st

show_data = st.checkbox("Show Data")

if show_data:
    st.write("Data is visible.")
```

### Output

<img width="845" height="434" alt="image" src="https://github.com/user-attachments/assets/a207db32-a518-43d4-8443-84b4a2a17500" />


### Explanation

* Checkbox allows the user to select or clear an option.
* Returned value is `True` when selected and `False` otherwise.
* The value can be used in conditional logic.

---

## 3. Radio

The `st.radio()` function allows the user to choose one option from a group.

### Syntax

```python
st.radio(label, options)
```

### Example

```python
import streamlit as st

language = st.radio(
    "Choose a language",
    ["Python", "Java", "C++"]
)

st.write("Selected:", language)
```

### Output

<img width="845" height="434" alt="image" src="https://github.com/user-attachments/assets/d1c6e24a-cdad-448d-9410-c112bf9c60ff" />


### Explanation

* Supplied options are displayed as radio buttons.
* User can select one option.
* The selected value is returned and stored in `language`.

---

## 4. Select Box

The `st.selectbox()` function creates a dropdown selection widget.

### Syntax

```python
st.selectbox(label, options)
```

### Example

```python
import streamlit as st

city = st.selectbox(
    "Choose a city",
    ["Delhi", "Mumbai", "Bengaluru"]
)

st.write("Selected city:", city)
```

### Output

<img width="845" height="434" alt="image" src="https://github.com/user-attachments/assets/c678612c-c649-46ea-87ee-416854876a96" />


### Explanation

* Options are displayed in a dropdown menu.
* User selects one option.
* The selected option is returned by `st.selectbox()`.

---

## 5. Multiselect

The `st.multiselect()` function allows users to select multiple options.

### Syntax

```python
st.multiselect(label, options)
```

### Example

```python
import streamlit as st

skills = st.multiselect(
    "Choose your skills",
    ["Python", "SQL", "Machine Learning", "Power BI"]
)

st.write("Selected Skills:", skills)
```

### Output

<img width="845" height="434" alt="image" src="https://github.com/user-attachments/assets/4f318558-fbb3-4930-8974-adaf0c2c26e7" />


### Explanation

* Multiple options can be selected.
* Selected values are returned as a collection.
* It is useful when more than one choice is allowed.

---

## 6. Numerical Input

The `st.number_input()` function accepts numerical input.

### Syntax

```python
st.number_input(label, min_value, max_value)
```

### Example

```python
import streamlit as st

age = st.number_input(
    "Enter your age",
    min_value=1,
    max_value=100
)

st.write("Age:", age)
```

### Output

<img width="845" height="434" alt="image" src="https://github.com/user-attachments/assets/361578f3-dcd2-467b-8c8d-c5c6cfff8abd" />


### Explanation

* The widget accepts a numerical value.
* Minimum and maximum values can be used to restrict the allowed range.
* The entered value can be used in further calculations.

---

## 7. Text Input

The `st.text_input()` function creates a single-line text input field.

### Syntax

```python
st.text_input(label)
```

### Example

```python
import streamlit as st

name = st.text_input("Enter your name")

if name:
    st.write("Hello", name)
```

### Output

<img width="845" height="434" alt="image" src="https://github.com/user-attachments/assets/b95c4716-59e8-48ac-baef-5ff609f6bd75" />


### Explanation

* The widget accepts text entered by the user.
* Entered value is stored in `name`.
* The value can then be used by normal Python code.

---

## 8. Multiline Text Input

The `st.text_area()` function creates a multi-line text input field.

### Syntax

```python
st.text_area(label)
```

### Example

```python
import streamlit as st

message = st.text_area("Enter your message")

st.write("Message:", message)
```

### Output

<img width="845" height="434" alt="image" src="https://github.com/user-attachments/assets/017bd940-ebea-4931-8266-483ebecbaf9b" />


### Explanation

* Unlike `st.text_input()`, `st.text_area()` is intended for multiple lines of text.
* Entered text is returned by the widget.

---

## 9. Toggle

The `st.toggle()` function creates a switch that can be turned on or off.

### Syntax

```python
st.toggle(label)
```

### Example

```python
import streamlit as st

dark_mode = st.toggle("Dark Mode")

st.write("Enabled:", dark_mode)
```

### Output

<img width="845" height="434" alt="image" src="https://github.com/user-attachments/assets/eb03b60c-a2e2-410e-bec6-2fbcb0b1b528" />


### Explanation

* The widget provides an on/off selection.
* It returns a Boolean value representing the current state.

---

# 📤 Uploading Files

Streamlit provides `st.file_uploader()` for accepting files from users.

It can be used with applications that process:

* Datasets
* Images
* Other supported files

### Syntax

```python
st.file_uploader(label)
```

### Example

```python
import streamlit as st
import pandas as pd

file = st.file_uploader(
    "Upload a CSV file",
    type=["csv"]
)

if file is not None:
    df = pd.read_csv(file)
    st.dataframe(df)
```

### Output

<img width="845" height="434" alt="image" src="https://github.com/user-attachments/assets/2055ab42-0205-471e-9cf9-ceb36bb198c7" />


### Explanation

* `st.file_uploader()` creates a file-selection widget.
* The `type` argument limits the accepted file types.
* Uploaded CSV can be passed directly to Pandas.
* The resulting DataFrame is displayed using `st.dataframe()`.

---

# 📥 Downloading Files

The `st.download_button()` function provides a button that allows users to download data or files from the application.

### Syntax

```python
st.download_button(label, data)
```

### Example

```python
import streamlit as st

data = "name,marks\nAman,85\nRiya,92"

st.download_button(
    "Download CSV",
    data,
    file_name="students.csv"
)
```

### Output

<img width="845" height="434" alt="image" src="https://github.com/user-attachments/assets/cdfec7da-c837-4dbf-80a6-61b9a786d94c" />


### Explanation

* The button provides the supplied data as a downloadable file.
* `file_name` specifies the name used for the downloaded file.

---

# 🖼️ Displaying Images

The `st.image()` function displays an image in a Streamlit application.

### Syntax

```python
st.image(image)
```

### Example

```python
import streamlit as st

st.image(
    "image.png",
    caption="Sample Image"
)
```

### Output

The image will be displayed in the browser.

### Explanation

* The image is loaded from the specified source.
* The `caption` argument provides descriptive text.
* Streamlit also provides functions for displaying audio and video content.

---

# 🧱 Layouts and Containers

Streamlit provides layouts and containers to organize application elements.

Common options include:

* Columns
* Containers
* Tabs
* Expanders
* Popovers
* Sidebars

---

## 1. Columns

The `st.columns()` function creates side-by-side columns.

### Syntax

```python
st.columns(spec)
```

### Example

```python
import streamlit as st

col1, col2 = st.columns(2)

with col1:
    st.metric("Users", 1200)

with col2:
    st.metric("Revenue", "$25K")
```

### Output

<img width="845" height="434" alt="image" src="https://github.com/user-attachments/assets/23aff3bb-1b71-4806-a758-9cc20adf5807" />


### Explanation

* `st.columns(2)` creates two columns.
* Elements placed inside each column appear side by side.
* Columns are useful for dashboards containing multiple metrics or visualizations.

---

## 2. Sidebar

The sidebar provides a separate area for application controls.

### Syntax

```python
st.sidebar.element(...)
```

### Example

```python
import streamlit as st

st.sidebar.title("Filters")

category = st.sidebar.selectbox(
    "Choose Category",
    ["All", "Python", "AI"]
)

st.write("Selected:", category)
```

### Output

<img width="936" height="548" alt="image" src="https://github.com/user-attachments/assets/7c513d8a-878c-4e2d-b2ff-61b04eb6e9bc" />


### Explanation

* Streamlit elements can be placed in the sidebar.
* Sidebars are commonly used for filters and navigation controls.
* The selected value can still be used in the main application.

---

## 3. Tabs

The `st.tabs()` function creates multiple tabbed sections.

### Syntax

```python
st.tabs(tabs)
```

### Example

```python
import streamlit as st

tab1, tab2 = st.tabs([
    "Overview",
    "Details"
])

with tab1:
    st.write("Overview")

with tab2:
    st.write("Details")
```

### Output

<img width="859" height="453" alt="image" src="https://github.com/user-attachments/assets/ab178189-bee7-4548-8459-27999a05de6c" />


### Explanation

* `st.tabs()` creates separate labeled tabs.
* Content can be added to each tab using the returned objects.
* Tabs are useful for grouping related information.

---

## 4. Expander

The `st.expander()` function creates a collapsible section.

### Syntax

```python
st.expander(label)
```

### Example

```python
import streamlit as st

with st.expander("View Details"):
    st.write("Additional information is displayed here.")
```

### Output

<img width="859" height="453" alt="image" src="https://github.com/user-attachments/assets/2ce96fca-aa78-4295-968d-92b17a9babe2" />


### Explanation

* Content inside the expander can be opened or collapsed.
* It is useful for secondary information or advanced options.

---

## 5. Container

The `st.container()` function creates a container that can hold multiple elements.

### Syntax

```python
st.container()
```

### Example

```python
import streamlit as st

container = st.container()

container.write("First element")
container.write("Second element")
```

### Output
<img width="859" height="453" alt="image" src="https://github.com/user-attachments/assets/fb80a39b-4f95-4ccb-a473-0604f45d7f0f" />


### Explanation

* A container groups multiple Streamlit elements.
* Elements can be written into the same container.

---

## 6. Divider

The `st.divider()` function adds a horizontal divider between sections.

### Syntax

```python
st.divider()
```

### Example

```python
import streamlit as st

st.header("Section 1")
st.write("Content")

st.divider()

st.header("Section 2")
st.write("More Content")
```

### Output



### Explanation

* `st.divider()` inserts a horizontal line.
* It can visually separate sections of an application.

---

# ⚡ Caching in Streamlit

Streamlit reruns the script when users interact with widgets.

Expensive operations can therefore be repeated.

Caching stores the results of suitable functions so that Streamlit can reuse them instead of recomputing them unnecessarily.

Streamlit provides two main caching decorators:

* `st.cache_data` — for functions that return data.
* `st.cache_resource` — for reusable resources such as models or connections.

---

## `st.cache_data`

### Syntax

```python
@st.cache_data
def function():
    ...
```

### Example

```python
import streamlit as st
import pandas as pd

@st.cache_data
def load_data():
    return pd.read_csv("data.csv")

df = load_data()

st.dataframe(df)
```

### Explanation

* `load_data()` reads the dataset.
* `@st.cache_data` tells Streamlit to cache the returned data.
* This helps avoid repeating the same expensive data operation during reruns.

---

## `st.cache_resource`

`st.cache_resource` is designed for resources that should be reused, such as:

* Machine learning models
* Database connections
* Other reusable resources

### Syntax

```python
@st.cache_resource
def function():
    ...
```

### Example

```python
import streamlit as st

@st.cache_resource
def load_model():
    model = load_machine_learning_model()
    return model

model = load_model()
```

### Explanation

* The model is created inside the cached function.
* Streamlit can reuse the resource across reruns.
* This avoids repeatedly initializing expensive resources.

---

# 🔄 Session State in Streamlit

Streamlit reruns the script when the user interacts with a widget.

`st.session_state` allows values to be preserved between these reruns for each user's session.

### Syntax

Using dictionary-style access:

```python
st.session_state["key"]
```

Or attribute-style access:

```python
st.session_state.key
```

### Example

```python
import streamlit as st

if "count" not in st.session_state:
    st.session_state.count = 0

if st.button("Increment"):
    st.session_state.count += 1

st.write("Count:", st.session_state.count)
```

### Output

<img width="859" height="453" alt="image" src="https://github.com/user-attachments/assets/4693a0f7-dde2-4d0d-a4df-84a857fd78f6" />


### Explanation

* The counter is initialized only when it does not already exist.
* Clicking the button increases the stored value.
* The value remains available when Streamlit reruns the script.
* Session State is maintained separately for each user session.

---

# 📑 Creating Multipage Applications

Streamlit supports multipage applications, which allow a larger application to be divided into separate pages.

Modern Streamlit applications can define pages using:

* `st.Page()`
* `st.navigation()`

### Syntax

```python
pages = [
    st.Page("page1.py"),
    st.Page("page2.py")
]

pg = st.navigation(pages)

pg.run()
```

### Example

```python
import streamlit as st

pages = [
    st.Page("home.py", title="Home"),
    st.Page("dashboard.py", title="Dashboard")
]

pg = st.navigation(pages)

pg.run()
```

### Output

<img width="928" height="608" alt="image" src="https://github.com/user-attachments/assets/2dddba0e-a738-4151-8810-ed5a7b54fce8" />


### Explanation

* `st.Page()` defines the pages of the application.
* `st.navigation()` creates the navigation structure.
* `pg.run()` runs the selected page.
* Multipage applications are useful for organizing larger Streamlit projects.

---

# 🎓 Creating a Small Streamlit Application

The Streamlit components discussed above can be combined to create a simple **Student Performance Dashboard**.

## The Application Will

* Accept the student's name.
* Allow the user to select a subject.
* Accept marks using a slider.
* Display the result using a metric.
* Show a simple chart.
* Organize controls using the sidebar and columns.

---

# 💻 Complete Code

```python
import streamlit as st
import pandas as pd

# Title
st.title("Student Performance Dashboard")

# Sidebar inputs
st.sidebar.header("Student Details")

name = st.sidebar.text_input("Enter your name")

subject = st.sidebar.selectbox(
    "Select Subject",
    ["Python", "SQL", "Machine Learning"]
)

marks = st.sidebar.slider(
    "Select Marks",
    0,
    100,
    50
)

# Main content
if name:
    st.header(f"Welcome, {name}!")

    col1, col2 = st.columns(2)

    with col1:
        st.metric("Selected Marks", marks)

    with col2:
        if marks >= 50:
            st.success("Result: Pass")
        else:
            st.error("Result: Fail")

    st.subheader("Performance")

    data = pd.DataFrame({
        "Subject": ["Python", "SQL", "Machine Learning"],
        "Marks": [marks, 70, 85]
    })

    st.dataframe(data)

    st.subheader("Marks Visualization")

    st.bar_chart(
        data,
        x="Subject",
        y="Marks"
    )

else:
    st.info("Enter your name from the sidebar to view the dashboard.")
```

---

## 📸 Application Output

<img width="1910" height="872" alt="image" src="https://github.com/user-attachments/assets/d8126b52-8b9b-4e12-953f-5d6101d19f54" />


---

# 🌟 Advantages of Streamlit

### 1. Simple Development

Applications can be created primarily using Python.

### 2. Interactive

Built-in widgets allow users to interact with application data and logic.

### 3. Data-Friendly

Streamlit works directly with DataFrames and common visualization libraries.

### 4. Fast Prototyping

Data and machine learning applications can be developed without creating a separate frontend.

### 5. Built-in Optimization

Caching and Session State help handle reruns and application state.

---

# 📚 Streamlit Functions Covered

| Category       | Function               |
| -------------- | ---------------------- |
| Title          | `st.title()`           |
| Header         | `st.header()`          |
| Subheader      | `st.subheader()`       |
| General Output | `st.write()`           |
| Markdown       | `st.markdown()`        |
| Caption        | `st.caption()`         |
| Code           | `st.code()`            |
| DataFrame      | `st.dataframe()`       |
| JSON           | `st.json()`            |
| Line Chart     | `st.line_chart()`      |
| Bar Chart      | `st.bar_chart()`       |
| Map            | `st.map()`             |
| Button         | `st.button()`          |
| Checkbox       | `st.checkbox()`        |
| Radio          | `st.radio()`           |
| Select Box     | `st.selectbox()`       |
| Multiselect    | `st.multiselect()`     |
| Number Input   | `st.number_input()`    |
| Text Input     | `st.text_input()`      |
| Text Area      | `st.text_area()`       |
| Toggle         | `st.toggle()`          |
| File Upload    | `st.file_uploader()`   |
| File Download  | `st.download_button()` |
| Image          | `st.image()`           |
| Columns        | `st.columns()`         |
| Sidebar        | `st.sidebar`           |
| Tabs           | `st.tabs()`            |
| Expander       | `st.expander()`        |
| Container      | `st.container()`       |
| Divider        | `st.divider()`         |
| Data Cache     | `st.cache_data`        |
| Resource Cache | `st.cache_resource`    |
| Session State  | `st.session_state`     |
| Multipage      | `st.Page()`            |
| Navigation     | `st.navigation()`      |

---

# 🏁 Conclusion

Streamlit makes it possible to create interactive **data science, machine learning, AI, dashboard, and analytical applications using Python** without requiring a separate frontend.

By learning:

* Text elements
* Data display
* Charts
* Input widgets
* File handling
* Images
* Layouts
* Caching
* Session State
* Multipage applications

you can build complete interactive Streamlit applications using Python.

---

## 🚀 Quick Start

```bash
pip install streamlit
```

Create a Python file:

```bash
app.py
```

Add:

```python
import streamlit as st

st.title("My First Streamlit App")
st.write("Hello, Streamlit!")
```

Run:

```bash
streamlit run app.py
```

Your Streamlit application will open in the browser.
