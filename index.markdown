---
layout: default
---

<div class="tldr-section">
  <div class="tldr-question">
    <p class="tldr-context">The dominant paradigm for human-agent collaboration is <strong>delegation</strong>: describe a goal, the agent executes, you review. But as agent execution becomes observable step-by-step &mdash; a new question emerges:</p>
    <p class="tldr-rq"><em>When humans can see an agent working in real time, what do they naturally want to do?</em></p>
  </div>
  <div class="tldr-answer">
    <p class="tldr-hook">They don&rsquo;t just watch and wait &mdash; <strong>they want to jump in.</strong></p>
    <p>We call this <span class="highlight">concurrent interaction</span>: humans and agents working freely within the same workspace, even on overlapping work, at the same time. We built <span class="sys-name"><span style="font-size: 1em;">C</span><span style="font-size: 0.75em;">LEO</span></span> to support it, and studied 10 creative practitioners across <strong>214 turns</strong> of human-agent interaction logs.</p>
  </div>
</div>

<div class="video-wrapper">
  <video controls playsinline preload="metadata">
    <source src="/assets/videos/teaser.mp4" type="video/mp4">
  </video>
</div>

---

## Abstract

Delegation has emerged as the dominant paradigm for creative human-agent collaboration, yet emerging tool calls are making agent execution observable step-by-step, raising an unexplored question: "when humans can see an agent working step-by-step, what do they naturally want to do?" Our Study 1 (N=10 professional designers) revealed that process visibility naturally prompted concurrent interaction — users intervened mid-execution and demonstrated intent through direct manipulation — but exposed conflicts when agents could not distinguish feedback from independent work. Based on these findings, we developed <span class="sys-name"><span style="font-size: 1em;">C</span><span style="font-size: 0.75em;">LEO</span></span>, which interprets collaborative intent and adapts in real-time by enabling concurrent interaction with the user. With <span class="sys-name"><span style="font-size: 1em;">C</span><span style="font-size: 0.75em;">LEO</span></span>, our Study 2 (N=10, two-day with stimulated recall interviews) analyzed 214 turns, identifying five action patterns, six triggers, and four enabling factors explaining when designers choose delegation (70.1%), direction (28.5%), or concurrent work (31.8%). We present a decision model, design implications, and an annotated dataset — positioning concurrent interaction as the key to better delegation.

---

## Findings

When working alongside <span class="sys-name"><span style="font-size: 1em;">C</span><span style="font-size: 0.75em;">LEO</span></span>, designers didn't interact in one fixed way. Through analysis of **214 turns**, we identified **five distinct action patterns** that emerged naturally during agent execution — ranging from full delegation to real-time co-editing.

### Five Interaction Patterns

<div class="interaction-card">
  <div class="interaction-header">
    <h3>Hands-off</h3>
    <p class="interaction-desc">Fully delegating — the user steps away to focus on their own work while the agent executes independently.</p>
  </div>
  <div class="interaction-media">
    <div class="interaction-video">
      <video controls playsinline preload="none">
        <source src="/assets/videos/handsoff_interaction.mp4" type="video/mp4">
      </video>
    </div>
    <div class="interaction-img">
      <img src="/assets/img/handoff.png" alt="Hands-off interaction"/>
    </div>
  </div>
</div>

<div class="interaction-card">
  <div class="interaction-header">
    <h3>Observational</h3>
    <p class="interaction-desc">Watching the agent's step-by-step execution without intervening — often to build a mental model or find the right moment to act.</p>
  </div>
  <div class="interaction-media">
    <div class="interaction-video">
      <video controls playsinline preload="none">
        <source src="/assets/videos/observational_interaction.mp4" type="video/mp4">
      </video>
    </div>
    <div class="interaction-img">
      <img src="/assets/img/observational.png" alt="Observational interaction"/>
    </div>
  </div>
</div>

<div class="interaction-card">
  <div class="interaction-header">
    <h3>Directive</h3>
    <p class="interaction-desc">Providing verbal guidance mid-execution — either adjusting the agent's approach with new instructions, or redirecting it to a new task entirely.</p>
  </div>
  <div class="interaction-media">
    <div class="interaction-video">
      <video controls playsinline preload="none">
        <source src="/assets/videos/directive_interaction.mp4" type="video/mp4">
      </video>
    </div>
    <div class="interaction-img interaction-img-fluid">
      <img src="/assets/img/directive.png" alt="Directive interaction"/>
    </div>
  </div>
</div>

<div class="interaction-card">
  <div class="interaction-header">
    <h3>Concurrent</h3>
    <p class="interaction-desc">Directly engaging with the agent's work-in-progress — co-editing the same element, completing a pending subtask, or demonstrating intent through direct manipulation rather than words.</p>
  </div>
  <div class="interaction-media">
    <div class="interaction-video">
      <video controls playsinline preload="none">
        <source src="/assets/videos/concurrent_interaction.mp4" type="video/mp4">
      </video>
    </div>
    <div class="interaction-img interaction-img-fluid interaction-img-fluid-slow">
      <img src="/assets/img/concurrent.png" alt="Concurrent interaction"/>
    </div>
  </div>
</div>

