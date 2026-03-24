# Projects

## 2025–2026

### Video Game Price Analysis

A data science project analyzing whether Steam video game prices in the European market have kept pace with inflation over the past decade (2015–2024), and how COVID-19 affected pricing strategies. I deliberately chose a domain I knew well so I could ask the right questions—like whether psychological price points and game tier composition were shifting alongside broader trends—and spot when a finding needed deeper investigation.

[View the interactive analysis notebooks →](https://jbenigeri.github.io/Video-Game-Price-Analysis/) | [GitHub](https://github.com/jbenigeri/Video-Game-Price-Analysis)

#### Part 1: Exploratory Data Analysis
[View Notebook →](https://jbenigeri.github.io/Video-Game-Price-Analysis/nb1-exploratory-data-analysis/)

Cleaned and merged Steam sales data with Eurostat HICP indices, filtered to 2015–2024 for meaningful trend analysis. Covers correlation analysis, platform availability patterns, and price distributions across Windows, Linux, and MacOS.

<a href="https://jbenigeri.github.io/Video-Game-Price-Analysis/nb1-exploratory-data-analysis/">
  <img src="images/sec_4-3_price_distribution_by_platform.png" alt="Price Distribution by Platform" width="300">
</a>

#### Part 2: Price & Inflation Analysis
[View Notebook →](https://jbenigeri.github.io/Video-Game-Price-Analysis/nb2-prices-analysis/)

Adjusted prices using HICP to compare real versus nominal trends over time, and used statistical modeling to measure how pricing shifted across periods. Covers COVID-19 impact analysis (2020–2022), price tier composition over time, and psychological price point patterns.

<div class="image-row">
<a href="https://jbenigeri.github.io/Video-Game-Price-Analysis/nb2-prices-analysis/">
  <img src="images/sec_5-1_tier_composition.png" alt="Tier Composition">
</a>
<a href="https://jbenigeri.github.io/Video-Game-Price-Analysis/nb2-prices-analysis/">
  <img src="images/sec_5-2_price_evolution.png" alt="Price Evolution">
</a>
<a href="https://jbenigeri.github.io/Video-Game-Price-Analysis/nb2-prices-analysis/">
  <img src="images/sec_5-3_covid_impact.png" alt="COVID Impact">
</a>
</div>

---

### Hand Gesture Detection

A demo of my own version of Zoom's hand gesture detection feature: **real-time detection of 9 common video call gestures (👍 👎 ✋ 👏 ✌️ 👌 👆 🤘 ✊) with emoji reactions displayed on screen.**

[GitHub](https://github.com/jbenigeri/Hand-Gestures-Detection)

<a href="https://github.com/jbenigeri/Hand-Gestures-Detection">
  <img src="images/demo.gif" alt="Hand Gesture Recognition Demo">
</a>

I started with a rules-based approach: [MediaPipe](https://github.com/google-ai-edge/mediapipe/blob/master/docs/solutions/hands.md) tracks 21 points on your hand, and simple rules check the geometry between them. For example, "thumb tip is above the thumb base and all other fingers are curled" reliably detects a thumbs-up. But rules struggle with ambiguous gestures. An OK sign 👌 requires the thumb and index finger to be "close enough" to form a circle, and a fixed distance threshold breaks when someone is farther from the camera or forms the gesture loosely.

So I built a data collection tool, recorded labeled samples across varying hand positions, distances, and lighting, and trained a Random Forest classifier that learns to handle that variability from examples instead of hard-coded rules—achieving 98.9% accuracy across all 9 gesture classes. The Streamlit UI provides a live webcam feed, gesture toggle controls, and a statistics dashboard.

LLM coding assistants helped me build fast, but many of the key design decisions were mine. For example, it was my call to drop the rules and switch to ML when I found them to be unreliable.

---

## 2017

### Machine Learning for Handwritten Digit Recognition

**International Summer Science Institute (ISSI) — Weizmann Institute of Science**

Built classifiers for handwritten digit recognition (MNIST) using KNN, SVM, ANN, and CNN. Achieved 99%+ accuracy with the CNN model. Worked with Daniel Burghardt and Viney Kumar, mentored by Itay Safran and Dr. Ohad Shamir. This was my first exposure to machine learning and deep learning.

[View Project Report (PDF, p.106) →](https://www.weizmann.org.uk/assets/site/documents/Reports_ISSI2017.pdf)
