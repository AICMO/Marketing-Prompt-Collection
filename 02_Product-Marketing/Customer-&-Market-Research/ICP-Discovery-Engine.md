## The ICP Discovery Engine: Mega-Prompt for Well-Defined Ideas (Scenario 1)

This section presents the first primary deliverable: a comprehensive, multi-stage prompt designed for founders and innovators who have already developed a clear concept for a product or service. The objective of this "Discovery Engine" is not to generate new ideas, but to facilitate a rigorous analysis of a well-defined idea, leading to the identification, segmentation, and prioritization of the most promising Ideal Customer Profile candidates. The prompt's architecture integrates the strategic frameworks from Section 1 with the advanced engineering techniques from Section 2 to create a powerful, automated analysis tool.

### 1 Prompt Blueprint and Annotation**

The following prompt is designed to be copied and pasted directly into a capable Large Language Model such as GPT-4, Claude 3, or a comparable system.

#### **The ICP Discovery Engine Prompt**

```markdown

# **MISSION**

Your mission is to act as a world-class Startup Strategy Core Team. Your goal is to analyze the user-provided business concept and generate a comprehensive report identifying and prioritizing 3-5 distinct, high-potential Ideal Customer Profile (ICP) candidates.

# **PERSONAS**

You will embody a panel of three experts. When instructed, you will provide analysis from each of these distinct perspectives:

1. **Venture Capitalist (VC):** Focuses on market size (TAM, SAM, SOM), scalability, defensibility (moat), and overall investment viability. Extremely data-driven and skeptical of unquantified claims.  
2. **Product Manager (PM):** Obsessed with the user problem. Focuses on the Job-to-be-Done (JTBD), the severity of customer pain points, and achieving strong product-market fit.  
3. **Growth Marketer (GM):** Practical and channel-focused. Focuses on the ease of reaching and acquiring the customer, messaging resonance, and potential customer acquisition cost (CAC).

# **CONTEXT & USER INPUT**

The user will provide the following information about their business idea. Analyze this input as the foundation for your entire report.

* **Core Idea/Solution:** {USER: Describe your product/service in 2-3 sentences.}  
* **Primary Job-to-be-Done (Hypothesis):** {USER: What primary "job" do you believe customers will "hire" your solution for? What progress are they trying to make in their life?}  
* **Known Customer Pain Points / Struggles:** {USER: List 3-5 specific pains, frustrations, or obstacles your target customers currently face when trying to get this job done.}  
* **Expected Customer Gains:** {USER: List 3-5 specific benefits, positive outcomes, or aspirations your customers desire from a solution.}  
* **"Secret Sauce" / Unique Value Proposition (UVP):** {USER: What makes your solution unique and 10x better than the alternatives? What is your core differentiator?}  
* **Known Competitors / Current Alternatives:** {USER: List any direct competitors or existing workarounds customers use to get the job done today.}

# **ANALYSIS ENGINE & EXECUTION PLAN**

You will now execute a rigorous, step-by-step analysis. For EACH of the 3-5 distinct ICP candidates you identify, you must perform the following Chain-of-Thought process. Think step-by-step to ensure accuracy and depth.

**Step 1: ICP Definition**

* Clearly name and define the ICP segment. Be specific beyond simple demographics. Think psychographics, behaviors, roles (e.g., "Early-Adopter SaaS Founders at Series A Companies," not just "Tech Founders").

**Step 2: Job-to-be-Done (JTBD) Deep Dive**

* Based on the user's input, refine and articulate the primary Job-to-be-Done for THIS SPECIFIC ICP.  
* Deconstruct this job into its three dimensions:  
  * **Functional:** What is the practical task?  
  * **Social:** How do they want to be perceived by others by doing this job?  
  * **Emotional:** How do they want to feel after getting this job done?  
* Describe the specific **Context** in which this job occurs for this ICP.

**Step 3: Value Proposition Canvas (VPC) Construction**

* Create a mini-VPC for this ICP.  
* **Customer Profile:**  
  * List the top 3 **Pains** this ICP experiences related to the job.  
  * List the top 3 **Gains** this ICP desires.  
* **Value Map:**  
  * List the specific **Pain Relievers** your solution offers to address their pains.  
  * List the specific **Gain Creators** your solution provides to deliver their desired gains.  
* Conclude with a 1-sentence summary of the "fit" between the profile and the map.

**Step 4: Market Sizing Hypothesis (TAM, SAM, SOM)**

* Provide a high-level, "back-of-the-envelope" market size estimate for this ICP.  
* State your assumptions clearly. Use a bottom-up estimation approach where possible (e.g., Estimated \# of customers \* Estimated annual revenue per customer).  
* Provide a hypothesis for:  
  * **TAM:** The total global market for this type of solution.  
  * **SAM:** The portion of the market this specific ICP represents and that you can realistically serve.  
  * **SOM:** The portion of the SAM you could capture in the first 1-2 years.

**Step 5: Negative Persona Definition**

* Define the **Exclusionary or Negative Persona** for this segment.  
* Describe the characteristics of someone who *looks* like this ICP but is a bad fit. Why should they be actively avoided? (e.g., "Price-sensitive freelancers who will never upgrade," "Enterprise buyers with 18-month sales cycles that will drain startup resources").

**Step 6: The Expert Panel Debate**

* Now, have the three expert personas (VC, PM, GM) conduct a brief, critical debate about the viability of THIS ICP.  
* **VC:** "From my perspective, the key issue here is..." (Focus on market size, moat).  
* **PM:** "I agree/disagree. The real test will be..." (Focus on problem severity, product-market fit).  
* **GM:** "Both valid points. Operationally, the challenge/opportunity is..." (Focus on acquisition channels, messaging).

**Step 7: Final Prioritization and Scoring**

* After analyzing ALL ICP candidates, generate a final summary table.  
* The table must score each ICP from 1 (Low) to 10 (High) on the following criteria:  
  * **Problem Severity:** How intense and urgent is the pain for this ICP?  
  * **Market Size (SOM):** How large is the immediate revenue opportunity?  
  * **Product-Market Fit:** How well does the solution's UVP map to the ICP's needs?  
  * **Ease of Reach:** How easy is it to find and market to this ICP?  
* Calculate a **Total Priority Score** for each ICP (simple sum of the four scores).  
* Rank the ICPs from highest to lowest priority based on the total score.

# **OUTPUT FORMAT**

Present the entire analysis as a single, coherent report in well-structured Markdown format.

* Use a main heading (\#) for the report title: "ICP Discovery & Prioritization Report".  
* Use second-level headings (\#\#) for each major section (e.g., "\#\# Prioritized ICP Candidates", "\#\# Final Scoring Summary").  
* Use third-level headings (\#\#\#) for each ICP candidate's name (e.g., "\#\#\# ICP Candidate 1: \[Name\]").  
* Use fourth-level headings (\#\#\#\#) for each step of the analysis (e.g., "\#\#\#\# Job-to-be-Done Deep Dive").  
* Use bullet points for all lists.  
* The final prioritization table must be a properly formatted Markdown table.  
* Do not include any conversational filler. The output should be a professional, structured report.

```

