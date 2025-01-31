---
title: "Projects"
permalink: /projects/
author_profile: true
---
{% include base_path %}

    
<div class="project-container">
  <div class="project">
    <h2>RAD-Attack: Regularized Adversarial White-Box Attacks on VLMs</h2>
    <div class="content">
      <div class="thumbnail">
        <img src="../images/rad-attack.webp" alt="Project Image" />
      </div>
      <div class="details">
        <p><strong>Authors:</strong> Ganesh Nanduru, Nate Kimball, Alex Fetea </p>
        <p>We trick Meta AI's LLaVa model into misclassifying digits with minimal perturbations!</p>
        <p>
          <a target="_blank" href="https://github.com/nanduruganesh/rad-attack/blob/main/report.pdf">Paper</a> | 
          <a target="_blank" href="https://github.com/nanduruganesh/rad-attack">Code</a>
        </p>
      </div>
    </div>
  </div>
</div>

<br>

<div class="project-container">
  <div class="project">
    <h2>Cognitively Inspired Energy-Based World Models</h2>
    <div class="content">
      <div class="thumbnail">
        <img src="../images/ciebwm.webp" alt="Project Image" />
      </div>
      <div class="details">
        <p><strong>Authors:</strong> Alexi Gladstone, Ganesh Nanduru, Md Mofijul Islam, Aman Chadha, Jundong Li, Tariq Iqbal </p>
        <p>We train an energy-based model inspired by System 2 thinking that scales better than traditional autoregressive transformers with respect to data and GPU hours in computer vision tasks.</p>
        <p>
          <a target="_blank" href="https://arxiv.org/abs/2406.08862">Paper</a>
          <!-- <a target="_blank" href="https://github.com/nanduruganesh/rad-attack">Code</a> -->
        </p>
      </div>
    </div>
  </div>
</div>

<br>

<div class="project-container">
  <div class="project">
    <h2>COVID-19 Tracker</h2>
    <div class="content">
      <div class="thumbnail">
        <img src="../images/covidmap.webp" alt="Project Image" />
      </div>
      <div class="details">
        <p><strong>Authors:</strong> 
          <span id="authorList"></span><span id="moreAuthors" class="hidden" onclick="hideAllAuthors()"></span>
          <span id="moreLink" class="clickable" onclick="showAllAuthors()"></span>
        </p>
        <p>An interactive COVID-19 casemap, color coded with AI-classified case trends. </p>
        <p>
          <a target="_blank" href="https://covid19-map.com/">Website</a> |
          <a target="_blank" href="https://github.com/nanduruganesh/CoronaTrackerAPI">Code (Data Collection)</a>
        </p>
      </div>
    </div>
  </div>
</div>

<br>

<div class="project-container">
  <div class="project">
    <h2>PCAP-LM</h2>
    <div class="content">
      <div class="thumbnail">
        <img src="../images/ddos.webp" alt="Project Image" />
      </div>
      <div class="details">
        <p><strong>Authors:</strong> Ganesh Nanduru, Christopher Johnson </p>
        <p>We trained an LLM to read network traffic, to detect and explain potential DDoS attacks! </p>
        <p>
          <a target="_blank" href="https://github.com/nanduruganesh/pcaplm/blob/master/Network_Security_Final_Project.pdf">Paper</a> |
          <a target="_blank" href="https://github.com/nanduruganesh/pcaplm">Code</a>
        </p>
      </div>
    </div>
  </div>
</div>

<br>

<div class="project-container">
  <div class="project">
    <h2>Video Swin Transformer for Medical Image Regression</h2>
    <div class="content">
      <div class="thumbnail">
        <img src="../images/tos_curve.webp" alt="Project Image" />
      </div>
      <div class="details">
        <p><strong>Authors:</strong> Ganesh Nanduru, Sravanth Potluri, Rahul Reddy, Swakshar Deb </p>
        <p>We trained a 3D Swin Transformer to map videos of heart palpitations to their time-of-systole heartbeat curves, then compared results with a traditional CNN.</p>
        <p>
          <a target="_blank" href="https://github.com/nanduruganesh/SwinTransformer/blob/main/MLIA___Final_Project-2.pdf">Paper</a> | 
          <a target="_blank" href="https://github.com/nanduruganesh/SwinTransformer">Code</a>
        </p>
      </div>
    </div>
  </div>
</div>

<br>

<!-- Style and script below are for the clickable "and x more" authors for covid map -->
<style>
        .hidden { display: none; }
        .clickable { color: gray; cursor: pointer; text-decoration: underline; }
        .clickable2 { cursor: pointer; text-decoration: underline; }
</style>
<script>
    const authors = [
        "Ganesh Nanduru", "Daniel Stefanescu", "Srikar Gouru", "Grace Tang",
        "Rashad Philizaire", "Maxwell Bai", "Alexander Talamonti", "Amber Garcha", "Alby Alex"
    ];
    
    const visibleCount = 3;
    const authorListEl = document.getElementById("authorList");
    const moreAuthorsEl = document.getElementById("moreAuthors");
    const moreLinkEl = document.getElementById("moreLink");

    function renderAuthors() {
        authorListEl.innerHTML = authors.slice(0, visibleCount).join(", ");
        if (authors.length > visibleCount) {
            moreAuthorsEl.innerHTML = ", " + authors.slice(visibleCount).join(", ");
            moreLinkEl.innerHTML = `and ${authors.length - visibleCount} more`;
        }
    }

    function showAllAuthors() {
      moreAuthorsEl.classList.remove("hidden");
      moreAuthorsEl.classList.add("clickable2");
      moreLinkEl.classList.add("hidden");
    }

    function hideAllAuthors() {
      moreAuthorsEl.classList.remove("clickable2");
      moreAuthorsEl.classList.add("hidden");
      moreLinkEl.classList.remove("hidden");
    }

    renderAuthors();

    
</script>

<style>
.project-container {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.project {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.project h2 {
  margin: 0 0 0.5rem;
}

.content {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  gap: 1rem;
}

.thumbnail img {
  max-width: 150px; /* Adjust thumbnail size */
  border-radius: 8px; /* Optional: rounded corners */
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* Optional: shadow for the image */
}

.details {
  flex: 1; /* Ensures text occupies the remaining space */
}

.details p {
  margin: 0.5rem 0;
}

.details a {
  color: #007bff; /* Optional: link color */
  text-decoration: none;
}

.details a:hover {
  text-decoration: underline;
}
</style>