# Google-Assisant

Since 2019 Google removed the [hotword detection](https://github.com/googlesamples/assistant-sdk-python/issues/411)
software which disabled the function to be able to recognise "Hey Google"
or "OK Google" to trigger the assistant. There was a work around 
called [snowboy](https://github.com/Kitt-AI/snowboy) which Kitt-Ai stopped maintaining.
So I decided to make my own speech to text trigger with the [SpeechRecognition](https://pypi.org/project/SpeechRecognition/) python module. I also added an aditional module for playing a sound when the assistant is triggered.

# Installation 

First of all register the device with this [tutorial](https://developers.google.com/assistant/sdk/guides/service/python). Follow until the step 4. After that you need to clone this repository `git clone https://github.com/raspberrypi5621/google-assisant.git` after change directory inside the assistant with `cd google-assisant/assistant` and continue with the step 5 but without running `python3 -m venv env`.  

# Run the code

I will have a redy to run google-assistant-sdk in the repository. To run the assistant run the following command:

`googlesamples-assistant-hotword` (modified hotword detection)


