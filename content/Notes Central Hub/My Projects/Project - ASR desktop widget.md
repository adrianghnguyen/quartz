---
aliases:
  - desktop text to speech transcription
  - ASR (automatic speech recognition) widget
  - my audio transcription project
tags:
  - my-projects
note-type:
  - project
description: Use the OpenAI whisper package to do text transcription as a desktop widget
progress:
  - done
file-created: 2023-10-21
file-modified: 2023-10-26
start: 2023-10-21
end: 2023-10-23
difficulty:
  - low
linter-yaml-title-alias: ASR desktop engine
---

# ASR desktop engine

## Goals and Key success factors

I'm looking to create my own speech recognition add-on or Windows widget where I can just speak into any application I'd be able to write. Right now I can use the native Windows, but it's kind of finicky. So building my own I think is a bit more flexible and it would allow me to use different speech recognition engines since the Microsoft one doesn't work too well.

- [x] Speak into the microphone and return the transcript
- [ ] Open file for transcription
- [-] Ability to select different engine models for [[automatic speech recognition (ASR)|automatic speech recognition (ASR)]] within the `speechrecognition` package
- [x] Ability to paste transcribed audio into clipboard
- [x] Ability to run as standalone application/widget

## Project resources

- [[ASR Engine Brainstorming.canvas|ASR Engine Brainstorming]]
- [Python GUI - tkinter - GeeksforGeeks](https://www.geeksforgeeks.org/python-gui-tkinter/)
	- It provides a good overview of all the various commands and how the overall library works. It would be useful to read through.
- [The Ultimate Guide To Speech Recognition With Python – Real Python](https://realpython.com/python-speech-recognition/#working-with-microphones)
- Well fuck - someone's built it all [SpeechRecognition · PyPI](https://pypi.org/project/SpeechRecognition/)
	- [microphone\_recognition.py](https://github.com/Uberi/speech_recognition/blob/master/examples/microphone_recognition.py)
		- The key part here would be allowing it to swap out the engine to a locally hosted one
- [SamLowe/roberta-base-go\_emotions · Hugging Face](https://huggingface.co/SamLowe/roberta-base-go_emotions
	- This model from [[Machine learning collaboration platforms|HuggingFace]] allows me to label emotions
	- I'll probably need to read through this to better understand how to use the resulting outputs [Quick tour of Transformers](https://huggingface.co/docs/transformers/quicktour)

## Project diary and tasks

### [[2023-10-21|Saturday October 21st 2023]]

- Exploring how LLM architecture even works
- looking into how to use [[Hugging Face Audio Data Course|Hugging Face Audio Data Course]] to help me understand how to get pre-trained models
- Drawing basic architecture of the desktop widget
- I was thinking of using `pyaudio` and `sounddevice` as packages but turns out they're somewhat unwieldy.
- Perhaps using QT might be better?
	- [Audio Recorder Example | Qt Multimedia 5.15.15](https://doc.qt.io/qt-5.15/qtmultimedia-multimedia-audiorecorder-example.html#:~:text=To%20record%20audio%20we%20simply,state%20of%20the%20audioRecorder%20object.)
- I'm using the tkinter library and copying the staple code allows me to set up a quick thingie.
	- [tkinter — Python interface to Tcl/Tk — Python 3.12.0 documentation](https://docs.python.org/3/library/tkinter.html#tkinter-modules)

### [[2023-10-22|Sunday October 22nd 2023]]

- Using the `speech_recognition` and turns out you need to have `r.adjust_for_ambient_noise(source)` otherwise it won't pick it up
- got the error of missing `whisper` package but turns out there's also another package on PyPi with the same name. As a result you need to install it using `pip install git+https://github.com/openai/whisper.git`
- Nice! Got it working - but it generated 140mb apparently? Seems excessive for a small speech size.
- How do I change the default whisper binding model?
- Decided to use the `pysimplegui` package as it seems recommended by people
- [Demo\_Buttons\_Base64\_Simple.py](https://github.com/PySimpleGUI/PySimpleGUI/blob/master/DemoPrograms/Demo_Buttons_Base64_Simple.py) <- How to make buttons
- Is output element what I'm looking for?
	- [PySimpleGUI](https://www.pysimplegui.org/en/latest/#output-element)
	- [Print output?](https://www.pysimplegui.org/en/latest/cookbook/#recipe-printing-24-print-to-output-element)

### [[2023-10-23|Monday October 23rd 2023]]

You can create it into a windows executable based on this link: [Cookbook - PySimpleGUI](https://www.pysimplegui.org/en/latest/cookbook/#creating-a-windows-exe-file)

## Features and expected behaviour

### Version 1

- Click a button which begins listening to audio
- Have a window which displays the transcribed text
- Button to copy text
- Button to terminate widget
- Optional - automatically copy into clipboard

### Version 2

- Change button to display current recording state readiness which should go through as a loop
	- Ready to listen
	- Calibrating
	- Listening
	- Ready to listen

Apparently the best way to do this would be though a simulated callback function as listed here:
- [Callback function simulation](https://www.pysimplegui.org/en/latest/cookbook/#recipe-callback-function-simulation)
---

## Learned Lessons

> [!faq] What went well? What went poorly? What can we do better?

It was interesting to build my first little [[Python programming|Python programming]] project. It was a chance for me to interacted with [[Machine learning collaboration platforms|HuggingFace]] and how to use the speech recognition library for [[automatic speech recognition (ASR)|automatic speech recognition (ASR)]]. It also helped me understand a bit more about how [[Large language models produce human text using big data|LLMs]] work and their transformer architecture.

What went well:
- Learned how to use `pysimplegui` and `speech_recognition` package
- Troubleshooting some basic problems and understanding how to read documentation
- Built something which was useful to me

What can we do better:
- Not sure for now. This was just a fun little project to take on
- Packaging it into a standalone .exe rather than launching it from a .bat file. Hey there recommend using the `pyinstaller` library
	- [How can I make a Python script standalone executable to run without ANY dependency? - Stack Overflow](https://stackoverflow.com/questions/5458048/how-can-i-make-a-python-script-standalone-executable-to-run-without-any-dependen)