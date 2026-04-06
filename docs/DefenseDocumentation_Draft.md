# Stock Trading AI Analyst - Defense Documentation (Draft)

Student: Michael Ludwikowski  
Advisor: Dr. Hayes  
Program: B.S. Computer Science  
Date: April 2026  

## Chapter 1: Statement of Purpose (with Problem Statement)

### Purpose
The purpose of this project is to create an educational stock trading platform that helps beginner traders learn stock market concepts, practice decision-making, and understand portfolio risk without using real money. The platform combines fake-money trading, market data, charts, and AI-generated analysis to create a guided learning environment.

### Problem Statement
Many new traders enter the stock market with little practical experience and lose money because they do not understand market behavior, risk management, or trading discipline. Existing tools are often either too advanced for beginners or too simple to provide realistic practice. This project addresses that gap by offering a safe system where users can learn by doing, analyze results, and improve before ever risking real capital.

### Project Objectives
1. Provide a realistic but safe stock trading experience using simulated funds.
2. Support learning through dashboards, charts, portfolio feedback, and guided pages.
3. Integrate AI-based recommendations to explain possible buy, sell, or hold decisions.
4. Store user activity so balances, trades, and portfolio changes can be reviewed.

## Chapter 2: Research and Background

### Domain Background
Stock trading education is difficult because users must learn both technical platform skills and market fundamentals at the same time. Core beginner challenges include:
- understanding volatility and trend behavior
- position sizing and risk control
- interpreting chart movement and recent price history
- avoiding emotional or impulsive decisions

### Technical Background
To support those learning goals, this project combines:
- market data retrieval with caching and fallback behavior
- simulated trade execution with transaction logging
- portfolio value and gain/loss calculations
- AI-assisted prediction output with confidence and risk messaging
- web interface workflows for dashboard, stock browsing, practice mode, and simulation mode

### Key Constraints Discovered
1. Free market-data APIs may have strict request limits and slower refresh times.
2. Some intraday or premium endpoints require paid tiers.
3. Cached data can quickly become stale if refresh logic is not handled carefully.
4. AI output quality depends on historical data quality and prompt design.

## Chapter 3: Project Language(s), Software, and Hardware

### Programming Languages
- Python: Primary implementation language for backend logic, AI integration, data handling, database access, and web routes.
- HTML/CSS/JavaScript: Frontend templates and user interaction.

### Frameworks and Libraries
- Flask: Web framework for routes, templates, and session-based UI flow.
- SQLite: Local database storage for users, accounts, holdings, and transactions.
- Pandas / NumPy: Data manipulation and numeric processing.
- Bokeh: Interactive charting support.
- Ollama (Llama model): AI-assisted stock analysis and recommendation generation.
- Requests: HTTP communication for market API calls.
- Pytest: Test execution and validation.

### Development and Runtime Environment
- IDE: Visual Studio Code
- OS: Linux (primary development environment)
- Python Environment: Virtual environment (.venv)
- Source Control: Git/GitHub

### Hardware
- Primary development hardware: personal laptop/desktop class system
- No specialized GPU or cluster hardware required for the main version of the project

## Chapter 4: Project Requirements

### Core Requirements Implemented
1. Account and user management
   - user registration and login
   - logout and password reset flow in the web interface
   - account reset back to the default starting balance

2. Wallet and transaction controls
   - initialize new accounts with $1000 in fake money
   - prevent purchases when funds are not available
   - store holdings, balances, and transaction history in SQLite

3. Stock data and analysis
   - search stocks by symbol
   - retrieve quote and historical data with caching
   - display historical charts and stock detail information

4. Trading operations
   - buy and sell stock through the application
   - update holdings and portfolio value after trades
   - calculate total value and gain/loss information

5. AI analyst support
   - generate buy, sell, or hold recommendations
   - include confidence, risk level, and a short rationale

6. Learning and practice features
   - learning page for beginner information
   - historical simulation mode
   - practice mode with different difficulty settings

7. Interface and display
   - dashboard with balance, holdings, and recent activity
   - portfolio page and stock detail pages
   - interactive charts using Bokeh

8. Testing and reliability
   - test plan and written test cases
   - Python test scripts for API and AI integration work
   - transaction and balance validation in code

### Partially Implemented or Future Requirements
- Multiple account support exists in the data model, but the main workflow currently uses one main account.
- AI auto-investing and full AI training/performance tracking are only partially tested.
- Some advanced educational features such as quizzes and broader alert tools are still future work.

### Priority Notes
- Critical priorities include accurate wallet enforcement, core trading operations, and reliable stock information presentation.
- High priorities include dashboard clarity, portfolio analytics, AI-assisted guidance, and database-backed persistence.
- Medium priorities include expanded educational activities and advanced AI or trading options.

---

## Chapter 5: Project Implementation Description and Explanation

The final project was built mainly in Python. The main controller is in src/app.py, where the core parts of the system are connected together. These parts include the trading engine, market data provider, AI prediction engine, simulation mode, practice mode, and the database layer. This made the project easier to organize and test because each major feature is separated into its own module.

The project supports both a command-line version and a Flask web version. The web version is the main interface for the final project because it is easier to demonstrate and gives a clearer view of balances, holdings, charts, and stock details. In the web app, users can register, log in, reset their account, browse stocks, view their portfolio, and make trades. There are also pages for practice mode, simulation mode, and learning content.