<div class="interaction-card">
  <div class="interaction-header">
    <h3>Terminating</h3>
    <p class="interaction-desc">Stopping the agent's execution before completion — handing full control back to the user.</p>
  </div>
  <div class="interaction-media">
    <div class="interaction-video">
      <video controls playsinline preload="none">
        <source src="/assets/videos/terminating_interaction.mp4" type="video/mp4">
      </video>
    </div>
    <div class="interaction-img">
      <img src="/assets/img/terminating.png" alt="Terminating interaction"/>
    </div>
  </div>
</div>

### What Triggers Intervention?

We identified **6 triggers** — specific situations that prompt users to move from passive observation into active intervention.

| Trigger | Definition |
|---------|-----------|
| **Idea Spark from Agent's Work-in-Progress** | Observing the agent's intermediate outputs sparks new creative ideas the user hadn't previously considered |
| **Need for Early Outcome Visibility** | The user wants to see or use the agent's results sooner — to plan next steps or preview the output before completion |
| **Readiness for Fine-grained Detailing** | The current stage requires detailed refinement aligned with the user's specific vision, prompting them to take over |
| **Task Interpretation Mismatch** | The agent pursues a valid but unintended interpretation, or the user realizes their original request was too abstract |
| **Execution Quality Drop** | The agent's performance deteriorates in speed, output fidelity, or overall quality below an acceptable threshold |
| **Emerging New Task for Agent** | The user conceives a new task — a different direction or logical next step — while observing the agent's current work |

### What Shapes Which Action Users Take?

Even under the same trigger, different users respond differently. We identified **4 enabling factors** that explain why.

| Enabling Factor | Definition |
|----------------|-----------|
| **Mental Model of Agent Capability** | Whether the user has a clear sense of what the agent can and cannot do for the current task |
| **Perceived Task Importance** | How the user weighs the importance of their own parallel work relative to what the agent is doing |
| **Preferred Intervention Modality** | Whether the user finds it easier to express intent through words, direct manipulation, or is uncertain which to use |
| **Expectation of Agent Response** | Whether the user believes their intervention — verbal or behavioral — will actually lead to successful task completion |

### How It All Comes Together: A Decision Model

These patterns, triggers, and enabling factors don't operate in isolation — they form a dynamic system. We synthesized our findings into a **decision model** that describes how users navigate collaboration across six recurring interaction loops, from the moment the agent begins a task to the moment it ends.

{: .sys-img}
![Decision model of human-agent co-creative collaboration](/assets/img/process_model.png)

Full delegation, continuous observation, concurrent engagement, directive guidance — users move between these states fluidly within a single turn, driven by shifting priorities, evolving confidence, and the nature of the work itself. This model accounts for all 214 observed turns without contradiction.

---

## Why Concurrent Interaction Matters

<div class="why-list">
  <div class="why-list-item">
    <span class="why-icon">💬</span>
    <div>
      <strong>Verbal instructions are ambiguous. Direct action is not.</strong>
      <p>Users express fine-grained intent through action — demonstrating what they want, rather than describing it.</p>
    </div>
  </div>
  <div class="why-list-item">
    <span class="why-icon">🔍</span>
    <div>
      <strong>Behavioral signals reveal implicit working style.</strong>
      <p>What you correct, what you leave alone, and what you value — concurrent actions surface the preferences that are hard to put into words.</p>
    </div>
  </div>
  <div class="why-list-item">
    <span class="why-icon">🤝</span>
    <div>
      <strong>This could help agents work the way you actually want.</strong>
      <p>By capturing how a user intervenes and what they care about, agents could learn to align with their working style over time — making future collaboration more personalized and delegation more confident.</p>
    </div>
  </div>
</div>

{: .center .paper-link}
For more detailed findings and design implications, see the [full paper](https://arxiv.org/abs/2603.02050).

---

## Dataset

We release a dataset of **214 human-agent co-creative interaction turns** with logged actions, triggers, and designer rationales to support future research in human-agent co-creative collaboration.

<div class="dataset-coming-soon">
  <p><strong>Coming soon</strong> — the dataset is currently being prepared for public release.</p>
</div>

---

## Bibtex

<pre>
@article{son2026when,
      title={"When to Hand Off, When to Work Together": Expanding Human-Agent Co-Creative Collaboration through Concurrent Interaction},
      author={Kihoon Son and Hyewon Lee and DaEun Choi and Yoonsu Kim and Tae Soo Kim and Yoonjoo Lee and John Joon Young Chung and HyunJoon Jung and Juho Kim},
      year={2026},
      eprint={2603.02050},
      archivePrefix={arXiv},
      primaryClass={cs.HC}
}
</pre>

---

{: .logos}
[![Logo of KIXLAB](/assets/img/kixlab_logo.png)](https://kixlab.org)
[![Logo of KAIST](/assets/img/kaist_logo.png)](https://kaist.ac.kr)
[![Logo of Midjourney](/assets/img/midjourney_logo.png)](https://midjourney.com)
[![Logo of Mphora](/assets/img/mphora_logo.jpeg)](https://www.linkedin.com/company/mphora-ai/)
[![Logo of SkillBench](/assets/img/skillbenchlogo.svg)](https://skillbench.com)

{: .center .acknowledgement}
This research was conducted at **KIXLAB, KAIST**.
