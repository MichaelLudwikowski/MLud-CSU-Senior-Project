Senior Project Requirements: Stock Trading with AI Assistant
===================================================

*   Account / User (1-5)
*      Requirement Type: Functional
       Priority Level: High
       Fit Criteria: Users can access their profile and settings from a menu with a response time of 2 seconds
       Rationale: Enables users to have control over their configurations, data, and settings.
 
       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The system accuratly stores and retreives the users fake money balance and history with 100% accuracy
       Rationale: Allows the users to track their historic data and view mistakes they have made previously
  
       Requirement Type: Functional
       Priority Level: Medium
       Fit Criteria: Users can manually reset their account and start over with confirmation steps to how it was when they first started
       Rationale: Provides a fresh start for users who feel stuck or confused  

       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: Users can create and manage multiple investment accounts
       Rationale: Allows the users to test different simulations and strategies
 
       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The system provides users with notifications, updated, and alerts whenever a stock meets a specified alert ammount. 
       Rationale: Keeps the user informed of what might be going on at a certain time i.e. AI updates

*   Fake Money & Wallet System (6-10)
*      Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The system initializes new accounts with a default balance of $1000
       Rationale: Creates a standard starting point for all users

       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The current balance is displayed in the wallet interface 
       Rationale: Ensures that the user is keeping track of their balance
 
       Requirement Type: Functional
       Priority Level: Critical
       Fit Criteria: Transactions are prohibited if the user has insufficient available funds
       Rationale: Prevents unrealistic purchases in the environment
 
       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: Users receive a notification when their balance goes below $100 (including their portfolio)
       Rationale: Helps the users track their funds

       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The system generates transaction logs of all trades they make for the user to see
       Rationale: Provides a transparency for the user to view

*   Stock Market Simulation (11 - 19)
*      Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The system uses real historic data over the past couple of months to base its simulated stocks
       Rationale: Provides the user with a realistic idea of how stocks could work

       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: Users can input stock symbols or company names and receive their market data
       Rationale: Supports access to specific stocks

       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: Users can view stocks charts along with their recent history and performance ovre the past 3 months.
       Rationale: Allows the users to view how the company has been doing
  
       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: Users can set custom alerts for price changes for certain stocks
       Rationale: Promotes proactive trading decisions

       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: Allows the user to "buy" and "sell" shares in a stock using fake money that are put into their portfolio
       Rationale: The whole idea behind the project, buying and selling stocks and trying to sell high

       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: Program shall provide confirmation logs when the user completes a transaction 
       Rationale: Confirms that a purchase goes through

       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: Program shows the users portfolio information with all stock they own
       Rationale: Allows the users to see where their money is currently in the stock market

       Requirement Type: Functional
       Priority Level: Medium
       Fit Criteria: Users can simulate a limited margin trading option
       Rationale: introduces an advanced trading concept for new users

       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The system provides a portfolio overview, including overall gains and losses over their entire time trading
       Rationale: Helpps users evaluate their performance over time

*   AI Analyst Potential Functions (20-26)
*      Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The AI model generates predictions based on months of historical data
       Rationale: Enhances the decision making for unsure or new users
 
       Requirement Type: Functional
       Priority Level: Medium
       Fit Criteria: Shows the AI's top stock perdiction with the highset and lowest percentage change for the day every day
       Rationale: Gives users a base from where to start looking

       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: Users can toggle the AI's auto investing feature on or off
       Rationale: Allows basic control over the AI

       Requirement Type: Functional
       Priority Level: Medium
       Fit Criteria: The AI model provides risk evaluation metric for each stock recomendation
       Rationale: Helps users gauge potential investment risks

       Requirement Type: Functional
       Priority Level: Medium
       Fit Criteria: AI-generated predictions are accompanied by confidence intervals with a rationale
       Rationale: Further ensures the transparany and reasoningg behind recomendations

       Requirement Type: Functional
       Priority Level: Medium
       Fit Criteria: Users can view the AI's trading history over all time it was on for analysis
       Rationale: Helps the user track the AU investment performance

* AI Training and Simulation (27-30)
  
       Requirement Type: Functional
       Priority Level: Critical
       Fit Criteria: The system shall simulate real world training events over the past 3 months to train the AI learning model 
       Rationale: basing the AI off of real data can make it more accurate than simulated data
 
       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The system shall include tools to measure the AI's prediction accuracy to see how off it might be. I am hoping to start in the positive range, then go from there to around as low as 10% error if possible.
       Rationale: Make sure the AI is staying on track with it's predictions
 
       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The system shall display the prediction performance over all its lifetime and over different simulations
       Rationale: Allows perspective for how the AI is doing over a long period of time
 
       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The system shall include adjustable settings for the AI such as tolerance, frequence, and balance
       Rationale: Promotes further control over the AI for maximum performance and learning

* Educational Features (31-35)
  
       Requirement Type: Functional
       Priority Level: Medium
       Fit Criteria: The system shall offer first time traders and users with a basic explanation of the stock market going over what stocks are, who owns them, and how you make money from them. 
       Rationale: Explains to users who may have never done anything with the stock market with a quick explanation of the basics
 
       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The system shall show users why certain trades may be favorable or more risky than others 
       Rationale: Explains the reasoning and helps the users to start thinking on their own
 
       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The system shall offer easy, itermediate, and advanced training simulations that vary the help provided
       Rationale: Allows the user to test their skills in harder challenges
 
       Requirement Type: Functional
       Priority Level: Medium
       Fit Criteria: The system shall have an optional quiz-style assesments for the user to practice their knoledge with stock trading
       Rationale: Allows the user to review what they have learned
 
       Requirement Type: Functional
       Priority Level: Medium
       Fit Criteria: The system shall provide future learning oportunities and resources such as the history of stocks, how different factors affect them, and what to look out for if you want to become better
       Rationale: Allows for adamant users to learn more about stock trading

 * Interface and Display (36-39)
   
       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The system shall include a home page or dashboard displaying the users balance, portfolio, and AI features
       Rationale: Gives the user a single page with all of their information
 
       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The system shall provide helpful visual indicators such as arrows and colors for different stock trends
       Rationale: Makes it easier for the user to distinguish how a stock might be trending
 
       Requirement Type: Functional
       Priority Level: Critical
       Fit Criteria: The system shall provide users with information about a current stock and it's worth
       Rationale: Makes sure that the users have something to base their stock trading off of
 
       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The system shall have helpful tips with current stocks depending on what difficulty is set. The easier the difficulty the more tips provided
       Rationale: Gives new users on a lower difficulty a better idea of how they can perform well

* Testing and Debugging (40-44)
 
       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The system shall allow admin developers to run tests on all trading options ie buying more than what the stock is worth, trying to sell and buy more than what they have, and other fuzzer tests.
       Rationale: General testing for different things that the user may do
  
       Requirement Type: Functional
       Priority Level: Critical
       Fit Criteria: The system shall include logging of all trading activity for both users and AI over all time.
       Rationale: Crucial to allowing the users and admin to view how not just the user is performing, but making sure that the program is as well
  
       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The system shall include a "Debug mode" that pulls up the recent logs and data within the last 30 days
       Rationale: Gives raw data about the logs with more specifics that may be unnessary in the feedback

       Requirement Type: Functional
       Priority Level: High
       Fit Criteria: The system shall warn users if the AI is having issues or crashes with a timout time of around 5 seconds
       Rationale: Makes sure that the AI is staying active and not in need of debugging
