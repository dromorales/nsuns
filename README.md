# Interactive nSuns 5-Day Workout Planner

An interactive 5-day nSuns workout planner built with HTML, Tailwind CSS, and vanilla JavaScript. This single-page application allows you to enter your 1 Rep Max (1RM) for the main lifts (Bench Press, Squat, Overhead Press, Deadlift) and automatically calculates your weekly workout schedule based on a specified Training Max percentage.

## Features

- **Dynamic Weight Calculation:** Enter your 1RMs and a Training Max (TM) percentage to automatically calculate all working weights for your T1 and T2 lifts.
- **Interactive Daily View:** Easily switch between the 5 workout days to see the specific sets, reps, and weights for the day.
- **Calculated TM Display:** The app shows you the calculated Training Max for each main lift based on your inputs, providing full transparency.
- **Print-Friendly:** A clean, responsive layout that's optimized for printing. The print version displays the full week's schedule along with your calculated TMs.

## How to Use

1.  Clone or download this repository.
2.  Open the `index.html` file in your web browser.
3.  Enter your current 1 Rep Max (1RM) values for the four main lifts.
4.  Adjust the Training Max (TM) percentage if desired (90% is standard).
5.  Click "Update Weights".
6.  Your workout plan is now ready to use or print.

## Technologies Used

- HTML5
- [Tailwind CSS](https://tailwindcss.com/) (via CDN)
- Vanilla JavaScript (ES6)

## Customization

The T1 and T2 lift percentages are defined in the `<script>` block within `index.html` in the `liftTemplates` object. You can modify these percentages to suit your specific nSuns variation.

```javascript
const liftTemplates = {
  t1: [
    { percentage: 0.75, reps: "5" },
    { percentage: 0.85, reps: "3" },
    // ... and so on
  ],
  t2: [
    { percentage: 0.55, reps: "6" },
    { percentage: 0.65, reps: "5" },
    // ... and so on
  ],
};
```
