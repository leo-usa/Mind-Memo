Mind Memo App

Path system prompt:

You are an expert in TypeScript, Next.js App Router, React, and Tailwind. Follow @Next.js docs for Data Fetching, Rendering, and Routing.

Make the app mobile compitiable and optimized for mobile.

App description:

I want to create a voice-based note-taking app.

App flow and functionality:

The flow of the app is as follows:

When user opens the page, it opens the front page showing title "Mind Memo", subtitle: "Created by Elynn Pang, sponsored by NACEF" (Elynn Pang URL: https://www.elynnpang.com, NACEF URL: https://www.nacef.org). 

It should have a toggle to switch betweeen English, Simplified Chinese, and Traditional Chinese. The displayed texts and buttons should the corresponding language accordingly. 

It uses Firebase authorization to allow user to either register or log in. In the user registration, it allows to register by using Google, or by email/phone number and password. 

The bottom should have links commonn on website, such as "About", "NACEF", etc.

It should remember the user. User doesn't have to log in everytime.

Once user loggs in, and there is a play/start button to start recording your voice.
When the user clicks on the button, it asks for permission to access the microphone.
If the user clicks allow, the app starts recording and the button changes to a stop button.
When the user clicks on the stop button, the app stops recording and transcribes the voice note using the the latest OpenAI transcribe API. The following is an example:
import fs from "fs";
import OpenAI from "openai";

const openai = new OpenAI();

const transcription = await openai.audio.transcriptions.create({
  file: fs.createReadStream("/path/to/file/speech.mp3"),
  model: "gpt-4o-mini-transcribe",
  response_format: "text",
});

console.log(transcription.text);

While the user is speaking, there is a clean, simple animation on the screen along with the realtime transcription of the voice note.
The user can click the stop button to stop the recording.

After ther is done recording, it shows an UI that displayed the transcribed text. 
In this UI it has icons for fucnctions: edit, clear, translate (into English), summary, medical, and save. Edit allows user to edit th note. Rest uses OpenAI model to generate the new note: Clear: it re-write the notes based on its sounds and meanings. Translate: translate the note into English. Summary: summarize the note. Medical note: re-write the note in a style that doctors and nurses use. Save: save the note  with the date, timeinto the Firebase Firestore database.

Now, the app displays the note in a list of all notes on the home screen.

It allows user to select either all notes or individual note. It has options: delete, medical note. Basically it deletes the selected notes, or convert the selected notes into new a medical note.

This application is set-up with existing configuration for OpenAI APIs and Firebase. Implement all the functionality in the flow above while using the existing codebase as a starting point, but fully modify the codebase to fit the flow and functionality described above.