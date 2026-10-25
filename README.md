# 🌿 EcoLearn – Explore, Learn, Protect
### Interactive Environmental Awareness & Action Platform for Students

EcoLearn is a modern, responsive, educational web platform tailored for school and college students. It makes environmental science captivating through interactive learning modules, gamified quizzes, hands-on mini-games, real-world eco-challenges, practical projects, and a dynamic student progress dashboard.

---

## 🌟 Key Features & Architecture

1. **Home Page (`Home.jsx`)**:
   - Hero banner: *"Small Actions, Big Impact"*.
   - Live student impact metrics: Virtual trees planted, quiz questions answered, freshwater conserved, and CO₂ prevented.
   - Interactive Student Carbon Footprint Quick Estimator.
   - Curated topic highlights and daily eco-fact generator with shuffle.
   - Featured daily challenges with instant action logging.

2. **Interactive Learn (`Learn.jsx`)**:
   - 11 comprehensive modules: Climate Change, Global Warming, Air Pollution & AQI, Water Pollution, Deforestation, Biodiversity, Waste Management, Circular Economy, Renewable Energy, Oceans & Marine Conservation, and Sustainable Living.
   - Categorized by levels: Beginner, Intermediate, and Advanced.
   - Instant Search by concept or keyword.
   - Text-to-Speech audio reader using standard Web Speech API.
   - Deep-dive sections, key scientific data, India & global case studies (e.g. Sundarbans, Bhadla Solar Park, Indore waste segregation, Tamil Nadu rainwater harvesting, Chipko movement).
   - In-module Mini Knowledge Checks granting instant XP upon completion.

3. **Eco Quiz Zone (`QuizZone.jsx`)**:
   - Category selector: Climate, Oceans & Water, Clean Energy, Forests & Wildlife, Circularity.
   - Multiple difficulty levels: Easy, Medium, Hard.
   - Timed quiz engine with progress bar, instant feedback, and detailed scientific explanations.
   - Results summary, XP rewards, grade badges, and celebratory confetti.

4. **5 Educational Mini-Games (`EcoGames.jsx`)**:
   - **Waste Sorting Master**: Tap/drag items (compost, recyclables, hazardous e-waste) into color-coded bins with streak multipliers.
   - **Save the Forest**: Re-wild barren plots with indigenous trees (Neem, Peepal, Banyan, Mangrove) and extinguish wildfire sparks.
   - **Water Leak Rush**: 30-second reflex challenge to locate and seal dripping taps, leaky valves, and running hoses.
   - **Renewable Energy Match**: Match solar, wind, hydro, and biomass assets with their optimal geographical environments to power a 100% clean grid.
   - **Eco Memory Cards**: 16-card flip matching game featuring endangered wildlife and clean technology symbols, revealing ecological facts on each match.

5. **Student Eco-Challenges (`Challenges.jsx`)**:
   - Daily and weekly actionable missions (e.g. Zero Single-Use Plastic, 4-Minute Shower, Vampire Power Hunter, Native Tree Planting).
   - Personal reflection/proof logger and streak counter.

6. **Practical Student Projects (`Projects.jsx`)**:
   - 6 actionable guides: School Herb & Pollinator Garden, Campus Paper & E-Waste Drive, DIY Rainwater Harvesting Demonstration Model, Plastic-Free Campus Audit, Aerobic Composting Bucket, and Neighborhood Biodiversity BioBlitz.
   - Detailed materials list, step-by-step phases, and expected educational outcomes.
   - Interactive Project Submission Logger awarding up to 200 XP and honor badges.

7. **Student Progress Dashboard (`Dashboard.jsx`)**:
   - Customizable student avatar and name.
   - Level progression system (Level 1 Seedling -> Level 5 Forest Guardian).
   - 12 unlockable badges with date achieved.
   - Activity history log and progress reset.
   - **Official Eco-Certificate Generator (`CertificateModal.jsx`)**: Generates a printable/downloadable PDF certificate of environmental excellence.

