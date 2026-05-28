# AI-Powered Movie Review Blog Generator

**Module:** Industrial Skills Assessment — PGDip Artificial Intelligence (Human Centred)  
**Institution:** Bournemouth University, UK  
**Stack:** Python · Django · OpenAI API · AssemblyAI · PyTube · Jupyter Notebook  

---

## Overview

An AI-powered content platform that automatically transforms user-generated movie ratings and reviews into published blog posts — functioning like a **Substack for IMDb**.

Users leave movie ratings and reviews on social media, either as written text or as video reviews. The system automatically:
- Downloads video reviews via PyTube
- Transcribes spoken video feedback using AssemblyAI's speech-to-text API
- Generates polished, structured blog posts from that content using OpenAI's GPT API
- Publishes the output as readable articles — turning every user rating into a piece of longform content

The result is a user-generated content engine where the community's opinions become a continuously updated publication, with no manual writing required.

---

## The Problem This Solves

Platforms like IMDb collect millions of star ratings and short reviews, but this content rarely reaches its full potential as readable, shareable articles. Meanwhile, YouTube and social media are full of video movie reviews that are never indexed or searchable as text.

This project bridges that gap — automatically converting both written and video-format reviews into structured blog content, making community opinions more discoverable and valuable.

---

## How It Works

```
User leaves a movie rating/review (text or video)
            ↓
If video: PyTube downloads the video from YouTube/social media
            ↓
AssemblyAI transcribes the spoken audio to text
            ↓
OpenAI GPT structures and generates a polished blog post
            ↓
Django serves the published blog post to readers
```

---

## Tech Stack

| Component | Technology | Purpose |
|-----------|-----------|---------|
| Web Framework | Django | Backend, routing, serving blog posts |
| AI Content Generation | OpenAI API (GPT) | Generating structured blog posts from review content |
| Speech-to-Text | AssemblyAI | Transcribing video/audio reviews to text |
| Video Download | PyTube | Extracting video content from YouTube and social media |
| Environment | Jupyter Notebook | Development and prototyping |
| Language | Python 3 | Core application logic |

---

## Installation

```bash
# Clone the repository
git clone https://github.com/Phissie/Blog_generator_AI.git
cd Blog_generator_AI

# Install dependencies
pip install django
pip install pytube
pip install openai
pip install assemblyai

# Set up environment variables
# Create a .env file with your API keys:
# OPENAI_API_KEY=your_openai_key_here
# ASSEMBLYAI_API_KEY=your_assemblyai_key_here
```

---

## Usage

Open the Jupyter notebook:

```bash
jupyter notebook Blog_Generator_for_Industrial_Skills_Assessment_.ipynb
```

The notebook walks through:
1. Connecting to the OpenAI and AssemblyAI APIs
2. Downloading a video review via PyTube
3. Transcribing the audio with AssemblyAI
4. Sending the transcription to OpenAI GPT to generate a structured blog post
5. Outputting the final blog post content

---

## Key Dependencies

```python
from pytube import YouTube        # Video download from YouTube/social media
import assemblyai as aai          # Speech-to-text transcription
import openai                     # Blog post generation via GPT
import json                       # Data handling
import os                         # Environment and file management
```

---

## Use Cases

- **Movie review aggregation** — collect community opinions and publish them as articles
- **Video review transcription** — make spoken reviews searchable and readable
- **User-generated content platforms** — any platform where community feedback can be repurposed as longform content
- **Content automation** — reduce manual writing effort while maintaining authentic user voices

---

## Project Context

This project was built as part of the Industrial Skills Assessment module of the PGDip in Artificial Intelligence (Human Centred) at Bournemouth University. It demonstrates practical application of:

- Third-party AI API integration (OpenAI, AssemblyAI)
- Multimodal input handling (text and video/audio)
- Automated content generation pipelines
- Django web framework for serving AI-generated content
- Real-world product thinking — solving a genuine gap between user-generated ratings and publishable content

---

## Future Development

- [ ] Direct social media API integration (pull reviews automatically from Twitter/X, YouTube)
- [ ] User authentication and personalised review pages
- [ ] Sentiment analysis to categorise reviews before generation
- [ ] Multi-language support via AssemblyAI's language detection
- [ ] Rating aggregation dashboard alongside blog posts

---

## Author

**Fisayo Fagade**  
PGDip Artificial Intelligence (Human Centred), Bournemouth University  
[LinkedIn](https://www.linkedin.com/in/fisayofagade/) | [Website](https://www.fisayofagade.uk) | [GitHub](https://github.com/Phissie)
