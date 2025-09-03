# Exercises

# Simple Landing Page

Create a simple landing page for a fictional e-commerce site that sells tech gadgets. The page should include a navigation bar, a grid-based product listing section, and a footer. 

1. Use semantic HTML elements like `<header>`, `<nav>`, `<main>`, `<section>`, and `<footer>` to structure your webpage.
2. Include a navigation bar with links to "Home", "Products", "About Us", and "Contact".
3. Create a product section using a grid layout to display at least 6 products with images, names, and prices.
4. Add a footer with links to privacy policy, terms of service, and social media icons.

5. Implement Responsive Design:
- Use media queries to create at least two breakpoints: tablet (768px to 1023px), and desktop (1024px and above)
- Use relative units (em, rem, %, vh, vw) for sizing elements where appropriate
- Implement a responsive hero section at the top of the page with a background image and overlay text

# Styling List

Create an HTML file with an ordered list of at least 5 college events. Each event should include the event name, time, and location as nested unordered list.

Style the list using CSS to make it stand out:
- Use custom bullets or numbers instead of default ones
- Add hover effects that change the color of the text or background when the user hovers over an event.
- Include spacing and padding to ensure the list is easy to read.

# Styling table

Create an HTML table to keep track of your grades throughout the semester. You should list all your modules, assignments, exams, and their respective scores. The table should include the following columns:
- Module
- Assignment/Exam Name
- Maximum Marks
- Marks Obtained
- Percentage
- Grade

Example: 
Module: "SDA101" - Assignment 1: "Figma Design" - Max Marks: 10 - Marks Obtained: 7 - Percentage: 70% - Grade: B

---
###
---
# Hostel Room Maintenance Request Form

Create an HTML form for hostel room maintenance requests and style it using CSS. Include information like name, room number, type of issue, description, urgency etc.

Some suggestions while styling the form:
- Style the form to have a clean, modern look.
- Incorporate appropriate input types and placeholders
- Use an appropriate color scheme that's easy on the eyes.
- Style form inputs consistently, including on focus states.
- Make the submit button stand out.

## **Sample Sections**

### **Full Name**
- **Input type**: `text`
- **Requirements**: Required, 2-50 characters, pattern validation for letters and spaces only
- **Placeholder**: "Enter your full name"

### **Student ID**
- **Input type**: `number` or `text` with pattern
- **Requirements**: Required, exactly 8 digits, numeric validation
- **Placeholder**: "02250123"

### **Email Address**
- **Input type**: `email`
- **Requirements**: Required, valid email format
- **Placeholder**: "student.cst@rub.edu.bt"

### **Phone Number**
- **Input type**: `tel`
- **Requirements**: Required, phone pattern validation
- **Placeholder**: "12345678"

---

## **Room Information Section**

### **Block/Building Name**
- **Input type**: `select` dropdown
- **Options**: Block A, Block B, Block C, Block F, RK
- **Requirements**: Required selection

### **Room Number**
- **Input type**: `number`
- **Requirements**: Required, range 100-999
- **Placeholder**: "Room number (e.g., 205)"

### **Floor Number**
- **Input type**: `number`
- **Requirements**: Required, range 1-10
- **Placeholder**: "Floor number"

---

## **Issue Details Section**

### **Type of Issue**
- **Input type**: `select` dropdown with grouped options
- **Categories**:
  - Electrical
  - Plumbing
  - Furniture
  - Infrastructure
  - Cleaning
  - Other


### **Issue Priority/Urgency**
- **Input type**: `radio` buttons
- **Options**:
  - Emergency (Immediate attention required)
  - High (Within 24 hours)
  - Medium (Within 3 days)
  - Low (Within a week)
- **Requirements**: Required selection

### **Issue Description**
- **Input type**: `textarea`
- **Requirements**: Required, 20-500 characters, word counter
- **Placeholder**: "Please describe the issue in detail..."
- **Attributes**: `rows="5" cols="50"`
