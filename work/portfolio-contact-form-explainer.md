# Portfolio Contact Form — Plain-Words Explanation

## What I added

I added one dynamic feature to my portfolio: a working contact form.

The purpose of the form is to allow a visitor to send me a message directly from my portfolio instead of only viewing my projects and profile.

## What is a backend?

A backend is the part of an application that handles work behind the interface that the user sees.

For a simple website, the frontend is what the visitor interacts with: the page, buttons, text fields, and form.

The backend or backend service receives and processes information submitted by the frontend.

For this feature, I did not build a custom backend server. I used Netlify's form handling service so that the portfolio can receive form submissions without me maintaining a separate server.

## How my contact form works

The visitor opens my portfolio and fills in three fields:

- Name
- Email
- Message

When the visitor clicks "Send Message", the browser submits the form.

The form is configured for Netlify's form handling. Netlify receives the submitted form data and records the submission.

I can then view the submitted information through my Netlify site dashboard.

The basic data flow is:

Visitor
→ Contact form
→ Browser sends form data
→ Netlify receives the submission
→ Submission becomes available to me

## Why I chose this feature

I chose a contact form because my portfolio is mainly a professional profile and project showcase.

A visitor who is interested in working with me needs a simple way to contact me.

I also wanted the feature to be small enough that I could understand how it works instead of adding several features that I could not properly explain.

## What I tested

I deployed the feature to my live portfolio and submitted a real test message.

I then checked the Netlify form submissions to confirm that the data reached the service successfully.

This confirmed that the feature works end to end.

## What I learned

The main thing I learned is that a website does not have to contain a large custom backend to have dynamic behavior.

A static page can send information to a backend service through a form request, and that service can process and store the submission.

This helped me understand the difference between what happens in the browser and what happens after the browser sends data to a server-side service.
