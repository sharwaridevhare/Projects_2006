import sounddevice as sd
from scipy.io.wavfile import write
import wavio
import speech_recognition as sr
from gtts import gTTS
import os
import time
from playsound import playsound

def record_audio(filename="input.wav", duration=5, fs=44100):
    print("🎙️ Speak now...")
    audio = sd.rec(int(duration * fs), samplerate=fs, channels=1)
    sd.wait()
    wavio.write(filename, audio, fs, sampwidth=2)
    print("✅ Recording saved.")

def recognize_speech(filename="input.wav"):
    recognizer = sr.Recognizer()
    with sr.AudioFile(filename) as source:
        audio = recognizer.record(source)
    try:
        text = recognizer.recognize_google(audio)
        print("🗣️ You said:", text)
        return text
    except sr.UnknownValueError:
        return "Sorry, I could not understand."
    except sr.RequestError:
        return "Could not request results from Google Speech Recognition."

def speak_text(text):
    tts = gTTS(text=text, lang='en')
    filename = "response.mp3"
    tts.save(filename)
    playsound(filename)
    os.remove(filename)

def main():
    while True:
        record_audio()
        query = recognize_speech()

        if "exit" in query.lower():
            speak_text("Goodbye! Have a nice day.")
            break

        # Simple commands
        if "your name" in query.lower():
            response = "I am your Python voice assistant!"
        elif "time" in query.lower():
            response = f"The current time is {time.strftime('%I:%M %p')}"
        else:
            response = "Sorry, I can't help with that yet."

        print("🤖 Assistant:", response)
        speak_text(response)

if __name__ == "__main__":
    main()
# Projects_2006
