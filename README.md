# Telegram → Google Gemini (Gemini 2.5 Flash - Nano Banana) → Veo3 

This n8n workflow automates the process of receiving an image from Telegram, enhancing it with **Google Gemini**, collecting **user approval via Telegram**, and—depending on the user’s choice—either re-generating the image or creating a cinematic video with **Veo3_fast (via Kie API)**.  

---

## Features  

- **Telegram Integration**  
  - Users send an image (with an optional caption as prompt).  
  - Workflow replies with generated content and requests feedback.  

- **Image Processing (Google Gemini)**  
  - Extracts the Telegram image file.  
  - Sends image + prompt to Gemini API for enhancement.  
  - Returns a base64-encoded AI-generated image back to the user.  

- **Feedback & Approval Loop**  
  - Telegram bot asks user whether to:  
    - Approve → Generate cinematic video.  
    - Re-create → Retry edit with updated instructions.  

- **Video Generation (Veo3_fast API)**  
  - Uploads image to ImgBB for reference URL.  
  - Analyzes image with OpenAI (gpt-4o) for cinematic context.  
  - Generates structured UGC-style video prompt with AI Agent.  
  - Calls Veo3_fast API to create an 8s verti_
