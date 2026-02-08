# 🏖️ VieraVille - Private Town Tycoon

A city-building tycoon game where you hire autonomous managers to build and develop a Florida-themed town. Watch as your managers propose construction plans, build roads and structures, and grow your town into a thriving metropolis!

---

## 🎮 How to Play

Build and manage a thriving Florida community. Hire **unlimited managers** who autonomously generate construction plans, build roads and structures, and grow your town. Balance your budget, maintain structures, and watch your population soar!

### Getting Started
1. **Hire Your First Manager** - Choose from managers with unique building preferences
2. **Review Construction Plans** - Managers propose 3-tier plans with cost estimates
3. **Approve or Enable AUTO Mode** - Let managers work autonomously
4. **Watch Your Town Grow** - Managers build roads and structures independently
5. **Manage Maintenance** - Repair damaged buildings and roads to keep happiness high
6. **Hire More Managers** - Scale up with unlimited hires for faster expansion

### Key Features
- 🔄 **Unlimited Manager Hiring** - Hire as many managers as you want
- 🤖 **AUTO Mode** - Toggle automatic plan approval per manager
- 🏗️ **Autonomous Building** - Managers execute construction independently
- 🔧 **Click-to-Repair** - Left-click damaged structures to instantly repair them
- 💰 **Economic Management** - Balance income, construction costs, and maintenance
- 📊 **Real-time Stats** - Monitor population, jobs, happiness, and revenue
- 💾 **Auto-save** - Never lose progress with automatic saving

---

## 🎯 Controls

### Camera Controls
- **Mouse Drag** - Pan/move the camera around the map
- **Mouse Wheel** - Zoom in/out (max zoom: 3x, min zoom: 0.75x)
- **WASD / Arrow Keys** - Pan the camera with keyboard
- **+/- Keys** - Zoom in/out with keyboard
- **Spacebar** - Reset camera to center view

### Game Controls
- **Left Click** - Select buildings/roads to view info or repair if damaged
- **Left Click (Damaged Tile)** - Auto-repair structure (yellow overlay = damaged)
- **ESC** - Open options menu
- **P** - Pause/unpause game

### UI Interactions
- **Manager Cards** - Click to view details, toggle AUTO mode button
- **Top HUD** - Displays budget, population, jobs, happiness, year/month
- **Left Panel** - Manager panel (can be collapsed)
- **Right Panel** - Dashboard with statistics (can be collapsed)
- **Notifications** - Bottom-left toast notifications for events

---

## 💡 Tips & Strategy

### Early Game Strategy
- **Start with 2-3 managers** to establish steady growth without overwhelming costs
- **Enable AUTO mode early** once you understand manager preferences (saves time)
- **Focus on residential buildings first** to build population quickly
- **Balance housing with commercial/industrial** for jobs and revenue
- **Don't overspend** - watch your budget and approve affordable plans

### Manager Management
- **Check preferences before hiring** - Managers with 40-60% in one type are specialists
- **AUTO mode works great** - Managers pick their specialty 80% of the time
- **Mix AUTO and manual** - Use AUTO for trusted managers, manual for expensive plans
- **Hire specialists** - High-percentage managers build faster in their category
- **More managers = faster growth** - But watch those monthly salaries!

### Budget Tips
- **Monthly revenue comes from buildings** - Commercial and industrial are best
- **Construction costs are immediate** - Money deducted as building progresses
- **Plan ahead** - Some manager plans cost $1M+, make sure you can afford it
- **Repair costs scale with value** - Buildings cost 1% of value, roads are $200
- **Watch the monthly expenses** - Salaries and maintenance add up quickly

### Maintenance & Repairs
- **Yellow overlay = damaged** - Look for the glowing yellow squares
- **Repair immediately** - Damage hurts happiness (-1% per 10 damaged tiles)
- **Click to repair** - Just left-click the yellow tile, instant fix
- **Up to 10 per month degrade** - Keep an eye on the disrepair counter
- **Roads are cheap, buildings vary** - Roads always $200, buildings 1% of value

### Building Type Strategy
- **Residential** 🏠 - Essential for population growth, low maintenance
- **Commercial** 🏢 - Best revenue generators, provides jobs
- **Industrial** 🏭 - High employment, good revenue, may lower happiness
- **Agricultural** 🌾 - Steady income, low operating costs
- **Amenity** 🎭 - Boosts happiness significantly, low revenue
- **Ranch** 🐴 - Specialty buildings, good for diversification

### Late Game Scaling
- **Hire 5-10 managers** once budget is stable
- **Enable AUTO on all** for explosive autonomous growth
- **Monitor disrepair count** - More buildings = more maintenance
- **Optimize for goals** - Push population or revenue depending on win conditions
- **Keep happiness above 70%** - Build amenities if it drops