Market data is handled through the market_data.py module. The program can request stock quotes and historical data, cache the data, and use fallback behavior if the API is limited or unavailable. This was important because free APIs do not always respond quickly and may have usage limits. The charting portion of the project uses Bokeh so that users can view interactive stock charts instead of only seeing raw numbers.

The AI portion of the project is handled through predictor.py. The system sends recent historical data to a local Ollama model and asks for a recommendation such as BUY, SELL, or HOLD. The result also includes a confidence value, risk level, and short explanation. If the model is not available, the system still works by using a fallback prediction method based on recent price trend data. This made the project more dependable during development and testing.

Another major part of the project is the practice and simulation support. Simulation mode lets the user move through historical market data over time. Practice mode creates a guided environment with synthetic companies and events so the user can practice without depending only on live data. These features support the educational purpose of the project and make it more than a basic buy/sell demo.

Source code repository: https://github.com/MichaelLudwikowski/MLud-CSU-Senior-Project

### Figures Used in This Documentation

Fig 1. Login page (web authentication entry point)

![Fig 1. Login page](../Project%20Explanation%20Pictures/Login%20Page.png)

Fig 2. Dashboard view after login (initial account overview)

![Fig 2. Dashboard view after login](../Project%20Explanation%20Pictures/Dashboard.png)

Fig 3. Stock search page (symbol search and popular stock list)

![Fig 3. Stock search page](../Project%20Explanation%20Pictures/Stock%20Search.png)

Fig 4. Stock detail page for AAPL (quick trade, AI recommendation, and interactive chart)

![Fig 4. AAPL stock detail page](../Project%20Explanation%20Pictures/AAPL%20Page.png)

Fig 5. Dashboard after placing a trade (cash, portfolio value, and transaction log update)

![Fig 5. Dashboard after AAPL trade](../Project%20Explanation%20Pictures/Dashboard%20after%20AAPL.png)

Fig 6. Practice mode setup page (difficulty and session length options)

![Fig 6. Practice mode setup](../Project%20Explanation%20Pictures/Practice%20mode%20page.png)

Fig 7. Practice mode active session (news events, progress, holdings, and gain/loss)

![Fig 7. Practice mode active session](../Project%20Explanation%20Pictures/Practice%20after%20some%20time.png)

Fig 8. Practice stock detail page (generated company, AI recommendation, and chart)

![Fig 8. Practice stock detail page](../Project%20Explanation%20Pictures/Fake%20Stock%20Practice.png)

---

## Chapter 6: Known Limitations and Risk Mitigation

One limitation of the project is that free market-data APIs have request limits. Because of that, the system uses caching and fallback behavior so that it can still show data even when the API cannot be called again right away. This reduces failures during demos and normal use.

Another limitation is that the AI features depend on a local Ollama setup. If Ollama is not running or the model is not installed, the full AI response will not be available. To reduce this problem, the project includes a fallback prediction method based on price trend analysis so that the application can still give a recommendation instead of failing completely.

Some planned features are not fully finished in the current version. Multiple account support exists in the data model but is not fully exposed in the user workflow. Margin trading logic also exists in code but is currently disabled. AI auto-investing and full AI training are only partially implemented. In this defense, those features should be presented as future improvements rather than as completed work.

The project is meant for education, not for real investing. Even when real market data is available, the system should not be treated as financial advice. This keeps the project focused on learning and practice instead of real-money trading.


---

## Chapter 7: Test Results Summary

Testing for this project was documented through a formal test plan, CSV-based test case files, and Python test scripts in the repository. The current test materials focus on account creation, trading rules, API integration, AI integration, and data handling. These tests were useful for checking whether the main features worked as expected and whether the program handled common failures.

The project repository includes test files such as test_alpha_vantage.py, test_ai_with_real_data.py, test_week2_api_integration.py, tests/test_ollama_integration.py, and tests/test_quick.py. There is also a larger written test plan and multiple test case spreadsheets and CSV files. Together, these show that testing was part of the project and not only something added at the very end.

Based on the current project state, the strongest tested areas are the core workflows: creating a user, storing account data, preventing invalid trades, retrieving stock data, and generating AI-based analysis. These results support the main goal of the project, which is to provide a safe educational trading platform with portfolio tracking and AI assistance.

For the final defense package, this section can still be improved by adding pass/fail snapshots, screenshots from successful test runs, and a short table that maps major requirements to the test files or test cases that support them.


---

## Chapter 8: Future Enhancements

Future work for this project includes finishing multi-account support, improving AI performance tracking, and expanding the educational side of the platform. More detailed alerts, better reporting, and additional learning activities would make the system more useful for beginner traders.

Another improvement would be better handling of real market data, especially around rate limits and refresh timing. The system could also be extended with stronger account security, more advanced portfolio analytics, and better administrative debugging tools.

Overall, the current version already demonstrates the main idea of the project, and future work would build on that foundation rather than restarting from scratch.

---

### Point 9: Future Enhancements
- multi-account workflow completion
- improved AI performance tracking and reporting
- expanded educational tools (alerts, quizzes, learning modules)
- security and analytics improvements

---

### Point 10: Defense Presentation Slides
- 10-12 slides total
- one main idea per slide
- use app visuals alongside short bullet text

Suggested slide order:
1. Title slide
2. Problem statement
3. Project goals
4. System architecture overview
5. Core features demo (dashboard/trading/AI)
6. Practice and simulation modes
7. Test plan and test results summary
8. Challenges overcome
9. Future enhancements
10. Conclusion and Q&A
