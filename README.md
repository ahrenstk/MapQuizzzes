# MapQuizzzes

**MapQuizzzes** is a flexible, web-based framework for creating interactive, GPS-supported outdoor puzzle tours for smartphones. It runs entirely in the user's browser, can be installed as a Progressive Web App (PWA), and does not require users to register or log in.

**German version:** **[https://github.com/ahrenstk/MapQuizzzes-de](https://github.com/ahrenstk/MapQuizzzes-de)**

---

## 🚀 Live Demo

You can check out the live demo **[Bourtange Quiz](https://ahrens.tk/MapQuizzzes-en)**. Imagine visiting the **[Bourtange Fortress](https://www.bourtange.co.uk)** and playing it right there on-site. You can also take a look at the **[Münster Quiz](https://ahrens.tk/muensterquiz-en)** and answer the quiz questions on-site if you ever find yourself in beautiful Münster.

---

## 🛠️ Who is MapQuizzzes the Perfect Solution For?

**MapQuizzzes** bridges the gap between the spirit of discovery and digital interaction. It is the ideal tool for anyone who wants to get people moving, inspire them in a playful way, and make knowledge tangible right on-site.

### 🌟 Perfectly Suited For:

* **Tourism & City Marketing Experts:** Turn classic guided city tours into gripping, interactive discovery tours and playfully captivate visitors with your region.

* **Experiential Educators & Schools:** Design modern, GPS-supported scavenger hunts and interactive learning paths out in the fresh air.

* **Event Agencies & Teambuilding Providers:** Create tailor-made outdoor rallies for corporate events, club outings, or private celebrations.

* **Creative Minds & Adventurers:** Easily create your own personal puzzle tour for friends and family.

---

### 💡 Your Path to Your Own Outdoor Quiz

The best part first: **MapQuizzzes is completely free!** Your path to your own MapQuizzz is incredibly simple:

1. **Lightning-Fast Setup:** Simply extract the software into a directory on your web server – and the technical foundation is already set up.

2. **Creative Design:** The most exciting part is up to you – bringing your tour to life! You define the locations, the puzzle questions, and the rewards.

3. **Instant Start:** To let you see what is possible right away, MapQuizzzes comes with a **fully-fledged demo tour**. This directly demonstrates all four flexible tour modes in action and serves as a perfect, easy-to-understand template for your own masterpiece.

---

## ✨ Features

- **Pure Browser Application:** The entire logic runs in the browser. No server-side data storage takes place.

- **PWA-Ready:** Can be added to the home screen of Android and iOS devices just like a native app.

- **No Registration:** Users can get started immediately without needing to create an account.

- **Interactive Maps:** MapQuizzzes uses Leaflet to display map material from OpenStreetMap and Esri.

- **GPS Navigation:** Shows the user's current location and offers a navigation function to the puzzle locations via Google Maps.

- **Flexible Tour Modes:**

    - **Step-by-Step:** Unlocks the next puzzle only after the previous one has been solved.

    - **Full Map:** All puzzles are visible from the start, including a GPX track.

    - **As the Crow Flies:** "Similar to Step-by-Step" but pointing directly with a straight line, without a GPX track.

    - **Freestyle:** Similar to "Full Map" but without a GPX track.

- **Versatile Puzzles:**

    - Multiple-choice questions or open-ended questions (each with a 3-second answer response time).

    - Hints as well as questions can be used optionally.

    - An image is used for each location.

    - Optionally, additional modals can be opened for each location, and links to external websites can be used.

- **Customizable & Extensible:** All tours, puzzles, and texts are configured using simple `JSON` files.

- **Multi-language Support:** The design is multilingual from the ground up and can easily be extended to support additional languages.

- **Open Source:** Released under the MIT License.

---

## 🛠️ Technical Structure

1. `index.php`: Loads the main configuration (`MapQuizzzes.json`), detects the language, and provides the basic HTML structure as well as the configuration data for the JavaScript app. It also serves as an API endpoint to load the data of a selected tour (`quizdata.json`).

2. `MapQuizzzes.js`: The core of the application.

3. Configuration Files (`.json`):

    - `MapQuizzzes.json`: Global configuration (name, available tours, UI translations).

    - `quizdata.json`: Contains all puzzle points for a specific tour (coordinates, questions, answers, images).

---

## 🚀 Creating Your Own Quiz Tour

MapQuizzzes is **not** a modular click-and-build system for creating interactive quizzes. However, with a little practice, it is not difficult to create your own puzzle tours:

1. **Delete or Rename Subfolders:**

   - In the demo: Fortress (Step-by-Step), Fortress (Full Map), Fortress (As the Crow Flies), Fortress (Freestyle).

2. **Create or Rename New Subfolders for Each Tour:**

   - e.g., `My First Tour`, `My Second Tour`.

3. **Adjust MapQuizzzes.json:**

    - Enter your own quiz name, homepage info, and register the tours, e.g., `My First Tour`, `My Second Tour`.

4. **Copy Necessary Files Into the Tour Folder:**

   - Images in two resolutions; feel free to use `upload.php` from the demo tour folders to automatically generate the correct image sizes.

   - Optionally assemble additional info (modalheader, modalfooter, modalextra).

5. **Adjust `quizdata.json` for Each Tour:**

    - Copy the `quizdata.json` file from the demo and customize it for your own tour.

    - Each JSON object contains the data required for each individual location.

6. **Adjust Instructions, Imprint (Legal Notice), and Privacy Policy:**

   - Customize the files or create them from scratch for your purposes. You can also link the imprint and privacy policy to external pages.

Done! Your MapQuizzzes instance with your tours is ready and good to go.

---

## 📄 License

This project is licensed under the **MIT License**. You can find the licensing details in the `LICENSE.txt` file.

---
