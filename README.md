# 🚗 Driving School Trainer 📝

An open-source, client-side **Driving School Trainer** web app for quizzing users on Polish driving exam questions with multilingual support and media integration.

## 🌟 Features

* Modes: 🆓 Learning (review answers immediately) and ⏱️ Exam (timed, no backtracking).
* Question Sets: Automatically generated sets combining ✅ Yes/No and 🅰️🅱️🅾️ Multiple Choice questions in the correct ratio.
* **🌐 Multilingual**: English 🇬🇧, Polish 🇵🇱, German 🇩🇪, Ukrainian 🇺🇦, French 🇫🇷, Russian 🇷🇺, Arabic 🇸🇦, Farsi 🇮🇷, Georgian 🇬🇪, Tajik 🇹🇯 (fallback to English).
* **🖼️ Media Support**: Images and 🎥 MP4 videos embedded, with custom play overlay and disabled seeking.
* **📊 Progress Tracking**: Visual progress bar, question counters, and final score calculation.
* **🔍 Review**: At the end of each set, users can review incorrect answers with correct choices highlighted.

## 🚀 Getting Started

1. **🔗 Clone the repo**

   ```bash
   git clone https://github.com/yourusername/driving-school-trainer.git
   cd driving-school-trainer
   ```

2. **📥 Download Media Assets**

   Place all required images and MP4 videos into the `/media` folder. You can download the complete media package from Google Drive:

   ```
   https://drive.google.com/file/d/13HRerzbuwIoDhIZXHZfzRhXahKCDjvMm/view?usp=drive_link
   ```

   After downloading, extract the files into the `media` directory so that filenames match those referenced in `questions.json`.

3. **⚙️ Serve Locally**

   Use Python's built-in HTTP server:

   ```bash
   python -m http.server 8000
   ```

   Navigate to `http://localhost:8000` in your browser.

4. **🛠️ Customize Questions**

   * Place your `questions.json` in the project root.
   * Ensure each question object has:

     ```json
     {
       "id": 99,
       "question": { "en": "...", "pl": "...", ... },
       "answers": { "A": { "en": "Yes", "pl": "Tak" }, "B": { ... } },
       "correct": "A",
       "type": "yes_no", // or "multiple_choice"
       "media": "AK_D05_06_org.mp4",
       "categories": ["A","B1",...]
     }
     ```

## 🤝 Contributing

We ❤️ contributions! Feel free to:

* 🍴 Fork this repository
* 🌿 Create a branch for your feature or bugfix
* 🔀 Submit a pull request

Please follow the standard GitHub workflow and ensure your changes maintain code style and pass manual testing.

## 📄 License

This project is licensed under the **MIT License**. Feel free to use it freely in your own applications.

---

*Built with ❤️ and open-source principles.*
