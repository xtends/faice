# iApps - from zero to hero<br />
Intelligent Agents Python Programming FAICE platform

<b><a href="https://github.com/faicey">FAICE</a> = Framework for Autonomous and Intelligent Computer Expressions</b></br>

<b>iApps = Intelligent Agent Python Programming System</a></b><br /><br /><br />

<b>Step 1: Environment Setup</b><br />

<b>create a python virtual environment</b>
```bash
python3 -m venv myenv
```
<b>activate python virtual environment</b>
```bash
source myenv/bin/activate
```

<b>Install required packages using pip</b><br />
```bash
pip install streamlit
```

<b>example run faice iApp</b>
```bash
streamlit run faice.py
```
<b>example run newfaice iApp</b>
```bash
streamlit run newfaice.py
```

<b>Step 2: Hello World</b>

Today I discovered <a href="https://streamlit.io/">Streamlit</a>. Start by creating an application in a Python file (iApp.py). I like to use notepad or gedit. Use whatever editor you like. Streamlit turns data scripts into shareable web apps blazingly fast... and with autonomous deployment well just stand back. You might not never need to read any of these notes.
All in pure <a href="https://www.python.org/">Python</a>. No front‑end experience required.
<br />

example 1: Import the Streamlit library, ask the user for a gpt API key, import a couple of encryption libraries,  and define a function to display a welcome message and start chatting with chatgpt.py click chatgpt.py for the full source code. iApp - from zero to hero<br />

<b>Step 3: Modular Design</b>

Create a separate Python file (modules.py) to organize modular code.
Move the display_hello function to modules.py.
Import display_hello from modules.py into app.py.

<b>Step 4: UI/UX/</b>

Enhance the UI by adding user input elements like buttons and text inputs.
Utilize the Streamlit functions to create user-friendly interaction.

<b>Step 5: AI Integration</b>

Integrate a basic machine learning model from your choice of models.
For instance Use CountVectorizer and Multinomial Naive Bayes classifier to implement the predict_spam function for spam prediction.

<b>Step 6: Language Model Extensions</b>

Utilize the Transformers library to add a text summarization feature.
Implement the summarize_text function for text summarization from BART

<b>Step 7: Security Best Practices</b>

Implement input validation and sanitization using regular expressions.
Use the sanitize_input function to ensure safe user inputs.

<b>Step 8: Deployment</b>

Choose a deployment platform such as AWS, GCP, or DigitalOcean.
Prepare your code for deployment by creating a requirements.txt file.
Configure a web server (Nginx or Apache) to handle requests.
Start the Streamlit app and make it accessible online.
The following code has been extracted from the official cheatsheet and is posted here to save time on rapid deployment</a><br />