8. **Eco Leaderboard (`Leaderboard.jsx`)**:
   - Dynamic podium for Top 3 students (Gold, Silver, Bronze).
   - Dynamic user rank placement reflecting your actual earned local XP.
   - Time filters: All Time, This Month, This Week.

9. **News & Planetary Facts (`NewsAndFacts.jsx`)**:
   - Curated articles on green hydrogen, African Great Green Wall, floating solar, and mycelium packaging.
   - Interactive planetary facts generator with one-click clipboard sharing.
   - Environmental awareness calendar (World Water Day, Earth Day, Environment Day, Ozone Day).

10. **About & Validated Contact (`AboutContact.jsx`)**:
    - Educational methodology: Learn -> Test -> Play -> Act.
    - FAQ accordion for students and teachers.
    - Fully validated contact form with friendly demo feedback.

11. **Student Login & Authentication Portal (`Login.jsx`)**:
    - Dual modes: **Sign In** and **Create Account**.
    - **1-Click Quick Demo Profiles**: Test as *Aarav Sharma* (Lvl 5 Guardian, 2,450 XP), *Priya Iyer* (Lvl 4 Steward, 2,180 XP), or a fresh *New Student* (0 XP).
    - Academic level and mascot avatar pickers with live password strength meter.
    - Interactive password recovery modal with simulated reset links.
    - Grants +100 XP Welcome Bonus upon registration.

12. **Design & Audio System**:
    - Nature-inspired color scheme: Forest green, emerald, ocean sky blue, and warm earth tones.
    - Dark mode and light mode with persistent toggle.
    - Zero-dependency Web Audio API synthesizer for pleasant chimes, water drops, and success fanfares.
    - Lightweight canvas-based confetti celebrations.
    - Global instant search (`Ctrl+K` / `⌘K`).

---

## 📁 Folder and File Structure

```
environment/
├── index.html                   # HTML5 entry with meta tags, SEO and fonts
├── package.json                 # Project dependencies and build scripts
├── vite.config.js               # Vite bundler configuration
├── tailwind.config.js           # Nature color palettes and custom animations
├── postcss.config.js            # PostCSS configuration
├── README.md                    # Project documentation & setup instructions
└── src/
    ├── main.jsx                 # React root mount
    ├── App.jsx                  # Main application routing and shell
    ├── index.css                # Base Tailwind styles & glassmorphism utilities
    ├── context/
    │   ├── EcoContext.jsx       # State management for XP, badges, streak, theme, auth
    │   └── SoundEffects.js      # Web Audio API procedural synthesizer
    ├── components/
    │   ├── Navbar.jsx           # Responsive sticky header with search & XP pill
    │   ├── Footer.jsx           # Eco-pledge banner, quick links, newsletter
    │   ├── SearchModal.jsx      # Global Ctrl+K multi-discipline search
    │   ├── CertificateModal.jsx # Printable student certificate of achievement
    │   └── Confetti.js          # Canvas confetti celebration generator
    ├── data/
    │   ├── modulesData.js       # 11 interactive educational curriculum modules
    │   ├── quizzesData.js       # Categorized MCQ quizzes with explanations
    │   ├── gamesData.js         # Educational data for 5 mini games
    │   ├── challengesData.js    # Daily and weekly student green challenges
    │   ├── projectsData.js      # 6 practical hands-on student projects
    │   ├── newsFactsData.js     # Science articles, eco-facts, and calendar
    │   └── leaderboardData.js   # Demonstrative student ranking data
    └── pages/
        ├── Home.jsx             # Hero, impact stats, carbon calculator, featured
        ├── Learn.jsx            # 11 modules, levels filter, audio reader, quiz
        ├── QuizZone.jsx         # Quiz catalog, timed player, results review
        ├── EcoGames.jsx         # 5 interactive playable educational games
        ├── Challenges.jsx       # Daily/weekly tasks with reflection logger
        ├── Projects.jsx         # Step-by-step action guides with report submit
        ├── Leaderboard.jsx      # Dynamic rankings, podium, and user rank
        ├── NewsAndFacts.jsx     # Articles, fact generator, events calendar
        ├── Dashboard.jsx        # Stats, levels, badges showcase, activity log
        ├── Login.jsx            # Student portal, Sign In/Up & 1-click demo profiles
        └── AboutContact.jsx     # Methodology, FAQ accordion, validated form
```