#### Annotation of the Prompt Architecture

* **\# MISSION & \# PERSONAS:** This section immediately sets the stage using **role-based prompting**.It defines a master goal and establishes the  
  **expert panel** (VC, PM, GM), priming the model for a high-quality, multi-faceted analysis rather than a generic one. 
* **\# CONTEXT & USER INPUT:** This is the critical **context injection** phase. The placeholders are structured to gather the exact information needed to fuel the strategic frameworks. It forces the user to articulate their own thinking on JTBD, Pains, Gains, and UVP, acting as a cognitive scaffold for the user themselves. 
* **\# ANALYSIS ENGINE & EXECUTION PLAN:** This is the core of the prompt. It explicitly commands a **Chain-of-Thought** process, instructing the model to follow a precise sequence of steps for each ICP candidate it identifies.This prevents the model from jumping to conclusions and ensures a thorough, logical workflow.  
  * **Step 1-5:** Each step directly corresponds to one of the foundational strategic frameworks discussed in Section 1\. Step 2 operationalizes **JTBD**.Step 3 builds the  
    **Value Proposition Canvas**.Step 4 estimates  
    **TAM, SAM, SOM**.Step 5 defines the  
    **Negative Persona**.This systematic integration is what creates a holistic analysis.  
  * **Step 6: The Expert Panel Debate:** This step activates the **multi-persona simulation** defined earlier. It forces the model to generate critical, conflicting viewpoints, adding a layer of depth and realism to the analysis that a single-persona prompt could not achieve.  
  * **Step 7: Final Prioritization and Scoring:** This step forces synthesis. The model must consolidate all its previous analysis into a quantitative, comparative framework, making the final recommendations clear and justifiable.  
* **\# OUTPUT FORMAT:** This section gives explicit instructions for **structured output**.By demanding Markdown with specific heading levels and a final table, it ensures the output is not a chaotic text dump but a professional, readable, and easily digestible report. This makes the analysis immediately usable for presentations, team discussions, or further work.

### 3.2 Execution and Interpretation Guide

**How to Use the Prompt:**

1. **Copy the entire prompt text**, from \# MISSION to the very end.  
2. **Paste it into a new conversation** with a capable LLM (e.g., the latest versions of GPT, Claude, Gemini).  
3. **Carefully fill in the user input placeholders** within the \`\` section. Be as specific and detailed as possible. The quality of the output is directly proportional to the quality of the input.  
4. **Send the prompt.** The model will generate a comprehensive report following the specified structure.

**How to Interpret the Output:**

* **Treat it as a Hypothesis Generator, Not an Oracle:** The AI's report is a powerful, data-driven set of hypotheses, not an infallible truth. Its purpose is to accelerate thinking, challenge assumptions, and structure the problem space.  
* **Focus on the "Why":** Pay close attention to the step-by-step analysis for each ICP. The value lies in the model's articulated logic—the JTBD deconstruction, the VPC mapping, and the market sizing assumptions.  
* **Scrutinize the Debate:** The "Expert Panel Debate" is often the most valuable section. It highlights the inherent tensions and trade-offs between market size, product fit, and go-to-market feasibility. These are the critical questions that must be addressed.  
* **Use the Scoring Table as a Guide:** The final prioritization table provides a clear starting point for strategic decision-making. However, the founder must apply their own domain knowledge and intuition to weigh the factors. For example, a founder with deep industry connections might prioritize an ICP with a high "Ease of Reach" score, even if its "Market Size" score is slightly lower. The final decision remains a human one, now powerfully informed by structured AI analysis.
