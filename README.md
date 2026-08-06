# DMI Portfolio Website (Static HTML/CSS)

This repository contains a clean, professional-looking **static portfolio website** used in **DevOps Micro Internship (DMI)** Week 1 to practice:
- Linux basics
- Nginx hosting
- Deployment proof / ownership
- Production-style checks

✅ Students deploy this website on an Ubuntu VM using Nginx and keep it live for 24 hours.

---

## Who is this for?
- DMI students (beginner → intermediate)
- Anyone learning how to host a static site with Nginx on Linux

---

## What you will build
A portfolio-style website hosted on:
- **Ubuntu VM**
- **Nginx**
- Accessible via: `http://<public-ip>`

---

## Mandatory Ownership Proof (DMI Rule)
Before you deploy, you MUST edit the footer and add your details:

Original:

```html
<p>Crafted with <span>cloud</span> excellence by Pravin Mishra</p>
```

Add this line (example):

```html
<p><strong>Deployed by:</strong> DMI Cohort 3 | Saima Usman | Group 2 | Week 5 | 06-08-2026</p>
```

✅ This proof must be visible in your browser screenshot submission.

## Dynamic Deployment Date

The website footer displays the deployment date automatically using JavaScript.

### Implementation

A `<span>` element is used as a placeholder for the deployment date.

```html
<span id="deployDate"></span>
```

JavaScript generates the current date in **DD Mon YYYY** format and inserts it into the footer when the page loads.

```javascript
const today = new Date();

const options = {
  day: "2-digit",
  month: "short",
  year: "numeric"
};

document.getElementById("deployDate").textContent =
  today.toLocaleDateString("en-GB", options);
```

Example output:

```
Last Deployment: 07 Aug 2026
```