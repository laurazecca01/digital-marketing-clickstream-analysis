# E-commerce Clickstream Analysis 💻

In this project I analyzed user behavior and conversion patterns of an e-commerce platform that offers five products across different categories. The analysis focuses on understanding user sessions, review impacts, and purchase patterns through various methods including time decay attribution, Shapley values, and Markov chain analysis.

## Data Description
The dataset provided in the assignement included:
- User session IDs
- Timestamps
- Page categories
- Product information
- Review types (customer, video, celebrity)
- Purchase indicators
  
## Analytical methods

### 1. Attribution Modeling
- **Last-Click Attribution**: Assigns conversion credit to the final touchpoint before purchase
- **Time Decay Attribution**: Weights touchpoints based on temporal proximity to conversion and implements exponential decay function with one-hour half-life

### 2. Shapley Value Analysis
- **Game Theory Application**:
  - Treats marketing touchpoints as players in cooperative game
  - Calculates marginal contribution of each touchpoint
  - Considers all possible touchpoint combinations

### 3. Markov Chain Analysis
- **State Transition Matrix**:
  - Pages/actions as states
  - Transition probabilities between states
  - Absorption states: Purchase and Exit
- **Key Metrics**:
  - Conversion probability for each path
  - Expected number of steps to conversion
  - Path efficiency scoring

### 4. Linear Regression Models
- **Feature Engineering**:
  - Review type presence indicators
  - Session duration binning
  - Click sequence encoding

### 5. User Path Analysis
- **Sankey Diagram Visualization**:
  - Node: Page/action states
  - Edge weights: User flow volume
  - Time decay incorporation
- **Path Processing**:
  - Sequential path extraction
  - Temporal alignment
  - Flow volume calculation

### 6. Session Analysis
- **Time-based Segmentation**:
  - Custom time bins for day/hour analysis
  - Session duration calculation
  - Purchase probability by time segment
- **Click Pattern Analysis**:
  - Click sequence extraction
  - Page category transition matrices
  - Purchase intent indicators

## Technologies Used
- Pyhon
- Libraries: pandas, matplotlib/seaborn, plotly, scikit-learn, markovclick, statsmodels
  
## Key Findings
1. **Session Patterns**
   - Peak user activity occurs on Monday evenings
   - Optimal session duration for purchases: 30 minutes to 1 hour
   - Users make approximately 18 clicks prior to purchase

2. **Review Impact**
   - Customer reviews show highest conversion impact
   - Combined effect of celebrity and customer reviews yields 1.34x effectiveness
   - Time decay analysis reveals gradual buildup of review influence

3. **User Behavior**
   - Homepage and product categories receive highest traffic
   - Clear patterns in user navigation between reviews and product pages
   - Most users return to homepage regardless of starting point