### Common Mistakes to Avoid
- ❌ Hiring too many managers early (salary costs)
- ❌ Approving plans you can't afford (budget death spiral)
- ❌ Ignoring damaged buildings (happiness plummets)
- ❌ Building only one type (unbalanced economy)
- ❌ Forgetting to save manually (use ESC menu)

---

## 🏗️ Building Types

### Residential
Provides population and housing for workers
- Small Houses, Medium Houses, Large Houses
- Apartments, Condos, Luxury Estates

### Commercial
Generates revenue and provides jobs
- Shops, Restaurants, Offices
- Shopping Malls, Business Parks

### Industrial
High employment, moderate to high income
- Factories (small/large), Warehouses

### Amenity
Parks, entertainment, happiness boosters
- Various recreational facilities

### Agricultural
Farms and food production
- Steady income, low costs

### Ranch
Specialty agricultural buildings
- Unique revenue streams

*Each type has different costs, population capacity, job creation, and revenue generation*

---

## 📁 Project Structure

```
/
├── index.html                    # Entry point
├── App.js                        # Main React app
├── README.md                     # This file
├── COMPLETE_FEATURE_LIST.md      # Full feature documentation
├── IMPLEMENTATION_PLAN.md        # Technical roadmap
├── SOUND_SYSTEM.md               # Audio architecture docs
├── CONTROLS_REFERENCE.md         # Player guide
│
├── constants/                    # Game configuration
│   ├── gameConfig.js            # Grid, time, costs, win/lose
│   ├── buildingData.js          # 20 building definitions
│   ├── managerData.js           # 10 manager definitions
│   └── uiConstants.js           # Colors, sizes, styling
│
├── state/                        # State management
│   ├── GameState.js             # Central game state singleton
│   └── StateManager.js          # React context provider
│
├── managers/                     # Game systems
│   ├── TimeManager.js           # Month/season/year progression
│   ├── ManagerAI.js             # Finite state machine AI
│   ├── RevenueManager.js        # Economic calculations
│   ├── PopulationManager.js     # Population & happiness
│   ├── EventManager.js          # Random events
│   ├── SoundManager.js          # Procedural audio (Tone.js)
│   ├── SaveManager.js           # LocalStorage persistence
│   └── ...
│
├── services/                     # Business logic
│   ├── TiledLoader.js           # Map loading
│   ├── PlanGenerator.js         # AI plan generation
│   ├── BuildingPlacer.js        # Building placement
│   ├── RoadBuilder.js           # Pathfinding for roads
│   └── RelationshipService.js   # Manager compatibility
│
├── components/                   # React UI components
│   ├── scenes/                  # Main screens
│   │   ├── TitleScreen.js
│   │   ├── ManagerSelection.js
│   │   └── GameScene.js
│   ├── hud/                     # HUD elements
│   │   ├── TopHUD.js
│   │   ├── ManagerPanel.js
│   │   ├── DashboardPanel.js
│   │   └── NotificationToast.js
│   ├── modals/                  # Popup windows
│   │   ├── ManagerDetailModal.js
│   │   ├── EventModal.js
│   │   ├── VictoryModal.js
│   │   └── DefeatModal.js
│   └── canvas/                  # Rendering
│       ├── GameCanvas.js
│       └── EntityLayer.js
│
└── utils/                        # Helper functions
    └── GridUtils.js
```

---

## 🎯 Game Systems

### Manager AI
Each manager operates with a **Finite State Machine:**
1. **Idle** - Wait for cooldown, then generate plan
2. **Proposing** - Present plan to player for approval
3. **Approved** - Plan accepted, ready to build
4. **Building** - Construct roads and buildings tile-by-tile

Managers have **specialties** (+20-30% bonus) and **relationships** (likes/dislikes affecting happiness).

### Economic System
- **Monthly Revenue** calculated from all buildings
- **Seasonal Multipliers** (e.g., Beach +50% in Summer)
- **Manager Bonuses** apply to specialty buildings
- **Costs:** Roads ($200/tile), salaries ($3K/month), maintenance ($50/building)

### Happiness System
Multi-factor calculation with weighted components:
- Employment Rate (30%)
- Building Diversity (20%)
- Amenities (25%)
- Housing Quality (25%)
- Manager Relationships (15%)

### Sound System
Procedural audio with **Tone.js** - no audio files needed!
- 25+ unique sound effects
- Type-specific building chords
- Event-driven music cues
- Mute toggle (M key)
- Persistent preferences

---

## 📊 Building Types

### Residential (6 types)
Small/Medium/Large Houses, Apartments, Condos, Luxury Estates

### Commercial (5 types)
Shops, Restaurants, Offices, Shopping Malls, Business Parks

### Industrial (3 types)
Small/Large Factories, Warehouses

### Civic (3 types)
Schools, Hospitals, Police Stations

### Recreational (2 types)
Parks, Golf Courses

### Agricultural (1 type)
Farms

*Each with unique costs, population, jobs, revenue, and seasonal bonuses*

---

## 👔 Manager Roster