<b>installation and running</b>
```bash
streamlit run your_script.py
```
<b>pre-release features -- ride the lightening</b>
```bash
pip uninstall streamlit
pip install streamlit-nightly --upgrade
```
<b>command line</b>
```bash
streamlit --help
streamlit run your_script.py
streamlit hello
streamlit config show
streamlit cache clear
streamlit docs
streamlit --version
```
<b>display text and markdown</b>
```python
st.text('Fixed width text')
st.markdown('_Markdown_')
st.latex(r''' e^{i\pi} + 1 = 0 ''')
st.write('Most objects')
st.title('My title')
st.header('My header')
st.subheader('My sub')
st.code('for i in range(8): foo()')
```
<b>data display</b>
```python
st.dataframe(my_dataframe)
st.table(data.iloc[0:10])
st.json({'foo':'bar','fu':'ba'})
st.metric('My metric', 42, 2)
```
<b>media display</b>
```python
st.image('./header.png')
st.audio(data)
st.video(data)
```
<b>buttons and controls</b>
```python
st.button('Click me')
st.checkbox('I agree')
st.toggle('Enable')
```
<b>selection widgets</b>
```python
st.radio('Pick one', ['cats', 'dogs'])
st.selectbox('Pick one', ['cats', 'dogs'])
st.multiselect('Buy', ['milk', 'apples', 'potatoes'])
```
<b>slider and input</b>
```python
st.slider('Pick a number', 0, 100)
st.select_slider('Pick a size', ['S', 'M', 'L'])
st.text_input('First name')
st.number_input('Pick a number', 0, 10)
st.text_area('Text to translate')
st.date_input('Your birthday')
st.time_input('Meeting time')
st.file_uploader('Upload a CSV')
st.camera_input("Take a picture")
st.color_picker('Pick a color')
```
<b>layout and structure</b>
```python
col1, col2 = st.columns(2)
col1.write("This is column 1")
col2.write("This is column 2")
```
<b>tabs</b>
```python
tab1, tab2 = st.tabs(["Tab 1", "Tab2"])
tab1.write("this is tab 1")
tab2.write("this is tab 2")
```
<b>control flow interaction</b>
```python
st.stop()
st.experimental_rerun()
```
<b>grouping widgets</b>
```python
with st.form(key='my_form'):
    username = st.text_input('Username')
    password = st.text_input('Password')
    st.form_submit_button('Login')
```
<b>caching data objects</b>
```python
@st.cache_data
def foo(bar):
    # Expensive computation
    return data
```
<b>caching data objects</b>
```python
@st.cache_data
def foo(bar):
    # Expensive computation
    return data
```
<b>global resource caching</b>
```python
@st.cache_resource
def foo(bar):
    # Create non-data object
    return session
```
<b>display progress and status</b>
```python
with st.spinner(text='In progress'):
    time.sleep(3)
    st.success('Done')
bar = st.progress(50)
time.sleep(3)
bar.progress(100)
with st.status('Authenticating...') as s:
    time.sleep(2)
    st.write('Some long response.')
    s.update(label='Response')
```
<b>personalization UIUX</b>
```python
if st.user.email == 'codephreak@dmg.finance':
    display_codephreak_content()
elif st.user.email == 'adamsmith@foocorp.io':
    display_adamsmith_content()
else:
    st.write("Signup here for access to great things")
```
<b>sharing url's</b>
```python
params = {'param1': value1, 'param2': value2}
st.experimental_set_query_params(**params)
```
<b>connecting to data sources</b>
```python
st.experimental_connection('database', type='sql')
conn = st.experimental_connection('sql')
```

# <b>Streamlit Custom Components Tips</b><br />

1. <b>Custom Language Model Integration</b><br />

You can create custom components that interface with local language models for tasks like sentiment analysis, translation, and summarization. Use the st.pydeck_chart component to visualize language model outputs interactively.<br /><br />
2. <b>ChatGPT Integration</b><br />

Integrate the ChatGPT API into your Streamlit app using a custom component. This allows users to have dynamic conversations with AI and obtain context-aware responses in real-time.<br /><br />
3. <b>Database API Integration</b><br />

Develop a custom component that interfaces with database APIs to fetch and display data seamlessly. This enables users to interact with and manipulate data directly within your app.<br /><br />
4. <b>User-Friendly Interfaces</b>

Design user-friendly interfaces for your custom components using intuitive widgets like buttons, sliders, and input fields. Keep the user experience streamlined and accessible.<br /><br />
5. <b>Real-Time Updates</b><br />

Enable real-time updates in custom components by integrating Streamlit's reactive framework. Ensure that changes in language models, ChatGPT responses, or database updates are reflected instantly.<br /><br />
6. <b>Progressive Loading</b><br />

Implement progressive loading for language model responses or API queries. Use placeholders and loading spinners to provide feedback while waiting for data to load.<br /><br />
7. <b>Contextual User Interactions</b><br />

Create custom components that allow users to interact contextually with AI models. For instance, trigger ChatGPT responses based on user actions or clicks.<br /><br />
8. <b>Error Handling</b><br />

