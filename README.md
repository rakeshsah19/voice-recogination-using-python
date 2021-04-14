# voice-recogination-using-python
import pyttsx3 

import speech_recognition as sr 

import datetime

import datetime

import webbrowser


import os

import smtplib



engine=pyttsx3.init('sapi5')
voices= engine.getproporty('voices')
engine.setProperty('voice',voices[0].id)
def speak(audio):
    engine.say(audio)
    engine.runAndWait()
def wishme():
    hour=(datetime.datetime.now().hour)
    if hour>=0 and hour<=12:
        speak("good morning friends")
    elif hour>=12 and hour<=18:
        spea("good evaning friend")
    else:
        speak("good evening friends")
    speak("i an frien mikel  i am made by rakesh.please tell me how can i healp you")
    
def takecomand():
    r=sr.Reconizer()
    with sr.microphone()as source:
        print("listining to you" )
        r.Pause_threshold=1
        audio=r.listen(source)
        
        try:
            print("recognizing your voice...")
            query= r.recognize_google(audio,langauge="en-in")
            print(f"rakesh said:{query}\n")
        except exception as e:
            print("rakeshmsay that aganin pleease..")
        return query
def sendEmail(to,content):
    server=smptlib.SMTP("smpt.gmail.com",587)
    server.ehol()
    server.starttls()
    server.login("youremail@gmail.com","your-password")
    server.sendmail(youremail@gmail.com,to,content)
    server.close()

if spak()  :
    wishme()
    while True:
        query=takecomand().lower()
        
        if "wikipedia"in query:
            speak("awarching wikipedia...")
            query=query.replace("wikipedia")
            result=wekipedi.summary(query)
            spak("acording to wikipedia")
            print(resuts)
            speak(results)
        elif "ope notpad in query":
            npath="C:\\WINDOWS\\system32\\notepad.exe"
            os.startfile(npath)
            
        elif "open youtoube " in query:
            webbrowser.open("youtoube.com")
        elif "open google "in query:
            webbrwser.open("google.com")
        
        elif "the time "in query:
            strTime=datetime.datetime.now().strftime("%H:%M:%S")
            speak(f"rakesh,the time is {strtime}")
            
        elif 'open chnel fun with data science'in query:
            webbrowser.open("https:// youtoube.com/c/funwithdatascience")
            
        elif "open linkedin" in query:
            webbrowser.open("www.linkedin.com")
        
        elif "email to rakesh" in query:
            try:
                speak("what should i send in the mail")
                content=takecommand()
                to ="rakeshkumarsah333@gmail.com"
                sendEmail(to,content)
                speak("Email hans been send to rakesh")
            except Exception as e:
                print(e)
                speak("sorry i am not able to send the email as you need to enter the password")
                 
            