---

## 💻 Setup & Installation Instructions

### Prerequisites
- Node.js (v18.0.0 or higher recommended)
- npm or yarn or pnpm

### Installation Steps

1. **Open your terminal or command prompt** in the project directory:
   ```bash
   cd environment
   ```

2. **Install project dependencies**:
   ```bash
   npm install
   ```

3. **Start the local development server**:
   ```bash
   npm run dev
   ```

4. **Open your browser**:
   Navigate to `http://localhost:3000` (or the URL printed in your terminal).

---

## 🛠️ Step-by-Step Instructions to Run in Visual Studio Code

1. Open **Visual Studio Code**.
2. Click **File -> Open Folder...** and select the `environment` directory.
3. Open the built-in terminal in VS Code:
   - Shortcut: ``Ctrl + ` `` (Backtick) or go to **Terminal -> New Terminal**.
4. In the terminal, run:
   ```bash
   npm install
   ```
5. Once dependencies are installed, start Vite:
   ```bash
   npm run dev
   ```
6. Hold `Ctrl` and click the link `http://localhost:3000` in the terminal to view the website in your browser.

---

## 🚀 Building & Deploying the Website

### Creating a Production Build
To test the optimized production bundle:
```bash
npm run build
```
This generates an optimized static `dist/` directory ready for deployment. You can preview it locally using:
```bash
npm run preview
```

### Deployment Options (100% Free)
- **Vercel**:
  1. Push the code to a GitHub repository.
  2. Log in to [vercel.com](https://vercel.com) and import the repository.
  3. Framework Preset: **Vite**. Root directory: `./`.
  4. Click **Deploy**.
- **Netlify**:
  1. Drag and drop the `dist/` folder into [app.netlify.com/drop](https://app.netlify.com/drop) or connect your Git repo.
  2. Build command: `npm run build`. Publish directory: `dist`.
- **GitHub Pages**:
  - Configure `base: './'` in `vite.config.js` and use GitHub Actions to deploy the `dist/` folder.

---

## ➕ How to Extend & Add New Content

### 1. Adding a New Learning Module
Open [src/data/modulesData.js](file:///c:/Users/Hp/OneDrive/Desktop/environment/src/data/modulesData.js) and add an object to `modulesData`:
```javascript
{
  id: 'green-architecture',
  title: 'Sustainable Architecture & Green Buildings',
  level: 'Intermediate', // 'Beginner' | 'Intermediate' | 'Advanced'
  category: 'Urban Planning',
  readTime: '6 min read',
  summary: 'Explore passive solar design, rainwater harvesting roofs, and bamboo construction.',
  overview: '...',
  keyFacts: ['...'],
  realWorldCase: { title: '...', description: '...' },
  sections: [{ heading: '...', content: '...' }],
  knowledgeCheck: [
    {
      question: 'What is passive cooling?',
      options: ['...', '...'],
      answerIndex: 0,
      explanation: '...'
    }
  ]
}
```

### 2. Adding a New Quiz
Open [src/data/quizzesData.js](file:///c:/Users/Hp/OneDrive/Desktop/environment/src/data/quizzesData.js) and add a quiz object with category, difficulty, questions, options, correct index, and explanations.

### 3. Adding New Challenges or Student Projects
- Challenges: Edit [src/data/challengesData.js](file:///c:/Users/Hp/OneDrive/Desktop/environment/src/data/challengesData.js)
- Practical Projects: Edit [src/data/projectsData.js](file:///c:/Users/Hp/OneDrive/Desktop/environment/src/data/projectsData.js)

### 4. Adding Badges
Open [src/context/EcoContext.jsx](file:///c:/Users/Hp/OneDrive/Desktop/environment/src/context/EcoContext.jsx) and add your badge to `ALL_AVAILABLE_BADGES`.

---

## 📜 License & Attribution
Designed and built for environmental education initiatives, schools, universities, and eco-clubs worldwide. All educational content is formatted for student engagement and accessible learning.
