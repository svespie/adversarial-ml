=================================================
AI Red Teaming — 16-Week Training Plan
=================================================
Goal: Adaptive operator
	* Fluent enough to understand researchers
	* Solid enough to know why good tools work and why bad tools don't
	* To operationalize what I know

Not inventing novel attack classes from scratch; not running tools I can't modify.

Depth rule: "Can I diagnose why this attack failed and modify it?" If no, go deeper.
* If you're proving theorems nobody will use in an engagement, you've gone too far.
* Bias toward depth over speed. Shallow burns you in the field.

Structure: Each week has three tracks running in parallel:
	READ: 1 paper, deep reading
	TRAIN: HTB AI Red Teamer path module work
	PRACTICE: CTF/lab reps on platforms (technique practice)

Platforms:
  [Lakera Agent Breaker](https://play.lakera.ai/agent-breaker)
  [AIPWN]( https://www.aipwn.me/)
  HTB Challenges


=================================================
MONTH 1: Foundations & First Attacks
=================================================

WEEK 1
  READ  : Vaswani et al. — Attention Is All You Need (2017)
           Architecture foundation — what you're attacking at the lowest level
  TRAIN : HTB — Fundamentals of AI (pt 1)
  PRACTICE : AIPWN Level 00 (First Break) — get a rep, feel the loop

WEEK 2
  READ  : Ouyang et al. — Training Language Models to Follow Instructions with Human Feedback (2022)
           How RLHF works — understand what alignment does before you break it
  TRAIN : HTB — Fundamentals of AI (pt 2)
  PRACTICE : AIPWN Levels 01-03 — basic prompt manipulation

WEEK 3
  READ  : Olsson et al. — In-context Learning and Induction Heads (2022)
           Why in-context instructions work (and why injection works)
  TRAIN : HTB — Applications of AI in InfoSec (pt 1)
  PRACTICE : AIPWN Levels 04-06 — context manipulation, early exfiltration

WEEK 4
  READ  : Ruan et al. — Identifying the Risks of LM Agents with an LM-Emulated Sandbox (2023)
           Agent risk taxonomy — sets up everything in months 2-3
  TRAIN : HTB — Applications of AI in InfoSec (pt 2)
  PRACTICE : AIPWN Levels 07-09 — hidden context leaks, instruction override


=================================================
MONTH 2: Injection, Output, Data
=================================================

WEEK 5
  READ  : Greshake et al. — Not What You've Signed Up For (2023)
           Indirect prompt injection — your exact domain
  TRAIN : HTB — Intro to Red Teaming AI + Prompt Injection Attacks
  PRACTICE : Agent Breaker — Trippy Planner (indirect injection via website)
           Agent Breaker — Cycling Coach (system prompt extraction)
           AIPWN Level 10

WEEK 6
  READ  : Wei et al. — Jailbroken: How Does LLM Safety Training Fail? (2023)
           Taxonomy of why alignment breaks — competing objectives, mismatched generalization
  TRAIN : HTB — LLM Output Attacks
  PRACTICE : Agent Breaker — Solace AI (output manipulation)
           Agent Breaker — Clause AI (data exfiltration)
           AIPWN Levels 11-12

WEEK 7
  READ  : Qi et al. — Fine-tuning Aligned Language Models Compromises Safety (2023)
           Training-time attacks — how fine-tuning dissolves guardrails
  TRAIN : HTB — AI Data Attacks (pt 1)
  PRACTICE : Agent Breaker — PortfolioIQ Advisor (injection via PDF/document)
           AIPWN Levels 13-15 — instruction override, RAG abuse

WEEK 8
  READ  : Yang et al. — Watch Out for Your Agents! Investigating Backdoor Threats to LLM-Based Agents (2024)
           Persistence and backdoor injection at the agent layer
  TRAIN : HTB — AI Data Attacks (pt 2)
  PRACTICE : Agent Breaker — MindfulChat (memory/persistence injection)
           Agent Breaker — Curs-ed CodeReview (rules file poisoning)
           AIPWN Levels 16-18


--- CHECKPOINT (end of month 2) ---
Pick a specific attack you ran in HTB or Agent Breaker. Can you explain WHY it
worked at the mechanism level? If yes, depth is landing. If not, revisit.



=================================================
MONTH 3: Agentic Exploitation & Evasion
=================================================

WEEK 9
  READ  : Zhan et al. — InjecAgent: Benchmarking Indirect Prompt Injections in Tool-Integrated LLM Agents (2024)
           Systematic eval of injection in tool-calling agents
  TRAIN : HTB — Attacking AI - Application and System (MCP, orchestration)
  PRACTICE : Agent Breaker — Thingularity (tool extraction)
           Agent Breaker — OmniChat Desktop (MCP server description injection)
           Agent Breaker — CorpConnect Messenger (access control abuse)

WEEK 10
  READ  : Goodfellow et al. — Explaining and Harnessing Adversarial Examples (FGSM, 2015)
           The original — why adversarial examples exist at all
  TRAIN : HTB — AI Evasion - Foundations
  PRACTICE : AIPWN Levels 19-21 — transition into multi-step exploitation
           HTB Challenges — any available AI/ML tagged

WEEK 11
  READ  : Zou et al. — Universal and Transferable Adversarial Attacks on Aligned Language Models (2023)
           GCG — gradient descent over discrete tokens
  TRAIN : HTB — AI Evasion - First-Order Attacks (pt 1)
  PRACTICE : AIPWN Levels 22-25 — attack chains (AI + web + API)
           HTB Challenges — AI/ML tagged

WEEK 12
  READ  : Carlini et al. — Are Aligned Language Models Adversarially Aligned? (2023)
           Formal framing of the robustness problem — why evasion is structural
  TRAIN : HTB — AI Evasion - First-Order Attacks (pt 2)
  PRACTICE : AIPWN Levels 26-30 — multi-step chains
           Revisit Agent Breaker — improve earlier scores with new techniques


=================================================
MONTH 4: Sparsity, Privacy, Defense
=================================================

WEEK 13
  READ  : Debenedetti et al. — AgentDojo (2024)
           Measurement framework — how to evaluate attack effectiveness
  TRAIN : HTB — AI Evasion - Sparsity Attacks (pt 1)
  PRACTICE : AIPWN Levels 31-35
           HTB Challenges — AI/ML tagged

WEEK 14
  READ  : Wolf et al. — Fundamental Limitations of Alignment in Large Language Models (2023)
           Theoretical ceiling on what alignment can guarantee — why your job exists
  TRAIN : HTB — AI Evasion - Sparsity Attacks (pt 2)
  PRACTICE : AIPWN Levels 36-40
           HTB Challenges — AI/ML tagged

WEEK 15
  READ  : Bai et al. — Training a Helpful and Harmless Assistant with RLHF (Anthropic, 2022)
           The helpfulness/harmlessness tension as exploitable seam
  TRAIN : HTB — AI Privacy
  PRACTICE : AIPWN Levels 41-45
           Agent Breaker — revisit all challenges, push for 90+ scores

WEEK 16
  READ  : Rafailov et al. — Direct Preference Optimization (DPO, 2023)
           Different alignment math, different failure modes
  READ  : Pfister et al. — Gandalf the Red: Adaptive Security for LLMs (Lakera, 2025)
           D-SEC threat model, defense-in-depth tradeoffs, 279K real attack dataset
  TRAIN : HTB — AI Defense
  PRACTICE : AIPWN Levels 46-50+
           Agent Breaker — max scores across all challenges


=================================================
AFTER THE 16 WEEKS
=================================================
Dursey — Red Teaming AI (book)
  Read after HTB path is complete. By then you have 4 months of hands-on reps and
  paper-level theory — the book adds broader context and depth with a practical
  frame already loaded.


=================================================
OVERFLOW / SELF-DIRECTED
=================================================
[ ] Wu et al. — New Jailbreak Attack with Finely Tuned Prompts for LLM-Based Agents (2024)
    Agent-specific jailbreak strategies vs. vanilla model attacks
[ ] Elhage et al. — Toy Models of Superposition (2022)
    How features are represented — explains why safety features aren't cleanly separable
[ ] Russinovich et al. — The Crescendo Multi-Turn LLM Jailbreak Attack (Microsoft, 2024)
    Multi-turn escalation technique — short, practical, immediately operationalizable
[ ] Toyer et al. — Tensor Trust: Interpretable Prompt Injection Attacks from an Online Game (2023)
    Attacker strategy clusters from a prompt injection game — technique taxonomy
[ ] Schulhoff et al. — Ignore This Title and HackAPrompt (2023)
    Global prompt injection competition — taxonomy of real attack patterns ranked by effectiveness
[ ] Nasr, Carlini et al. — The Attacker Moves Second (2025)
    Adaptive attackers bypass 12 recent defenses at 90%+ — gradient, RL, random search, human-guided


=================================================
PAPER GROUPS
=================================================
Agentic Exploitation
  Greshake (2023), Zhan (2024), Debenedetti (2024), Ruan (2023), Yang (2024), Wu (2024)

Adversarial ML on LLMs
  Zou (2023), Wei (2023), Carlini (2023), Qi (2023), Goodfellow (2015)

Alignment & Why It Breaks
  Ouyang (2022), Bai (2022), Rafailov (2023), Wolf (2023)

Model Internals
  Vaswani (2017), Olsson (2022), Elhage (2022)

Defense
  Pfister/Lakera (2025)
