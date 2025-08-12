---
title: "Datathon 2025 Scoring"
permalink: /evaluation/
layout: single
mathjax: true
classes: wide
---

<!-- Page-specific styles -->
<style>
  :root { --bg:#fff; --fg:#1f2937; --muted:#6b7280; --accent:#2563eb; --card:#f9fafb; --border:#e5e7eb; }
  .mm-page #main { background: var(--bg); color: var(--fg); }
  .card { background: var(--card); border:1px solid var(--border); border-radius:14px; padding:1rem 1.25rem; }
  .muted { color: var(--muted); }
  code, kbd { background:#f3f4f6; padding:.15rem .35rem; border-radius:6px; }
  .eq { background:#fff; border-left:3px solid var(--accent); padding:.75rem 1rem; border-radius:8px; overflow-x:auto; }
  table { width:100%; border-collapse:collapse; margin:1rem 0; }
  th, td { padding:.6rem .5rem; border-bottom:1px solid var(--border); vertical-align:top; }
  th { text-align:left; font-weight:700; }
  .pill { display:inline-block; padding:.2rem .5rem; border-radius:999px; background:#eef2ff; color:#3730a3; font-weight:600; font-size:.8rem; }
  .callout { border:1px solid var(--border); background:#fff; border-radius:12px; padding:1rem; }
  details { background:#fff; border:1px solid var(--border); border-radius:10px; padding:.5rem .75rem; }
  details > summary { cursor:pointer; font-weight:600; }
</style>

<header>
  <h1>Fair Scoring Methodology</h1>
  <p class="muted">Evaluating performance, team cohesion, and skill retention transparently.</p>
</header>

<section class="card">
  <h2>Overview</h2>
  <p>We evaluate teams across two challenges (C1 and C2). Scores reflect both the <strong>quality of deliverables</strong> and the ability to <strong>maintain team capacity</strong> despite dropouts.</p>
  <p>The final score combines a <span class="pill">Base Score</span>, a <span class="pill">Team Cohesion Multiplier</span>, and a <span class="pill">Skill Retention (Capacity) Multiplier</span>.</p>
</section>

<h2>Base Scoring Rubric</h2>

<h3>Challenge #1: Dataset Creation & Annotation (50 points total)</h3>
<table>
  <thead>
    <tr><th>Variable</th><th style="width:70px;text-align:center;">Max</th><th>Definition</th></tr>
  </thead>
  <tbody>
    <tr><td><code>C1_Relevance_Variety</code></td><td style="text-align:center;">10</td><td>Dataset includes relevant antisemitic and non-antisemitic posts; diverse sources (hashtags, keywords, user groups).</td></tr>
    <tr><td><code>C1_Annotation_Schema</code></td><td style="text-align:center;">10</td><td>Correct application of IHRA-WDA or justified adaptation; schema maps clearly to labels used.</td></tr>
    <tr><td><code>C1_Internal_Consistency</code></td><td style="text-align:center;">10</td><td>Labels applied consistently with minimal misclassification; shows internal review.</td></tr>
    <tr><td><code>C1_Data_Report_Quality</code></td><td style="text-align:center;">10</td><td>Dataset report includes keyword/time range, label definitions, label distribution, methodology.</td></tr>
    <tr><td><code>C1_Nuance_Reflection</code></td><td style="text-align:center;">10</td><td>Report addresses challenges, limitations, ambiguity, and—if present—social/ethical implications.</td></tr>
    <tr><td><code>C1_Bonus_IAA</code></td><td style="text-align:center;">10*</td><td><strong>Bonus:</strong> Formal inter-annotator agreement (Cohen’s Kappa, Krippendorff’s Alpha) reported and interpreted.</td></tr>
  </tbody>
</table>
<p class="muted">* Bonus points may push a team above 50 for C1 before the final multipliers.</p>

<h3>Challenge #2: Modeling &amp; Evaluation (50 points total)</h3>
<table>
  <thead>
    <tr><th>Variable</th><th style="width:70px;text-align:center;">Max</th><th>Definition</th></tr>
  </thead>
  <tbody>
    <tr><td><code>C2_Model_Performance</code></td><td style="text-align:center;">15</td><td>Precision, recall, and F1-score reported; confusion matrix included.</td></tr>
    <tr><td><code>C2_Use_Gold_Dataset</code></td><td style="text-align:center;">10</td><td>Used provided gold standard dataset correctly (no data leakage, correct splits).</td></tr>
    <tr><td><code>C2_Training_Pipeline</code></td><td style="text-align:center;">10</td><td>Training process documented (hyperparameters, train/test/val split, reproducibility).</td></tr>
    <tr><td><code>C2_Error_Analysis</code></td><td style="text-align:center;">10</td><td>Identifies error patterns; gives 3–5 FP/FN examples with reasoning.</td></tr>
    <tr><td><code>C2_Documentation</code></td><td style="text-align:center;">5</td><td>Code is clear, well-structured, and reproducible (e.g., runnable Colab/README).</td></tr>
    <tr><td><code>C2_Bonus_UnseenData</code></td><td style="text-align:center;">10*</td><td><strong>Bonus:</strong> Model tested on new, manually annotated unseen data; performance reported and reflected on.</td></tr>
  </tbody>
</table>
<p class="muted">* Bonus points may push a team above 50 for C2 before the final multipliers.</p>

<section>
  <h2>Variables</h2>
  <table>
    <thead><tr><th>Variable</th><th>Meaning</th></tr></thead>
    <tbody>
      <tr><td><code>Initial_Team_Size</code></td><td>Members at the start of the competition.</td></tr>
      <tr><td><code>Remaining_Team_Members</code></td><td>Members who completed the competition.</td></tr>
      <tr><td><code>Dropouts</code></td><td>Members who left.</td></tr>
      <tr><td><code>Initial_Coding_Experience</code></td><td>Initial count with prior coding experience.</td></tr>
      <tr><td><code>Remaining_Coding_Experience</code></td><td>Remaining count with coding experience.</td></tr>
      <tr><td><code>Initial_Antisemitism_Knowledge</code></td><td>Initial count with prior antisemitism knowledge.</td></tr>
      <tr><td><code>Remaining_Antisemitism_Knowledge</code></td><td>Remaining count with antisemitism knowledge.</td></tr>
      <tr><td><code>Total_Score</code></td><td>Sum of all C1 and C2 scoring components.</td></tr>
      <tr><td><code>Final_Score</code></td><td>Final score after cohesion and capacity multipliers (see formulas).</td></tr>
    </tbody>
  </table>
  <p class="muted">Note: Antisemitism and coding knowledge are inferred from application responses.</p>
</section>

<section>
  <h2>Formulas</h2>

  <h3>1) Base Score</h3>
  <div class="eq">
  $$
  \text{Total\_Score} = \sum \text{C1\_items} + \sum \text{C2\_items}
  $$
    <p class="muted"><strong>In other words:</strong> We just add up all points from Challenge 1 and Challenge 2 (including bonuses).</p>
  </div>

  <h3>2) Team Cohesion Multiplier</h3>
  <p>Rewards teams that retained members through to submission.</p>
  <div class="eq">
  $$
  \text{Cohesion\_Multiplier} = 1 + \alpha \times \left(\frac{\text{Remaining\_Team\_Members}}{\text{Initial\_Team\_Size}} - 1\right)
  $$
    <p class="muted"><strong>In other words:</strong> If nobody dropped out this equals 1. However the Cohesion Multiplier shrinks in proportion to proportion of teammats lost.</p>

  </div>
  <p class="muted">If all members remain, the ratio is 1 and the multiplier is 1. Fewer remaining members lower the multiplier. We use \(\alpha = 1.0\) by default.</p>

  <h3>3) Skill Retention (Capacity) Multiplier</h3>
  <div class="eq">
  $$
  \text{Capacity\_Multiplier} =
  0.5 \times \frac{\text{Remaining\_Coding\_Experience}}{\text{Initial\_Coding\_Experience}} +
  0.5 \times \frac{\text{Remaining\_Antisemitism\_Knowledge}}{\text{Initial\_Antisemitism\_Knowledge}}
  $$
    <p class="muted"><strong>In other words:</strong> Average two fractions—how much coding skill the teams kept and how much prior knowledge on antisemitism the teams kept (50/50).</p>
  </div>

  <h3>4) Final Score</h3>
  <div class="eq">
  $$
  \text{Final\_Score} = \text{Total\_Score} \times \text{Cohesion\_Multiplier} \times \text{Capacity\_Multiplier}
  $$
    <p class="muted"><strong>In Other words</strong> We take the base score and scale it by the two multipliers—teams that stayed intact and kept skills retain more of their points.</p>

  </div>
</section>

---

## Here is an example of how we handled the evaluation based on Team 2's scores.

**Inputs:**
- Total_Score = 115  
- Initial_Team_Size = 5  
- Remaining_Team_Members = 3 (2 dropouts)  
- Initial_Coding_Experience = 3, Remaining_Coding_Experience = 2  
- Initial_Antisemitism_Knowledge = 3, Remaining_Antisemitism_Knowledge = 1  
- α = 1.0  

**Step 1 — Cohesion Multiplier**  
$$
\text{Cohesion\_Multiplier} = 1 + \left(\frac{3}{5} - 1\right) = 0.6
$$

**Step 2 — Capacity Multiplier**  
$$
\text{Capacity\_Multiplier} =
0.5 \times \frac{2}{3} + 0.5 \times \frac{1}{3}
= 0.3333 + 0.1667 \approx 0.6667
$$

**Step 3 — Final Score**  
$$
\text{Final\_Score} = 115 \times 0.6 \times 0.6667 \approx 46.0
$$

**Interpretation:**  
While Team 2 produced strong deliverables, a 40% reduction in team size and loss of topical expertise reduced their final ranking.

---
