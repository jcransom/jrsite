---
title: 'How to slightly reduce the time it takes to transcribe an interview'
date: 21 Sep 2021
draft: false
places:
projects: ['Tools & processes']
summary: Over the past few months I’ve had hours and hours of interviews to transcribe, and this is my system for doing it as painlessly as possible.
---

{{< lead >}} Over the past few months I’ve had hours and hours of interviews to transcribe, and this is my system for doing it as painlessly as possible. {{< /lead >}}

I wanted to call this post ‘how to dramatically slash interview transcription times’. However, transcription – at least in an academic setting – is often a process of generating new ideas and uncovering layers of understanding at the same time as you go through your recording word-for-word. It’s a messy and time-consuming task, but there are technical steps you can take to speed it up. (For my policy work I often don’t transcribe at all – this is the best way to slash your transcription times).

Over the past few months I’ve had hours and hours of interviews to transcribe, and this is my system for doing it as painlessly as possible. 

### First: automatic transcription

The pandemic has forced interviews online, but thankfully both Zoom and Teams offer inbuilt transcription. You’ll want to host the meeting yourself to ensure you’re able to record the meeting, and of course seek permission to do so. You can then generate and download a transcript soon after the meeting finishes.

If you’re using a dictaphone, there are a raft of online automatic transcription services. Otter, Sonix and Ebby are three examples. If your interview is particularly sensitive you’ll want to check the relevant data security and storage policies of the service you choose.

A major benefit of transcription from Zoom or Teams is the accurate labelling of who said what. Some other services claim to be able to do this using machine learning, but online conversations will always split conversations flawlessly because the sound of each participant is saved as a different channel – unlike a dictaphone.
![](Screenshot%202021-09-16%20at%2015.00.41.png "Transcription isn't always flattering.")

### Second: initial clean

Transcription files are usually a `.vtt` file. There are timestamps and other metadata smeared everywhere. You can clean this up using an online tool called [Microsoft Stream transcript VTT file cleaner](https://web.microsoftstream.com/VTTCleaner/CleanVTT.html), which strips out the time codes, metadata, and extra lines and gives you a solid block of text.

I prefer do a quick clean using a text editor. For the uninitiated, a text editor gives you magical powers to manipulate text files – you can move, tidy, and change thousands of words in seconds. You can fly around huge documents with ninja-like speed. I use [Sublime Text](https://www.sublimetext.com), but [VS Code](https://code.visualstudio.com) and [Atom](https://atom.io) are open source alternatives. Microsoft Word is not a text editor.

It’s worth learning the basics of whichever text editor you pick, but support for multiple cursors, regular expressions and extensions are standard. I remove all the timestamps and other cruft, change the speaker names (from `<Smith, John>` to `Interviewee:`, for example), and save the file as text (`.rtf`). If you notice any repeated errors, for example I often find _Rwanda_ is transcribed as _Rhonda_, you can fix these all in one go too. This process takes no more than a couple of minutes – a fraction of what it would take to change everything manually.

### Third: review

Automatic transcription is pretty advanced – at least compared to ten years ago. But it will still need fixing. At the very least words will be wrong and some entire sentences garbled. You might also want to remove verbal fillers (people, including myself, say ‘yeah’ way more than I realised). I also found that transcription is more accurate for native English speakers from the UK and North America, suggesting some bias in the machine learning used.

I use a free application called [Transcriptions](https://github.com/soleil-alpin/Transcriptions) for Mac to review my recordings; similar options should be available for Windows. You load the text file transcript and your audio recording, and play it back, checking the accuracy. Some advice:

- Find a playback speed that allows you to correct on-the-fly, without needing to keep stopping and starting the recording. When you get into the flow you’ll tackle the whole text much quicker (an hour interview is usually 7,000 - 10,000 words). Around 0.75x usually worked for me.
- Learn the keyboard shortcuts to stop and start the recording, and to go back 10 seconds. You’ll need the last one to check anything that’s unclear, and not having to use the mouse/trackpad to find the relevant buttons will save lots of time on a less-than-crystal-clear transcription.
- In my interviews I usually ask around 10 questions. After each I add a timestamp (using another keyboard shortcut in the application). This allows you to later review the original recording if need be, and in the Transcriptions application you can click the timestamp to be taken to that part of the recording.
- Sometimes you’ll come across a name that keeps on getting garbled by the automatic transcription. It’s a pain to have to type out _ International Bank for Reconstruction and Development_ every time it’s wrong, and if it gets mangled into a different form every time, the find-and-replace function from above won’t help. Here substitutions are great: set a couple of characters, e.g. `-ib`, and this will automatically be expanded to _ International Bank for Reconstruction and Development_. This feature is built into Transcriptions, I use [Alfred](https://www.alfredapp.com) on the Mac (where the feature is called snippets), and there are loads for Windows – just search for ‘text expander’.
![](Screenshot%202021-09-17%20at%2009.39.56.png "The Transcriptions interface")

### Fourth: finalising

Once I have a complete and accurate transcript, I move the text back into Sublime Text and finalise it. Again, this is a speedy step that should take ten minutes.

I save the file as Markdown (`.md`). Now two clever (and free) Sublime Text extensions come into play: [MarkdownEditing](https://github.com/SublimeText-Markdown/MarkdownEditing) and [Markdown​TOC](https://packagecontrol.io/packages/MarkdownTOC). Using a Markdown subheading (`###`) I add in around ten topic headers – where the conversation moves into a new subject, or changes direction and I’ll want to find it again easily.
![](Screenshot%202021-09-16%20at%2015.15.49.png "Adding in topic headers")
Then using simple syntax I can generate a table of contents.
![](Screenshot%202021-09-16%20at%2015.15.57.png "Automatic TOC creation based on markdown headers")
Finally I quickly change the speaker names into italics (using multiple selections), make the timestamps bold (using regular expressions), and sometimes I’ll add in URLs to specific projects or organisations that have been discussed. I double check the interviewee’s name has been redacted throughout – you may, of course, not need to do this.
![](Screenshot%202021-09-16%20at%2015.08.01.png "Tidying the text")
Using the wizardry of [Pandoc](https://pandoc.org) (or the excellent [DocDown](https://github.com/lowercasename/docdown) if you want a command-line-free alternative for Mac), the Markdown file is transformed into a Microsoft Word file for easy sharing.
![](Screenshot%202021-09-16%20at%2015.10.26.png "The transcript in Word...")
You’ll notice that the table of contents is automatically created.
![](Screenshot%202021-09-16%20at%2015.17.00.png "...with a hyperlinked TOC")
Some of this is a little technical, and I’ve passed over some detail to keep this relatively concise. [Let me know](mailto:j.ransom@hey.com) if you’d like me to expand on anything.