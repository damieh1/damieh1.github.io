---
title: "Datathon 2025 Scoring"
permalink: /evaluation/
layout: single
mathjax: true
classes: wide
---

<!-- Page-specific styles -->
<style>
  :root {
    --bg: #ffffff;
    --fg: #1f2937;
    --muted: #6b7280;
    --accent: #2563eb;
    --card: #f9fafb;
    --border: #e5e7eb;
  }
  .mm-page #main { background: var(--bg); color: var(--fg); }
  .container { max-width: 980px; margin: 0 auto; }
  .card { background: var(--card); border: 1px solid var(--border); border-radius: 14px; padding: 1rem 1.25rem; }
  .muted { color: var(--muted); }
  code, kbd { background: #f3f4f6; padding: .15rem .35rem; border-radius: 6px; }
  .eq { background: #fff; border-left: 3px solid var(--accent); padding: .75rem 1rem; border-radius: 8px; overflow-x: auto; }
  table { width: 100%; border-collapse: collapse; margin: 1rem 0; }
  th, td { padding: .6rem .5rem; border-bottom: 1px solid var(--border); vertical-align: top; }
  th { text-align: left; font-weight: 700; }
  .pill { display: inline-block; padding: .2rem .5rem; border-radius: 999px; background: #eef2ff; color: #3730a3; font-weight: 600; font-size: .8rem; }
  .callout { border: 1px solid var(--border); background: #fff; border-radius: 12px; padding: 1rem; }
  details { background: #fff; border: 1px solid var(--border); border-radius: 10px; padding: .5rem .75rem; }
  details > summary { cursor: pointer; font-weight: 600; }
</style>

<header>
  <h1>Fair Scoring Methodology</h1>
  <p class="muted">Evaluating performance, team cohesion, and skill retention transparently.</p>
</header>

<section class="card">
  <h2>Overview</h2>
  <p>
    We evaluate teams across two challenges (C1 and C2). Scores reflect both the
    <strong>quality of deliverables</strong> and the ability to <strong>maintain team capacity</strong> despite dropouts.
  </p>
  <p>
    The final score combines a <span class="pill">Base Score</span>, a
    <span class="pill">Team Cohesion Multiplier</span>, and a
    <span class="pill">Skill Retention (Capacity) Multiplier</span>.
  </p>
</section>

<section>
  <h2>Variables</h2>
  <table>
    <thead>
      <tr><th>Variable</th><th>Meaning</th></tr>
    </thead>
    <tbody>
      <tr><td><code>C1_Relevance_Variety</code></td><td>Relevance and variety of data selected in Challenge 1.</td></tr>
      <tr><td><code>C1_Annotation_Schema</code></td><td>Clarity and quality of the annotation schema (C1).</td></tr>
      <tr><td><code>C1_Internal_Consistency</code></td><td>Internal consistency of annotations (C1).</td></tr>
      <tr><td><code>C1_Data_Report_Quality</code></td><td>Quality/completeness of the data report (C1).</td></tr>
      <tr><td><code>C1_Nuance_Reflection</code></td><td>Reflection on nuance in annotations (C1).</td></tr>
      <tr><td><code>C1_Bonus_IAA</code></td><td>Bonus for high inter-annotator agreement (C1).</td></tr>
      <tr><td><code>C2_Model_Performance</code></td><td>Model performance (C2).</td></tr>
      <tr><td><code>C2_Use_Gold_Dataset</code></td><td>Appropriate use of the provided gold dataset (C2).</td></tr>
      <tr><td><code>C2_Training_Pipeline</code></td><td>Completeness/quality of the training pipeline (C2).</td></tr>
      <tr><td><code>C2_Evaluation</code> or <code>C2_Error_Analysis</code></td><td>Quality of evaluation or error analysis (C2).</td></tr>
      <tr><td><code>C2_Nuance_Reflection</code></td><td>Reflection on nuance in outputs (C2).</td></tr>
      <tr><td><code>C2_Overall_Quality</code> / <code>C2_Documentation</code></td><td>Overall quality and/or documentation quality (C2).</td></tr>
      <tr><td><code>Initial_Team_Size</code></td><td>Members at the start of the competition.</td></tr>
      <tr><td><code>Remaining_Team_Members</code></td><td>Members who completed the competition.</td></tr>
      <tr><td><code>Dropouts</code></td><td>Members who left (computed or provided).</td></tr>
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
  </div>

  <h3>2) Team Cohesion Multiplier</h3>
  <p>Rewards teams that retained members through to submission.</p>
  <div class="eq">
  $$
  \text{Cohesion\_Multiplier} = 1 + \alpha \times \left(\frac{\text{Remaining\_Team\_Members}}{\text{Initial\_Team\_Size}} - 1\right)
  $$
  </div>
  <p class="muted">If all members remain, the ratio is 1 and the multiplier is 1. Fewer remaining members lower the multiplier. We use \(\alpha = 1.0\) by default.</p>

  <h3>3) Skill Retention (Capacity) Multiplier</h3>
  <p>Balances technical and topical expertise retained to completion.</p>
  <div class="eq">
  $$
  \text{Capacity\_Multiplier} =
  0.5 \times \frac{\text{Remaining\_Coding\_Experience}}{\text{Initial\_Coding\_Experience}} +
  0.5 \times \frac{\text{Remaining\_Antisemitism\_Knowledge}}{\text{Initial\_Antisemitism\_Knowledge}}
  $$
  </div>

  <h3>4) Final Score</h3>
  <div class="eq">
  $$
  \text{Final\_Score} = \text{Total\_Score} \times \text{Cohesion\_Multiplier} \times \text{Capacity\_Multiplier}
  $$
  </div>

  <details>
    <summary>Rationales</summary>
    <div class="callout">
      <ul>
        <li><strong>Quality first:</strong> The base score preserves the importance of the deliverables.</li>
        <li><strong>Retention matters:</strong> Teams that stayed intact receive proportional credit.</li>
        <li><strong>Skill mix:</strong> Retaining both coding and antisemitism knowledge is valued equally.</li>
        <li><strong>Transparent & reproducible:</strong> All terms and coefficients are explicit.</li>
      </ul>
    </div>
  </details>
</section>

<section>
  <h2>Worked Example (Team 2)</h2>
  <div class="card">
    <p><strong>Inputs</strong></p>
    <ul>
      <li><code>Total_Score = 115</code></li>
      <li><code>Initial_Team_Size = 5</code>, <code>Remaining_Team_Members = 3</code> → 2 dropouts</li>
      <li><code>Initial_Coding_Experience = 3</code>, <code>Remaining_Coding_Experience = 2</code></li>
      <li><code>Initial_Antisemitism_Knowledge = 3</code>, <code>Remaining_Antisemitism_Knowledge = 1</code></li>
      <li>\(\alpha = 1.0\)</li>
    </ul>
    <p><strong>Step 1 — Cohesion</strong></p>
    <div class="eq">
    $$
    \text{Cohesion\_Multiplier} =
    1 + \left(\frac{3}{5} - 1\right) = 0.6
    $$
    </div>
    <p><strong>Step 2 — Capacity</strong></p>
    <div class="eq">
    $$
    \text{Capacity\_Multiplier} =
    0.5 \times \frac{2}{3} + 0.5 \times \frac{1}{3}
    = \frac{1}{2} \approx 0.6667
    $$
    </div>
    <p><strong>Step 3 — Final Score</strong></p>
    <div class="eq">
    $$
    \text{Final\_Score} = 115 \times 0.6 \times 0.6667 \approx 46.0
    $$
    </div>
    <p class="muted">
      Interpretation: strong deliverables, but a 40% team size reduction and loss of expertise lowered the final result.
    </p>
  </div>
</section>

<section>
  <h2>Implementation Notes</h2>
  <ul>
    <li>Compute <code>Total_Score</code> by summing all <code>C1_*</code> and <code>C2_*</code> columns.</li>
    <li>Set \(\alpha\) to adjust how strongly dropouts affect scores (default \(\alpha = 1.0\)).</li>
    <li>Handle zero denominators (e.g., if a team reported 0 initial expertise) by defining the ratio as 1 when both initial and remaining are 0, or 0 when initial is 0 but remaining &gt; 0 (state your convention).</li>
  </ul>
</section>