Implement robust error handling in your custom components. Display clear error messages and provide users with guidance on how to proceed when unexpected issues arise.<br /><br />
9. <b>Security Considerations</b><br />

Prioritize <a href="https://en.wikipedia.org/wiki/Open-source_software_security">security</a> and integrate <a href="https://pypi.org/project/python-dotenv/">external APIs or databases</a> into <a href="https://pypi.org/project/python-dotenv/">Python-dotenv</a> or similar protection mechanisms . Ensure that sensitive data remains protected, and consider implementing <a href="https://pyjwt.readthedocs.io/en/stable/">authentication</a> and <a href="https://oauthlib.readthedocs.io/en/latest/">authorization</a> mechanisms.<br />

# #################################
# xperimental zone no promises here
# safe storage of API keys is on you
# #################################
<br />

<b>sentiment analysis</b>
```python

import streamlit as st

class SentimentAnalyzer:
    def analyze_sentiment(self, text):
        # Your sentiment analysis logic
        sentiment_score = analyze(text)
        return sentiment_score

analyzer = SentimentAnalyzer()

def main():
    st.title("Sentiment Analysis App")
    text = st.text_area("Enter text for sentiment analysis")
    
    if st.button("Analyze"):
        sentiment_score = analyzer.analyze_sentiment(text)
        st.write(f"Sentiment score: {sentiment_score}")

if __name__ == "__main__":
    main()
```
<b>chatGPT integration</b>
```python
#chatpgt.py
import streamlit as st

class ChatGPTComponent:
    def __init__(self, api_key):
        self.api_key = api_key

    def chat_with_gpt(self, message):
        # Call ChatGPT API with user message
        response = call_chatgpt_api(message, self.api_key)
        return response["message"]

api_key = "your_chatgpt_api_key"
chatgpt = ChatGPTComponent(api_key)

def main():
    st.title("Chat with codephreak-GPT4")
    user_input = st.text_input("You:", "")
    
    if st.button("Send"):
        response = chatgpt.chat_with_gpt(user_input)
        st.write("AI:", response)

if __name__ == "__main__":
    main()
```
<b>fetch and display data from a database API</b>
```python
#fetchdisplaydata.py
import streamlit as st

class DatabaseComponent:
    def fetch_data(self):
        # Fetch data from database API
        data = fetch_data_from_api()
        return data

db_component = DatabaseComponent()

def main():
    st.title("Database Viewer")
    data = db_component.fetch_data()
    
    if data:
        st.dataframe(data)
    else:
        st.write("No data available")

if __name__ == "__main__":
    main()
```
<b>creating a codephreak worthy interactive <a href="https://github.com/faicey">UIUX</a><a href="https://github.com/mlodular">mlodular</a> interface</b><br />
#interactive.py
```python
import streamlit as st

class InteractiveComponent:
    def get_user_input(self):
        user_input = st.text_input("Enter something:", "")
        return user_input

interactor = InteractiveComponent()

def main():
    st.title("Interactive App")
    user_input = interactor.get_user_input()
    st.write("You entered:", user_input)

if __name__ == "__main__":
    main()
```
<b>customizing real time updates</b>
```python
#realtime.py
import streamlit as st

class RealTimeComponent:
    def update_data(self):
        # Update data in real-time
        new_data = get_updated_data()
        return new_data

rt_component = RealTimeComponent()

def main():
    st.title("Real-Time Data Update")
    updated_data = rt_component.update_data()
    st.write("Updated Data:", updated_data)

if __name__ == "__main__":
    main()
```
<b>progressive loading</b>
```python
#progressiveloading.py
import streamlit as st
import time

class LoadingComponent:
    def load_data(self):
        st.text("Loading data...")
        time.sleep(3)
        data = fetch_data()
        return data

loader = LoadingComponent()

def main():
    st.title("Progressive Loading")
    data = loader.load_data()
    st.write("Loaded Data:", data)

if __name__ == "__main__":
    main()
```
<b>contextual interaction</b>
```python
#contexual.py
import streamlit as st

class ContextualComponent:
    def interact(self, context):
        if context == "greet":
            st.write("Hello, I am Professor Codephreak")
        elif context == "inform":
            st.write("Here's some information.")
        else:
            st.write("I'm not sure how to respond.")

contextual = ContextualComponent()

def main():
    st.title("Contextual Interaction")
    interaction_type = st.selectbox("Select interaction type:", ["greet", "inform", "other"])
    contextual.interact(interaction_type)

if __name__ == "__main__":
    main()
```
<b>error handling/<b>
```python
#errorhandling.py
import streamlit as st

class ErrorComponent:
    def perform_task(self):
        try:
            result = perform_risky_task()
            return result
        except Exception as e:
            st.error(f"An error occurred: {e}")
            return None

error_handler = ErrorComponent()

def main():
    st.title("Error Handling")
    task_result = error_handler.perform_task()
    if task_result is not None:
        st.write("Task Result:", task_result)

if __name__ == "__main__":
    main()
```
<b>security considerations skeleton ... customize to your own needs</b>
```python
#security.py
import streamlit as st

class SecureComponent:
    def perform_secure_task(self):
        secure_input = st.text_input("Enter secure input", type="password")
        # Implement secure processing here
        return secure_output

secure_processor = SecureComponent()

def main():
    st.title("Secure Processing")
    secure_result = secure_processor.perform_secure_task()
    st.write("Secure Result:", secure_result)

if __name__ == "__main__":
    main()
```
<b>provide comprehensive documentation for custom components to guide users</b>
```python
import streamlit as st

class DocumentationComponent:
    def display_documentation(self):
        st.markdown("# Custom Component Documentation")
        st.write("This is a detailed guide on how to use this component.")
        st.code("class DocumentationComponent:\n    def display_documentation(self):\n        # Documentation content")

doc_component = DocumentationComponent()

def main():
    st.title("Custom Component Documentation")
    doc_component.display_documentation()

if __name__ == "__main__":
    main()
```
<b>add some style</b>
```python
import streamlit as st

class StyledComponent:
    def show_styled_content(self):
        st.markdown('<style>body { background-color: #f0f0f0; }</style>', unsafe_allow_html=True)
        st.title("Stylish App")
        st.write("This app has a customized background color.")

styler = StyledComponent()

def main():
    styler.show_styled_content()

if __name__ == "__main__":
    main()
```
<b>add some <a href="https://github.com/webmindml/DDD.ddd">DDD</a> 3D interactive elements using <a href="https://threejs.org/docs/index.html#manual/en/introduction/Creating-a-scene">three.js</a></b>
```python
import streamlit as st

class ThreeJSComponent:
    def show_3d_model(self):
        st.title("3D Model Viewer")
        st.markdown('<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/110/three.min.js"></script>', unsafe_allow_html=True)
        st.write('<div id="container"></div>', unsafe_allow_html=True)
        st.markdown("""
        <script>
            // Three.js code to render 3D model
        </script>
        """, unsafe_allow_html=True)

threejs_viewer = ThreeJSComponent()

def main():
    threejs_viewer.show_3d_model()

if __name__ == "__main__":
    main()
```
# #########################################################
# alien DEVzone use with caution everything might be broken
<a href="https://github.com/Faicey"><b>FAICE</b></a>=<b>Framework for Autonomous and Intelligent Computer Expressions</b>
<b>the faice of codephreak</b>
```python
#faice.py

import streamlit as st

class ThreeJSComponent:
    def render_threejs_scene(self):
        """
        Renders a three.js scene using the provided example link.
        """
        st.title("Three.js Integration: Decals Example")
        st.markdown('<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/110/three.min.js"></script>', unsafe_allow_html=True)
        st.write('<div id="container"></div>', unsafe_allow_html=True)
        st.markdown("""
        <script>
            // Three.js code for rendering the decals example
            // You can replace this script with the content from the example link you provided.
        </script>
        """, unsafe_allow_html=True)

threejs_viewer = ThreeJSComponent()

def main():
    threejs_viewer.render_threejs_scene()

if __name__ == "__main__":
    main()
```
<b>newfaice upload to faice</b>
```python
#newfaice.py

import streamlit as st

class ThreeJSComponent:
    def render_custom_threejs_scene(self, uploaded_file):
        """
        Renders a custom three.js scene with an uploaded graphic.
        Args:
            uploaded_file: Uploaded graphic file (jpg, png, jpeg).
        """
        st.title("Custom Three.js Integration: Upload and Display")
        st.markdown('<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/110/three.min.js"></script>', unsafe_allow_html=True)
        st.write('<div id="container"></div>', unsafe_allow_html=True)
        
        # Load the uploaded custom graphic
        if uploaded_file is not None:
            st.write("Custom Graphic:")
            st.image(uploaded_file, caption="Uploaded Graphic", use_column_width=True)

        st.markdown("""
        <script>
            // Three.js code for rendering the custom scene
            // You can replace this script with the content for your custom scene.
        </script>
        """, unsafe_allow_html=True)

threejs_viewer = ThreeJSComponent()

def main(uploaded_file):
    threejs_viewer.render_custom_threejs_scene(uploaded_file)

if __name__ == "__main__":
    uploaded_file = st.file_uploader("Upload a custom graphic", type=["jpg", "png", "jpeg"])
    main(uploaded_file)
```
<b>transform controls xyz with three.js as a python module</b><br />
manipulate 3D objects using transform controls, such as translation, rotation, and scaling
```python
# transformControls.py

import streamlit as st

class ThreeJSTransformControls:
    def render_transform_controls_scene(self):
        st.title("Three.js Integration: Transform Controls Example")
        st.markdown('<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/110/three.min.js"></script>', unsafe_allow_html=True)
        st.markdown('<script src="https://threejs.org/examples/js/controls/TransformControls.js"></script>', unsafe_allow_html=True)
        st.write('<div id="container"></div>', unsafe_allow_html=True)
        st.markdown("""
        <script>
            // Three.js code for rendering the Transform Controls example
            // You can replace this script with the content from the example link you provided.
        </script>
        """, unsafe_allow_html=True)

transform_controls_viewer = ThreeJSTransformControls()

def main():
    transform_controls_viewer.render_transform_controls_scene()

if __name__ == "__main__":
    main()
```

