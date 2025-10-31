# Data Sources

## FIFA Dataset (2017-2023)

### Overview
The FIFA dataset contains official player statistics from FIFA video games spanning 2017 to 2023.

### Files
- `FIFA17_official_data.csv` - FIFA 2017 player data
- `FIFA18_official_data.csv` - FIFA 2018 player data (includes Release Clause)
- `FIFA19_official_data.csv` - FIFA 2019 player data (includes Release Clause)
- `FIFA20_official_data.csv` - FIFA 2020 player data (includes Defensive Awareness)
- `FIFA21_official_data.csv` - FIFA 2021 player data (includes Defensive Awareness)
- `FIFA22_official_data.csv` - FIFA 2022 player data
- `FIFA23_official_data.csv` - FIFA 2023 player data

### Dataset Statistics
- **Total Records**: ~102,000+ player entries (combined)
- **Features**: 60+ attributes per player
- **Years Covered**: 2017-2023

### Key Features
- **Demographics**: Name, Age, Nationality, Club, Position
- **Ratings**: Overall, Potential, Special
- **Economics**: Value, Wage, Release Clause
- **Physical**: Height, Weight, Body Type
- **Skills**: Pace, Shooting, Passing, Dribbling, Defending, Physical
- **Mental**: Aggression, Reactions, Composure, Vision
- **Technical**: Ball Control, Dribbling, Finishing, etc.

### Data Quality Issues Addressed
1. **Body Type Encoding**: Some entries had `PLAYER_BODY_TYPE_XXX` format
2. **Missing Values**: Club data had MCAR (Missing Completely at Random) patterns
3. **Mixed Data Types**: Position column had HTML span classes
4. **Currency Formats**: Values and wages needed conversion from string (€XXM/K) to numeric

### Cleaned Datasets
Processed datasets are available in `fifa_dataset_cleaned/` with:
- Resolved body type encodings
- Normalized height/weight values
- Converted wages and values to numeric
- Cleaned position data
- Engineered features (age categories, potential gap, composites)

### Usage Notes
- Free agent players have `null` values in Club column (intentional)
- Players on loan have `Loaned From` populated
- Some players have Easter egg body types (e.g., "Messi", "C. Ronaldo")

### Sources
Official FIFA game data exported from the video game series.

### Ethical Considerations
- Data used for educational and analytical purposes only
- Player names and likenesses are property of respective individuals/organizations
- No commercial use intended
