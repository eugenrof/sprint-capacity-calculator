# SprintCap | Sprint Capacity Planner

A lightweight, logic-driven tool built to simplify the "planning math" that often slows down Scrum teams. 

Most teams rely on complex, fragile spreadsheets to calculate capacity. **SprintCap** offers a reactive, browser-based alternative to help practitioners gain clear visibility into team commitment based on real-world availability.

[![GitHub Pages](https://img.shields.io/badge/Live-Demo-brightgreen?style=for-the-badge&logo=github)](https://eugenrof.github.io/sprint-capacity-planner)

## 📋 Purpose & Professional Impact

In the **Scrum Framework**, the Sprint Planning event is the heartbeat of a team's cycle. However, one of the most persistent challenges for a **Scrum Master** is moving a team from "gut feeling" to data-driven commitment.

**Sprint Capacity Planner** was developed as a specialized utility to bridge the gap between abstract story points and concrete human availability. By providing a structured, mathematical approach to team capacity, it ensures that the "Forecast" made at the beginning of a sprint is both realistic and sustainable.

### Why this tool?
As a **Professional Scrum Master (PSM II)**, I found that planning sessions often lost momentum due to manual calculations. I wanted to create a utility that respects the Scrum framework while removing the administrative friction of calculating man-days, focus factors, and public holidays.

* **Precision Planning**: Replaces vague estimates with a concrete "Available Days" metric, allowing the team to see exactly how holidays and personal leave impact their delivery power.
* **Efficiency**: Reduces the time spent on manual spreadsheets or fighting complex configurations in heavy Jira/Azure DevOps environments during live planning sessions.
* **Transparency**: Provides a visual, shareable "source of truth" that helps **Product Owners** and stakeholders understand exactly why a team’s velocity might fluctuate in a specific sprint (e.g., due to public holidays or team training).
* **Zero Overhead**: A focused, high-utility micro-app designed for immediate, zero-setup capacity modeling that can be exported or shared instantly.
* **Mobile-First Design**: Optimized for any device. Whether on a desktop monitor or a mobile phone during a breakout session, the interface scales seamlessly for data entry.

## 📊 Reference Baseline

The application initializes with a **pre-configured reference model** to demonstrate its logic in a live scenario. These values are intended as a functional starting point and should be adjusted to reflect your specific team context:

* **Team Composition**: Modeled for a standard cross-functional squad of **5 Developers**.
* **Sprint Cadence**: Set to a **3-week cycle** (15 working days), accounting for modern continuous delivery rhythms.
* **Baseline Velocity**: Initialized at **45 Story Points**, representing a historical average.

> [!IMPORTANT]
> These figures serve as a **benchmarking reference** rather than a prescriptive "golden standard." The tool is designed to be agnostic of team size, sprint length, or estimation units (Points, Hours, or Ideal Days), allowing you to calibrate it to your unique environment.

---

## 👥 Target Audience

This tool is specifically crafted for professionals operating within Agile and Scrum environments:

* **Scrum Masters & Agile Coaches**: To facilitate smoother, data-backed Sprint Planning sessions and protect the team from over-commitment.
* **Team Leads & Engineering Managers**: To model various "what-if" scenarios regarding team allocation and upcoming leave.
* **Self-Organizing Development Teams**: To take ownership of their own capacity and provide more accurate forecasts to their stakeholders.

---

## 📂 Project Structure

```text
sprint-capacity-planner/
├── images/
│   ├── favicon.ico          # Browser tab icon
│   └── share-preview.png    # Open Graph (OG) social media image
├── index.html               # Main application structure & SEO meta tags
├── script.js                # Core logic, state management & PDF engine
├── style.css                # Custom glassmorphism & Tailwind extensions
└── README.md                # Project documentation and methodology
```
---

## Key Features
- **Privacy-First:** No accounts, no databases, and no tracking. All data is processed locally in your browser.
- **Smart State Persistence:** Your configuration is automatically saved in your local storage.
- **Deep-Link Sharing:** Generate a unique URL (Base64 encoded) to share your specific capacity plan with team members or stakeholders.
- **Scrum Guardrails:** Built-in guidance for optimal team sizes (Scrum Guide alignment) and real-time velocity adjustments.
- **Professional Reporting:** Export your capacity plan to a clean PDF for Sprint documentation.

---

## 🧪 Technical Insights

### The Calculation Engine

To ensure maximum compatibility across all Markdown viewers, the tool uses the following logic for real-time modeling:

1. **Working Window** `Sprint Days - Public Holidays`

2. **Individual Availability** `(Working Window - Individual Days Off) × (Allocation % / 100)`

3. **Team Capacity %** `Total Available Days / (Team Size × Sprint Days)`

4. **Recommended Velocity** `Average Velocity × Team Capacity %`

### Technical Stack
- **Frontend:** HTML5, Tailwind CSS
- **Interactivity:** Vanilla JavaScript (ES6+)
- **Libraries:** Flatpickr (Date handling), jsPDF (PDF generation)
- **Deployment:** Netlify

---

## 💡 Usage Pro-Tips

* **Direct Editing**: You can click directly on member names in the table to rename them on the fly.
* **Visual Indicators**: The capacity bar changes color based on team health:
    * 🟢 **High**: $\ge$ 75% Capacity
    * 🟠 **Mid**: 50% - 74% Capacity
    * 🔴 **Low**: < 50% Capacity
* **Global Reset**: Use the "Reset Table Data" button to clear all custom inputs and return to the default team structure.

---

## ⚖️ License & Credits 
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📝 About the Author
I am a **Senior QA Engineer** and a certified **Professional Scrum Master (PSM I & PSM II)**, with a passion for testing & building tools that enhance team agility and transparency. This project was born out of a personal need and is shared freely for the Agile community.

If you have suggestions or find this tool helpful in your Sprints, feel free to explore the code or reach out via GitHub.

---
*Built for practitioners, by a practitioner.*

Developed by **Eugen Rof** (2026). Part of the **Scrum Master Toolset**.
[GitHub Repository](https://github.com/eugenrof/sprint-capacity-planner)
