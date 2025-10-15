# Interactive nSuns Workout Planner

An interactive nSuns workout planner built with HTML, Tailwind CSS, and vanilla JavaScript. This single-page application allows you to select between 3-day, 4-day, and 5-day routines. You can enter your 1 Rep Max (1RM) for the main lifts (Bench Press, Squat, Overhead Press, Deadlift) and automatically calculate your weekly workout schedule based on a specified Training Max percentage.

## Features

- **Multiple Routines:** Choose between 3-day, 4-day, and 5-day nSuns workout routines.
- **Dynamic Weight Calculation:** Enter your 1RMs and a Training Max (TM) percentage to automatically calculate all working weights for your T1 and T2 lifts.
- **Interactive Daily View:** Easily switch between the workout days to see the specific sets, reps, and weights for the day.
- **Calculated TM Display:** The app shows you the calculated Training Max for each main lift based on your inputs, providing full transparency.
- **Print-Friendly:** A clean, responsive layout that's optimized for printing. The print version displays the full week's schedule along with your calculated TMs.

## How to Use

1.  Clone or download this repository.
2.  Open the `index.html` file in your web browser.
3.  Select your desired routine (3-day, 4-day, or 5-day).
4.  Enter your current 1 Rep Max (1RM) values for the four main lifts.
5.  Adjust the Training Max (TM) percentage if desired (90% is standard).
6.  Click "Update Weights".
7.  Your workout plan is now ready to use or print.

## Technologies Used

- HTML5
- [Tailwind CSS](https://tailwindcss.com/) (via CDN)
- Vanilla JavaScript (ES6)

## Customization

The T1 and T2 lift percentages are defined in the `<script>` block within `index.html` in the `liftTemplates` object. The workout routines are defined in the `workoutData`, `workoutData4Day`, and `workoutData3Day` objects. You can modify these to suit your specific nSuns variation.

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

const workoutData = {
  day1: {
    title: "Day 1: Bench Press & Overhead Press",
    t1: { name: "Bench Press", liftKey: "bench" },
    t2: { name: "Overhead Press (OHP)", liftKey: "ohp" },
    accessories: [
      "Dumbbell Rows (4x10-12)",
      "Dumbbell Bench Press (3x10-15)",
      "Dumbbell Skullcrushers (3x10-15)",
      "Dumbbell Rear Delt Flyes (3x15-20)",
    ],
  },
  // ... and so on
};
```