<b>add transformUIUX.py to your iApp ensure that transformControls.py is in the same folder</b>
```python
# transformUIUX.py

import streamlit as st
from transformControls import ThreeJSTransformControls

transform_controls_viewer = ThreeJSTransformControls()

def main():
    st.title("iApps - From Zero to Hero")
    st.write("Welcome to your advanced UI/UX experience!")

    # You can include other components and functionality here

    transform_controls_viewer.render_transform_controls_scene()

if __name__ == "__main__":
    main()
```
<b>drag controls module<b/>
```python
#dragControls.py

import streamlit as st

class ThreeJSDragControls:
    def render_drag_controls_scene(self):
        st.title("Three.js Integration: Drag Controls Example")
        st.markdown('<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/110/three.min.js"></script>', unsafe_allow_html=True)
        st.markdown('<script src="https://threejs.org/examples/js/controls/DragControls.js"></script>', unsafe_allow_html=True)
        st.write('<div id="container"></div>', unsafe_allow_html=True)
        st.markdown("""
        <script>
            // Three.js code for rendering the Drag Controls example
            // You can replace this script with the content from the example link you provided.
        </script>
        """, unsafe_allow_html=True)

drag_controls_viewer = ThreeJSDragControls()

def main():
    drag_controls_viewer.render_drag_controls_scene()

if __name__ == "__main__":
    main()
```
```python
# dragcontrolsUIUX.py

import streamlit as st
from dragControls import ThreeJSDragControls

drag_controls_viewer = ThreeJSDragControls()

def main():
    st.title("iApps - From Zero to Hero")
    st.write("Welcome to your advanced UI/UX experience!")

    # You can include other components and functionality here

    drag_controls_viewer.render_drag_controls_scene()

if __name__ == "__main__":
    main()
```
<b>codephreak openGL animation module</b>  
<b>keyframesAnimation.py</b>
```python
# keyframesAnimation.py

import streamlit as st

class ThreeJSKeyframesAnimation:
    def render_keyframes_animation_scene(self):
        st.title("Three.js Integration: Keyframes Animation Example")
        st.markdown('<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/110/three.min.js"></script>', unsafe_allow_html=True)
        st.write('<div id="container"></div>', unsafe_allow_html=True)
        st.markdown("""
        <script>
            // Three.js code for rendering the keyframes animation example
            // You can replace this script with the content from the example link you provided.
        </script>
        """, unsafe_allow_html=True)

keyframes_animation_viewer = ThreeJSKeyframesAnimation()

def main():
    keyframes_animation_viewer.render_keyframes_animation_scene()

if __name__ == "__main__":
    main()
```
<b>include keyframes in your phreakUIUX.py include the module in the same folder</b>
```python
# phreakUIUX.py

import streamlit as st
from keyframesAnimation import ThreeJSKeyframesAnimation

keyframes_animation_viewer = ThreeJSKeyframesAnimation()

def main():
    st.title("iApps - From Zero to Hero")
    st.write("Welcome to your advanced UI/UX experience!")

    # You can include other components and functionality here

    keyframes_animation_viewer.render_keyframes_animation_scene()

if __name__ == "__main__":
    main()
```