1. **Alex Chen** - Balanced Developer
2. **Maria Rodriguez** - Residential Specialist
3. **James Thompson** - Commercial Expert
4. **Sarah Williams** - Industrial Tycoon
5. **David Park** - Civic Leader
6. **Emily Zhang** - Recreational Guru
7. **Michael O'Brien** - Agricultural Expert
8. **Priya Patel** - Mixed-Use Visionary
9. **Carlos Mendez** - Ranch Manager
10. **Lisa Anderson** - Luxury Developer

*Each with unique bonuses, relationships, and personalities*

---

## 🏆 Win/Lose Conditions

### Victory 🎉
- Reach **16,000 population**
- Maintain **70%+ happiness**
- Unlock victory modal with stats
- Option to continue playing

### Defeat 💔
- Happiness drops to **0%**
- Budget falls below **-$100K** (bankruptcy)
- Game over, must restart

---

## 💾 Save System

- **Auto-save** every 30 seconds to LocalStorage
- **Manual save** with Ctrl+S / Cmd+S
- **Export/Import** saves as JSON
- **Continue** from title screen if save exists
- Full game state restoration

---

## 🔊 Sound Features

All sounds are **procedurally generated** using Tone.js:

- **UI Sounds** - Clicks, hovers, modal open/close
- **Money Sounds** - Coin gain/loss, big payouts
- **Building Sounds** - Chords vary by building type
- **Manager Sounds** - Hired melody, plan feedback
- **Event Sounds** - Positive/negative progressions
- **Ambient Sounds** - Month changes, seasons

Toggle with **M key** or click the 🔊 button!

---

## 🛠️ Technology Stack

- **Framework:** React 18 (createElement, no JSX)
- **Architecture:** ESM modules, importmap, buildless
- **Rendering:** HTML5 Canvas 2D
- **Audio:** Tone.js (Web Audio API)
- **Storage:** LocalStorage
- **Map Format:** Tiled JSON (optional)

**No build tools required!** Pure ESM modules running directly in browser.

---

## 📚 Documentation

### For Players
- **[QUICK_START_GUIDE.md](QUICK_START_GUIDE.md)** - 🌟 **Start here!** Your first 10 minutes
- **[CONTROLS_REFERENCE.md](CONTROLS_REFERENCE.md)** - Complete controls & tips reference

### For Developers
- **[COMPLETE_FEATURE_LIST.md](COMPLETE_FEATURE_LIST.md)** - Full feature documentation
- **[IMPLEMENTATION_PLAN.md](IMPLEMENTATION_PLAN.md)** - Technical roadmap & phase tracking
- **[DESIGN_DOCUMENT_v2.md](DESIGN_DOCUMENT_v2.md)** - Original design specifications

### For Audio/QA
- **[SOUND_SYSTEM.md](SOUND_SYSTEM.md)** - Audio architecture documentation
- **[SOUND_IMPLEMENTATION_SUMMARY.md](SOUND_IMPLEMENTATION_SUMMARY.md)** - Sound feature summary
- **[SOUND_TEST_CHECKLIST.md](SOUND_TEST_CHECKLIST.md)** - QA testing guide

---

## 🎨 Credits

**Inspiration**
- Viera, Florida - Master-planned community by the Duda family

**Created for**
- 3-Day Game Jam Project
- Rosebud AI Platform

---

## 📈 Project Stats

- **Files:** 45+
- **Lines of Code:** 8,000+
- **Components:** 20+
- **Managers:** 10 unique AIs
- **Buildings:** 20 types
- **Sound Effects:** 25+
- **Development Time:** 30+ hours
- **Completion:** 100%

---

## 🐛 Known Limitations

### By Design
- First click required to initialize audio (browser security)
- Population updates silent (covered by month changes)
- Building sounds throttled to 200ms (prevents spam)

### Optional Enhancements
- Entity walk animations (sprite sheets)
- Tile-by-tile construction animation
- Background music loops
- Event choice system

---

## 🚀 Getting Started (Development)

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari)
- Local web server (for CORS if needed)
- No build tools required!

### Running Locally
1. Clone or download the repository
2. Open `index.html` in browser
3. Or use a simple HTTP server:
   ```bash
   python -m http.server 8000
   # Navigate to http://localhost:8000
   ```

### File Structure
All code is organized by responsibility:
- **constants/** - Configuration (no logic)
- **state/** - Data management
- **managers/** - Game systems
- **services/** - Business logic
- **components/** - UI rendering
- **utils/** - Helper functions

---

## 📝 License

Created for educational and portfolio purposes.
Inspired by real-world master-planned communities.

---

## 🎉 Status

**✅ Version 1.0 GOLD - Production Ready**

All core systems implemented, tested, and documented.
Ready for release, playtesting, and iteration!

**Win condition:** Build to 16K population with 70% happiness
**Good luck, Developer!** 🏖️

---

**Made with ❤️ using React, Canvas, and Tone.js**
**No build tools • Pure ESM modules • Procedural audio**
