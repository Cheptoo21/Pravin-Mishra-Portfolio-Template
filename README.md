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
<p>
  <strong>Deployed by:</strong> DMI Cohort 2 | Rahul Sharma | Group 4 | Week 1 |
  16-01-2026
</p>
```

✅ This proof must be visible in your browser screenshot submission.

## Footer requirement

The website footer must display today’s date automatically instead of a static hard-coded value.

## How the date is generated

The date is generated on the client side using JavaScript.
When the page loads, a script reads the current system date and injects it into the footer.

## Code snippet

<footer>
  <p>
    © <span id="deployDate"></span> Pravin Mishra. All rights reserved.
  </p>
</footer>

<script>
  const dateElement = document.getElementById("deployDate");

  const today = new Date();

  const options = {
    day: "2-digit",
    month: "short",
    year: "numeric"
  };

  dateElement.textContent = today.toLocaleDateString("en-GB", options);
</script>
