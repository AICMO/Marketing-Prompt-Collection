# Case Study Collection Automated Flow

## Goal
To create a fully automated, end-to-end case management workflow that handles cases from initial intake to final resolution with minimal manual intervention.

## Flow
Automated Flow: CRM (deal closed) → Zapier Automation → Zoom Call (15 mins) → Granola → Gemini/ChatGPT

### Flow Description
This flow automatically captures new cases from various channels (e.g., CRM, email, web forms) and uses AI to extract data, classify, and route them to automatically generate case. 

## Steps
- Trigger Event (e.g. CRM deal closed)
  - Send Webhook to Zapier with contacts 
  - Automatically create event Calendar and invite customer for 10 mins call on their use case to help them
- Zoom Call with recording (using Otter or Granola)
  - Recognize if not recognized in previous step 
- Put recognized transcript with prompt below into LLM (Gemini/ChatGPT/etc)

## How to Use the Prompt
Choose a prompt: Select the one that best fits your needs. The detailed prompt will almost always give you a better result.

Copy the text: Copy the entire prompt text into your AI chat interface (like Gemini, ChatGPT, etc.).

Paste your transcript: Replace the [PASTE YOUR... HERE] placeholder with the full, raw text from your meeting transcript.

Send and review: Let the AI generate the content. Review the output for accuracy and make any necessary edits to better reflect your company's voice or add details the AI might have missed.

## The Quick & Easy Prompt
Use this when you need a fast draft and the meeting transcript is fairly straightforward.

```markdown
Analyze the following meeting transcript and generate a case study.

First, identify the client, their core problem, the solution we proposed, and the final results.

Then, create three versions:
1.  Short Form: A concise paragraph summarizing the project.
2.  Long Form: A detailed narrative with sections for Challenge, Solution, and Results.
3.  Website Form: A version with a catchy headline, sub-headline, and bullet points for easy scanning.

[PASTE MEETING TRANSCRIPT HERE]
```

## The Detailed & Professional Prompt (Recommended)
This prompt provides more specific instructions, defines a persona for the AI, and requests structured outputs, which will yield higher-quality, more consistent results.
```markdown
ROLE:
You are an expert B2B Content Strategist specializing in transforming technical discussions and client meetings into compelling, results-oriented case studies.

OBJECTIVE:
Analyze the provided meeting transcript to extract key information and generate three distinct case study formats suitable for different marketing channels. Maintain a professional, confident, and value-focused tone of voice.

STEP 1: CORE ANALYSIS
First, meticulously review the entire transcript and identify the following components. If a component is not explicitly mentioned, note that it is missing.

* Client: The name of the client company/organization.
* The Challenge: The core business problem, pain points, or objectives the client was facing. What prompted them to seek a solution?
* The Solution: The product, service, or strategy that was proposed and implemented. Describe the key steps of the implementation process.
* The Results: The outcomes and impact of the solution. Prioritize quantifiable metrics (e.g., percentages, revenue figures, time saved).
* Compelling Quotes: Extract 1-2 direct quotes from the client that would make powerful testimonials.

STEP 2: CONTENT GENERATION
Using the information from your analysis, generate the following three formats.

FORMAT 1: Long-Form Case Study (For Blog/PDF)
Create a detailed narrative structure. Use the following headings:
* Executive Summary: A brief, 2-3 sentence overview of the entire project.
* The Client: A short paragraph introducing the client.
* The Challenge: A detailed description of the problem and its business implications.
* The Solution: An in-depth explanation of the strategy and implementation process.
* Results & Impact: A section focused on the positive outcomes, leading with the most impressive quantitative data.
* Conclusion: A brief summary of the project's success and partnership.

FORMAT 2: Short-Form Case Study (For Email/Social Media)
Write a concise, engaging summary of 150-200 words. Structure it to quickly grab attention by following a Problem-Solution-Result flow. End with a strong concluding sentence about the value delivered.

FORMAT 3: Website Version (For a "Case Studies" Page)
Design this for maximum scannability on a webpage.
* Catchy Headline: An outcome-focused title (e.g., "How [Client Name] Increased Efficiency by 45% with Our Solution").
* Sub-headline: A 1-2 sentence summary of the project.
* Project Snapshot:
    * Client: [Client Name]
    * Industry: [Client's Industry]
    * Service: [Service Provided]
* The Challenge: Use 2-3 bullet points.
* The Solution: Use 2-3 bullet points.
* The Results: Use 2-3 bullet points, starting each with a key metric (e.g., "45% Increase in...", "Reduced process time by...").
* Client Testimonial: Insert the best quote you extracted.

INSTRUCTIONS FOR AI:
* If specific metrics are mentioned but lack context, present them as they are.
* If no metrics are mentioned, use placeholders like `[Insert specific % increase]` and mention in your analysis that quantitative data is missing.
* Do not invent information. Base all content strictly on the provided transcript.

Begin Analysis and Generation below this line, based on the provided transcript:

[PASTE YOUR MEETING TRANSCRIPT HERE]
```
