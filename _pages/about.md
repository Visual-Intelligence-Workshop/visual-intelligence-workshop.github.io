---
layout: about
title: Home
permalink: /
subtitle: "December 2026 &bull; Location Date still open..."

selected_papers: false
social: false

announcements:
  enabled: false # set to true and give announcement that accepted.
  scrollable: true
  limit: 5

latest_posts:
  enabled: false
  scrollable: true
  limit: 3
---

<style>
.people-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 1.5rem;
  margin: 1rem 0 2rem;
}
.person-card {
  width: 160px;
  text-align: center;
}
.person-card img,
.person-placeholder {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  object-fit: cover;
  display: block;
  margin: 0 auto;
  background: #e0e0e0;
}
.person-card .person-name {
  font-weight: 600;
  font-size: 0.9rem;
  margin-top: 0.5rem;
  display: block;
}
.person-card .person-affiliation {
  font-size: 0.8rem;
  color: #888;
  display: block;
}
.person-card .person-bio {
  font-size: 0.78rem;
  margin-top: 0.4rem;
  text-align: left;
}
</style>

Humans do not experience vision as a set of parallel processes. We perceive, imagine, and act through a single integrated faculty. This unity took millions of years to evolve. This workshop asks whether this unity can emerge in silicon, and whether we would know if it did.

The history of large language models offers a provocative precedent. For years, language models scaled without producing qualitatively new behaviours. Then, at sufficient scale and with sufficient architectural coherence, capabilities appeared that had not been trained for directly: in-context learning, chain-of-thought reasoning, cross-domain analogy. These emergent properties were not designed; they arose. The field is now asking whether an analogous transition is possible for visual intelligence. Are systems that jointly perceive scenes, generate plausible futures, answer questions, and control robotic action starting to exhibit a unified visual understanding that is more than the sum of its parts.

This is not a settled question, and the workshop is not premised on an optimistic answer. The LLM analogy may be misleading: language has a structure that vision may lack as it is: sequential, compositional, grounded in a shared symbolic system. Visual intelligence may be fundamentally modular, and what appears to be unification may be sophisticated interpolation across correlated training distributions. However, emergent properties at scale have also been observed in the vision domain. We do not currently have the conceptual frameworks or evaluation tools to distinguish these possibilities. This workshop is organised around the effort to build them.

**Central hypothesis:** Unified visual intelligence may arise as an emergent property of scale and architectural convergence, in the same fashion as general reasoning emerged in large language models. The workshop stress-tests this hypothesis across perception, generation, action, and evaluation.

##### Tracks

The following tracks are unified by the central hypothesis. Each addresses a different facet of the same question: is visual intelligence emerging, and how would we know?

- **Visual Reasoning** — Do current systems reason about the visual world or exploit distributional shortcuts? Can a system that reasons well in language transfer that capacity to visual inference? What would purely visual reasoning look like in the absence of language scaffolding?
- **Evaluation and Benchmarking** — Existing benchmarks were designed for single-task models. What tasks, metrics, and protocols are needed to evaluate whether a system's visual capabilities are genuinely unified, i.e., mutually consistent and grounded, rather than separately capable? What would a "visual Turing test" for emergence look like?
- **Video Generative Models** — Generative models as a probe for understanding: if a model can generate physically plausible, temporally coherent video, does that imply an internal world model? What failure modes reveal the absence of genuine understanding beneath surface-level generation quality?
- **Unified Multimodal Architectures** — Joint models over perception, language, and generation: which architectural choices are necessary conditions for emergent unification, and which are incidental? What does the gap between current unified models and human visual cognition reveal?
- **Visual Perception and Cognition for Robotics** — Vision-Language-Action models provide a unique testbed: physical grounding exposes failures that purely perceptual or generative evaluations miss. Does embodiment accelerate or constrain the path toward unified visual intelligence?

---

### Invited Talks

#### Confirmed

{% assign confirmed_speakers = site.data.speakers | where_exp: "s", "s.confirmed == true" %}
<div class="people-grid">
{% for speaker in confirmed_speakers %}
<div class="person-card">
  {% if speaker.img and speaker.img != "" %}
  <img src="{{ speaker.img | relative_url }}" alt="{{ speaker.name }}">
  {% else %}
  <div class="person-placeholder"></div>
  {% endif %}
  <span class="person-name">{% if speaker.url and speaker.url != "" %}<a href="{{ speaker.url }}" target="_blank" rel="noopener noreferrer">{{ speaker.name }}</a>{% else %}{{ speaker.name }}{% endif %}</span>
  {% if speaker.affiliation and speaker.affiliation != "" %}<span class="person-affiliation">{{ speaker.affiliation }}</span>{% endif %}
  {% if speaker.bio and speaker.bio != "" %}<p class="person-bio">{{ speaker.bio }}</p>{% endif %}
</div>
{% endfor %}
</div>

#### Tentative

{% assign tentative_speakers = site.data.speakers | where_exp: "s", "s.confirmed != true" %}
<div class="people-grid">
{% for speaker in tentative_speakers %}
<div class="person-card">
  {% if speaker.img and speaker.img != "" %}
  <img src="{{ speaker.img | relative_url }}" alt="{{ speaker.name }}">
  {% else %}
  <div class="person-placeholder"></div>
  {% endif %}
  <span class="person-name">{% if speaker.url and speaker.url != "" %}<a href="{{ speaker.url }}" target="_blank" rel="noopener noreferrer">{{ speaker.name }}</a>{% else %}{{ speaker.name }}{% endif %}</span>
  {% if speaker.affiliation and speaker.affiliation != "" %}<span class="person-affiliation">{{ speaker.affiliation }}</span>{% endif %}
  {% if speaker.bio and speaker.bio != "" %}<p class="person-bio">{{ speaker.bio }}</p>{% endif %}
</div>
{% endfor %}
</div>

---

### Organizers

<div class="people-grid">
{% for organizer in site.data.organizers %}
<div class="person-card">
  {% if organizer.img and organizer.img != "" %}
  <img src="{{ organizer.img | relative_url }}" alt="{{ organizer.name }}">
  {% else %}
  <div class="person-placeholder"></div>
  {% endif %}
  <span class="person-name">{% if organizer.url and organizer.url != "" %}<a href="{{ organizer.url }}" target="_blank" rel="noopener noreferrer">{{ organizer.name }}</a>{% else %}{{ organizer.name }}{% endif %}</span>
  {% if organizer.affiliation and organizer.affiliation != "" %}<span class="person-affiliation">{{ organizer.affiliation }}</span>{% endif %}
  {% if organizer.bio and organizer.bio != "" %}<p class="person-bio">{{ organizer.bio }}</p>{% endif %}
</div>
{% endfor %}
</div>

<img src="{{ 'assets/img/organizer_logos.png' | relative_url }}" alt="Organizer affiliations" style="width: 100%; max-width: 800px; display: block; margin: 1rem auto 0;">