##### putting it all together #####<br />

<b>module to import a local language model as an app controller</b>

```python
# localLanguageModels.py

import streamlit as st
from transformers import pipeline

class LocalLanguageModels:
    def __init__(self):
        self.text_generator = pipeline("text-generation")

    def generate_text(self, prompt):
        generated_text = self.text_generator(prompt, max_length=100)
        return generated_text[0]['generated_text']

    def render_language_model_integration(self):
        st.title("Local Language Model Integration")
        prompt = st.text_input("Enter a prompt", "Once upon a time...")
        if st.button("Generate"):
            generated_text = self.generate_text(prompt)
            st.write("Generated Text:")
            st.write(generated_text)
```
<b>updated codephreakUIUX.py</b>
```python
# codephreakUIUX.py

import streamlit as st
from dragControls import ThreeJSDragControls
from decalsExample import ThreeJSDecalsExample
from keyframesAnimation import ThreeJSKeyframesAnimation
from newfaice import NewFaceGenerator
from chatgpt import ChatGPTInterface
from localLanguageModels import LocalLanguageModels

class CodephreakUIUXApp:
    def __init__(self):
        self.drag_controls_viewer = ThreeJSDragControls()
        self.decals_example_viewer = ThreeJSDecalsExample()
        self.keyframes_animation_viewer = ThreeJSKeyframesAnimation()
        self.new_face_generator = NewFaceGenerator()
        self.chatgpt_interface = ChatGPTInterface()
        self.language_model_integration = LocalLanguageModels()

    def render_app(self):
        st.title("iApps - From Zero to Hero")
        st.write("Welcome to your advanced UI/UX experience!")

        # You can include other components and functionality here

        self.drag_controls_viewer.render_drag_controls_scene()
        self.decals_example_viewer.render_decals_example_scene()
        self.keyframes_animation_viewer.render_keyframes_animation_scene()
        self.new_face_generator.render_new_face_generator()
        self.chatgpt_interface.render_chatgpt_interface()
        self.language_model_integration.render_language_model_integration()

def main():
    app = CodephreakUIUXApp()
    app.render_app()

if __name__ == "__main__":
    main()
```
<b>codephreakUIUX.py experimental user prompt version to be tested NO SECURITY v1</b>
```python
#codephreakUIUX.py

import streamlit as st
from dragControls import ThreeJSDragControls
from decalsExample import ThreeJSDecalsExample
from keyframesAnimation import ThreeJSKeyframesAnimation
from newfaice import NewFaceGenerator
from chatgpt import ChatGPTInterface
from localLanguageModels import LocalLanguageModels

class CodephreakUIUXApp:
    def __init__(self):
        self.drag_controls_viewer = ThreeJSDragControls()
        self.decals_example_viewer = ThreeJSDecalsExample()
        self.keyframes_animation_viewer = ThreeJSKeyframesAnimation()
        self.new_face_generator = NewFaceGenerator()
        self.chatgpt_interface = ChatGPTInterface()
        self.language_model_integration = LocalLanguageModels()

    def prompt_api_keys(self):
        st.title("Enter API Keys")
        self.chatgpt_api_key = st.text_input("ChatGPT API Key")
        self.language_model_api_key = st.text_input("Local Language Model API Key")
        self.database_api_key = st.text_input("Database API Key")

    def render_app(self):
        self.prompt_api_keys()

        st.title("iApps - From Zero to Hero")
        st.write("Welcome to your advanced UI/UX experience!")

        # You can include other components and functionality here

        self.drag_controls_viewer.render_drag_controls_scene()
        self.decals_example_viewer.render_decals_example_scene()
        self.keyframes_animation_viewer.render_keyframes_animation_scene()
        self.new_face_generator.render_new_face_generator()
        self.chatgpt_interface.render_chatgpt_interface(self.chatgpt_api_key)
        self.language_model_integration.render_language_model_integration(self.language_model_api_key)
        # Include database integration here using self.database_api_key

def main():
    app = CodephreakUIUXApp()
    app.render_app()

if __name__ == "__main__":
    main()
```

