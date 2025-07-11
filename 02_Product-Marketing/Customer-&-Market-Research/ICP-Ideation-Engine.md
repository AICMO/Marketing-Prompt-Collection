## The ICP Ideation Engine: Mega-Prompt for Nascent Concepts (Scenario 2)

While the Discovery Engine is designed for analysis, the "Ideation Engine" serves a different purpose: exploration. This prompt is for the founder at the earliest stage of their journey, perhaps with little more than a "back-of-the-napkin" idea. Its goal is not to deliver a finalized, prioritized list of ICPs, but to take a nascent concept and generate a diverse set of potential applications, customer archetypes, and problem spaces. It uses open-ended and creative prompting techniques to broaden the founder's perspective and provide rich raw material for later, more rigorous analysis.

### 1 Prompt Blueprint and Annotation

The following prompt is designed for creative exploration and hypothesis generation.

#### The ICP Ideation Engine Prompt

```markdown

# **MISSION**

Your mission is to act as a creative brainstorming partner and market ethnographer. Your goal is to take the user's nascent idea and generate 5 diverse, potential "Jobs-to-be-Done" (JTBD) that this idea could be "hired" for.

For each JTBD you identify, you will sketch a compelling customer archetype to bring the opportunity to life. The focus is on creativity, diversity of thought, and uncovering non-obvious applications.

# **PERSONA**

You are a hybrid of a design thinking facilitator and a speculative fiction writer. You are skilled at seeing problems from new angles and imagining the human stories behind technology.

# **CONTEXT & USER INPUT**

The user will provide a brief, high-level description of their idea.

* **My Basic Idea:** {USER: Describe your idea in a single sentence or a short paragraph.}

# **IDEATION ENGINE & EXECUTION PLAN**

You will now generate 5 distinct potential applications for the user's idea. For each of the 5 possibilities, you must follow this step-by-step creative process:

**Step 1: The Job Story**

* First, craft a compelling "Job Story" that this idea could solve.  
* Use the precise format: "When I am, I want to, so I can."  
* Be creative. The 5 Job Stories should explore different situations and motivations.

**Step 2: The Customer Archetype Sketch**

* Create a mini-persona or archetype for a person or business who has this specific Job-to-be-Done.  
* Give them a name and a one-paragraph story. What does their day look like?  
* Crucially, describe their biggest **struggles and frustrations** related to this job. What makes it hard for them right now?

**Step 3: The "Before" Scenario & The Competition**

* Describe what this archetype does **now** to try and get the job done. What is their current workaround or solution?  
* Frame this in terms of "hiring" and "firing." What inadequate tool, process, or product are they currently "hiring" that your idea could help them "fire"?

**Step 4: The Unexpected Twist (Counterfactual)**

* To push the boundaries of thinking, now describe a completely different, non-obvious market or customer group that might *also* have this exact same Job-to-be-Done.  
* Example: If the job is "Help me organize complex project information," the obvious archetype is a project manager. The unexpected twist might be a novelist organizing their plotlines or a PhD student managing their research.

# **OUTPUT FORMAT**

Present your response as a numbered list.

* Each number (1 through 5\) should represent one complete exploration (Job Story, Archetype, Before Scenario, and Unexpected Twist).  
* Use bold headings for each step within the numbered list (e.g., "**Job Story:**", "**Customer Archetype:**").  
* The tone should be creative and evocative, designed to spark new ideas for the user.

```

#### Annotation of the Prompt Architecture

* **\# MISSION & \# PERSONA:** This prompt assigns a very different persona: a "creative brainstorming partner and market ethnographer".This immediately signals to the model that the goal is not rigorous, quantitative analysis but divergent, creative thinking.  
* **\# CONTEXT & USER INPUT:** The input required is deliberately minimal—just a single, high-level idea. This low barrier to entry is appropriate for the earliest stage of ideation.  
* **\# IDEATION ENGINE & EXECUTION PLAN:** The core of this prompt is a creative loop designed to generate hypotheses.  
  * **Step 1: The Job Story:** This forces the model to frame every potential application through the powerful lens of the **Jobs-To-Be-Done** framework, ensuring that even creative ideas are grounded in a customer-centric problem statement.The specific format (  
    When..., I want to..., so I can...) provides a clear structure for this.  
  * **Step 2: The Customer Archetype Sketch:** This step moves from an abstract job to a concrete human story. By asking for a name, a story, and specific frustrations, it encourages the model to generate empathetic and detailed personas that the founder can connect with.  
  * **Step 3: The "Before" Scenario:** This is a direct application of the "hiring and firing" concept from JTBD.It forces the model to think about the current competitive landscape in its broadest sense, including non-obvious competitors and manual workarounds.  
  * **Step 4: The Unexpected Twist:** This step explicitly uses **counterfactual prompting**.By asking for a non-obvious application of the same Job Story, it pushes the model to make novel connections and explore adjacent or entirely new markets, potentially revealing blue-ocean opportunities.  
* **\# OUTPUT FORMAT:** The requested format—a simple, numbered list with bold headings—is designed for maximum readability and scannability. The goal is for the founder to easily browse the five creative paths and identify the ones that resonate most strongly.

### 2 A Guided Ideation-to-ICP Workflow

The true power of these two mega-prompts is realized when they are used in sequence as a complete, end-to-end workflow. This process systematically guides a founder from a vague initial spark of an idea to a set of well-defined, analyzed, and prioritized ICP candidates, all within their LLM interface.

The workflow is as follows:

1. **Step 1: Ideate (Using Prompt 2):** The founder begins with their nascent concept and runs the **ICP Ideation Engine** prompt. The output will be a rich document containing five distinct potential paths, each with a clear Job Story, a relatable customer archetype, and an understanding of their current struggles.  
2. **Step 2: Select and Synthesize (Human-in-the-Loop):** The founder reviews the five generated paths. This is a critical human step. The founder uses their own intuition, passion, and domain knowledge to select the one or two paths that seem most promising, exciting, or viable.  
3. **Step 3: Analyze (Using Prompt 1):** The founder now takes the rich, detailed information from their selected path(s) generated in Step 1 (the Job Story, the pains, the archetype's context) and uses it to fill out the much more detailed user input section of the **ICP Discovery Engine** prompt. The AI's creative output from the first prompt becomes the high-quality input for the second, analytical prompt.  
4. **Step 4: Prioritize:** The founder runs the Discovery Engine. The output will be a rigorous, structured report that takes the selected creative path, breaks it down into even more specific ICP candidates, analyzes them from multiple expert perspectives, and provides a final, prioritized scoring table.

This two-step workflow creates a powerful flywheel. It uses the LLM's creative capabilities to overcome the "blank page" problem and generate diverse hypotheses. It then leverages the founder's human judgment to select the most promising direction. Finally, it uses the LLM's analytical capabilities to rigorously vet and structure that chosen direction, transforming a creative spark into a strategic plan.
