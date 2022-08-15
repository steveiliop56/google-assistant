# Google-Assisant

Since 2019 Google removed the [hotword detection](https://github.com/googlesamples/assistant-sdk-python/issues/411)
software which disabled the function to be able to recognise "Hey Google"
or "OK Google" to trigger the assistant. There was a work around 
called [snowboy](https://github.com/Kitt-AI/snowboy) which Kitt-Ai stopped maintaining.
So I decided to make my own speech to text trigger with the [SpeechRecognition](https://pypi.org/project/SpeechRecognition/) python module. I also added an aditional module for playing a sound when the assistant is triggered.

# Installation 

First of all make the basic installation of google assistant with this [tutorial](https://developers.google.com/assistant/sdk/guides/service/python), make sure to add your email as a test user in order to work.

# Fix and modify the code

Now it's time to fix some code bugs and modify the code for hotword detection. First of all
we need to downgrade protobuf and upgrade tenacity with these commands (make sure you are in the virtual enviroment):

```
pip3 install --upgrade tenacity
pip3 install protobuf==3.20
```
Then delete the env/bin/googlesamples-assistant-hotword and env/bin/googlesamples-assistant-pushtotalk and replace them with the two files in the [assistant](https://github.com/raspberrypi5621/google-assistant/tree/main/assistant) in the repository.

Last but not least copy the two directories from the [assistant](https://github.com/raspberrypi5621/google-assistant/tree/main/assistant) direcory in my repository to env/lib/python3.9/site-packages/googlesamples/assistant. But make sure to delete all the contens before doing so.

Now we are ready to run the code but before doing it we need to install some dependencies with these commands (inside the env):

```
pip3 install speechrecognition
pip3 install pyaudio
pip3 install playsound
```

And you are done!

# Run the code

To run the code just enable the virtual enviroment with this command `source env/bin/activate` inside your google assistant directory and then type `cd env/bin'.

Now you can run this command for word detection:
`googlesamples-assistant-hotword` 

And this command for pushtotalk:
`googlesamples-assistant-pushtotalk`


