# 🚀 Countdown & Quotes Application

A dynamic JavaScript-based web application featuring a real-time countdown timer, motivational quotes slider, and delayed modal popup.

## 📋 Features

### ⏳ Countdown Timer
- Real-time countdown to New Year (automatically updates to next year)
- Start/Pause toggle functionality
- Automatically stops when countdown reaches zero
- Displays days, hours, minutes, and seconds

### 💬 Motivational Quotes Slider
- 6 inspirational quotes stored in an array
- Automatic rotation every 4 seconds
- Manual navigation with Next/Previous buttons
- Responsive layout that prevents content shifting

### 🖼️ Modal Popup
- Appears automatically after 5 seconds of page load
- Contains a welcome message
- Can be closed with the close button or by clicking outside

## 🛠️ Technologies Used

- **HTML5** - Semantic structure
- **CSS3** - Styling with modern dark theme
- **JavaScript (ES6+)** - Core functionality including:
  - `setInterval()` for countdown and quotes slider
  - `setTimeout()` for delayed modal
  - `clearInterval()` for timer control
  - Arrow functions and template literals
  - DOM manipulation
  - Event handling

## 📁 Project Structure

```
countdown-quotes-app/
├── index.html          # Main HTML file with embedded CSS and JS
├── README.md           # Project documentation
└── screenshots/        # Screenshots of the application (to be added)
```

## 🚀 How to Run

1. **Option 1: Open Directly**
   - Download or copy the `index.html` file
   - Double-click to open in any modern web browser

2. **Option 2: Live Server (Development)**
   ```bash
   # Using VS Code Live Server extension
   # Right-click index.html → "Open with Live Server"
   ```

3. **Option 3: Deploy to GitHub Pages**
   - Create a GitHub repository
   - Upload `index.html` and `README.md`
   - Enable GitHub Pages in repository settings

## 📝 Code Explanation

### 1. **Countdown Timer Implementation**
```javascript
// Set target date (next New Year)
const newYear = new Date().getFullYear() + 1;
const targetDate = new Date(`January 1, ${newYear} 00:00:00`);

// Update countdown every second
setInterval(() => {
  const diff = targetDate - new Date();
  // Calculate and display days, hours, minutes, seconds
}, 1000);
```

### 2. **Quotes Array and Rotation**
```javascript
const quotes = [
  "Success is not final, failure is not fatal...",
  // 5 more quotes
];

// Auto-rotate quotes every 4 seconds
setInterval(() => {
  currentQuoteIndex = (currentQuoteIndex + 1) % quotes.length;
  displayQuote(currentQuoteIndex);
}, 4000);
```

### 3. **Modal with setTimeout**
```javascript
// Show modal after 5 seconds
setTimeout(() => {
  modal.style.display = 'flex';
}, 5000);
```

## 🎯 Key JavaScript Concepts Demonstrated

| Concept | Implementation |
|---------|----------------|
| **Arrays** | Storing 6 motivational quotes |
| **Loops** | Iterating through quotes array |
| **Functions** | Countdown, slider, modal logic |
| **ES6 Features** | Arrow functions, template literals, let/const |
| **DOM Manipulation** | Updating timer, quotes, and modal |
| **Timers** | `setInterval`, `setTimeout`, `clearInterval` |
| **Event Handling** | Button clicks, modal close |

## 📸 Screenshots

*(<img width="1334" height="886" alt="image" src="https://github.com/user-attachments/assets/2faddc98-737e-400d-b01f-a2560807e430" />
)*

1. **Main Interface** - Shows countdown timer and current quote
2. **Modal Popup** - Welcome message after 5 seconds
3. **Paused State** - Countdown paused with "Start" button
4. **Timer Complete** - "Time's up!" message when countdown reaches zero

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## ✨ Author

Built as a learning project for JavaScript fundamentals.

## 🎯 Learning Outcomes

By building this project, you'll master:
- Working with JavaScript timing functions
- DOM manipulation techniques
- Event handling and user interactions
- ES6+ JavaScript features
- Creating interactive web applications

---

**🎉 Happy Coding! Stay Motivated!**