# <b>integrating streamlit with react</b><br />

```bash
npx create-react-app my-streamlit-component
```
```bash
npm install --save streamlit-component-lib
```

<b>modify /src/iApp.js</b>

```javascript
import { Streamlit, withStreamlitConnection } from "streamlit-component-lib";
import React from "react";

function App() {
  return (
    <button
      onClick={() => Streamlit.setComponentValue("Button clicked")}
    >
      Click Me
    </button>
  );
}

export default withStreamlitConnection(App);

```

<b>build the react component</b><br />

```bash
npm run build
```

<b>create the iApp streamlit codephreak.py as example name of iApp</b>
```python
#codephreak.py
import streamlit as st
import streamlit.components.v1 as components

_my_component = components.declare_component("my_streamlit_component", path="path/to/my-streamlit-component/build")

clicked = _my_component()

if clicked:
    st.write(f"You clicked the button: {clicked}")

<b>run the iApp</></b>
codephreak.py
<b>inject html and JavaScript into the streamlit iApp</></b>

import streamlit as st

st.write(
    """
    <script>
    function myFunction() {
        alert("Hello! Streamlit + JavaScript");
    }
    </script>
    <button onclick="myFunction()">Click Me</button>
    """,
    unsafe_allow_html=True,
)
```

setting unsafe_allow_html=True to allows HTML content<br />
as an example the JavaScript function myFunction shows an alert box when the button is clicked<br />

<b>Security Considerations for the platforming of iApps from here are considerable</b>

    Input Validaition and Sanitization: Always sanitize and validate data coming from custom components.
    Least Privilege Principle: Only use the permissions you need.
    Secure Communication: If the component interacts with external services, make sure to use HTTPS.
    Threat Modeling: Understand the data flows and potential areas where sensitive information might be exposed.
