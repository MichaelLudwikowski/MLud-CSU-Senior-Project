# Stock Trading with AI Analyst

---

## Test Scenarios and Cases

Below is a list of test scenarios, test cases, and expected results based on the current requirements and project plan.

---

### 1. User Account Management

**Test Scenario 1.1: Create a new user account**  
- **Test Case:**  
  1. Open app  
  2. Select 'Create Account'  
  3. Enter details  
  4. Submit  
- **Expected Result:** Account is created, user can log in

**Test Scenario 1.2: Reset user account**  
- **Test Case:**  
  1. Log in  
  2. Go to settings  
  3. Select 'Reset Account'  
  4. Confirm  
- **Expected Result:** Account resets to default state

**Test Scenario 1.3: Access user profile/settings**  
- **Test Case:**  
  1. Log in  
  2. Open profile/settings menu  
- **Expected Result:** Profile/settings load within 2 seconds

---

### 2. Wallet and Fake Money System

**Test Scenario 2.1: Initial wallet balance**  
- **Test Case:**  
  1. Create new account  
  2. View wallet  
- **Expected Result:** Wallet shows $1000

**Test Scenario 2.2: Update wallet balance after trade**  
- **Test Case:**  
  1. Make a trade  
  2. View wallet  
- **Expected Result:** Balance updates correctly

**Test Scenario 2.3: Prohibit transaction with insufficient funds**  
- **Test Case:**  
  1. Attempt trade with low balance  
- **Expected Result:** Transaction is blocked

**Test Scenario 2.4: Low balance notification**  
- **Test Case:**  
  1. Spend until balance < $100  
  2. Check notifications  
- **Expected Result:** Notification is sent

---

### 3. Stock Trading Simulation

**Test Scenario 3.1: Make a trade**  
- **Test Case:**  
  1. Select stock  
  2. Enter amount  
  3. Confirm trade  
- **Expected Result:** Trade is processed, shown in history

**Test Scenario 3.2: View trade history**  
- **Test Case:**  
  1. Open trade history  
- **Expected Result:** All trades are listed accurately

**Test Scenario 3.3: Manage multiple investment accounts**  
- **Test Case:**  
  1. Create additional accounts  
  2. Switch between them  
- **Expected Result:** Each account has separate history and balance

---

### 4. AI Analyst Predictions

**Test Scenario 4.1: Get AI prediction for a stock**  
- **Test Case:**  
  1. Select stock  
  2. Request AI analysis  
- **Expected Result:** AI provides prediction and confidence rating

**Test Scenario 4.2: AI auto-invest feature**  
- **Test Case:**  
  1. Enable auto-invest  
  2. Let AI make trades  
- **Expected Result:** AI makes trades based on its analysis

**Test Scenario 4.3: AI rationale and report**  
- **Test Case:**  
  1. Request rationale/report from AI  
- **Expected Result:** AI explains its decisions

---

### 5. Notifications and Alerts

**Test Scenario 5.1: Stock alert notification**  
- **Test Case:**  
  1. Set alert for a stock  
  2. Wait for condition  
- **Expected Result:** Notification is sent when condition met

**Test Scenario 5.2: General system notifications**  
- **Test Case:**  
  1. Trigger system events (e.g., account reset, trade)  
- **Expected Result:** User receives appropriate notifications

---

### 6. Portfolio Tracking and Reporting

**Test Scenario 6.1: View portfolio performance**  
- **Test Case:**  
  1. Open portfolio page  
- **Expected Result:** Performance metrics are shown

**Test Scenario 6.2: Generate portfolio report**  
- **Test Case:**  
  1. Request report  
- **Expected Result:** Report matches user activity and trades

---

### 7. User Interface and Usability

**Test Scenario 7.1: Use main features**  
- **Test Case:**  
  1. Navigate through app  
  2. Use features  
- **Expected Result:** No crashes, features work as expected

**Test Scenario 7.2: UI responsiveness**  
- **Test Case:**  
  1. Interact with menus, buttons  
- **Expected Result:** UI responds within 2 seconds

---

### 8. User Testing

**Test Scenario 8.1: User trial for ease of use**  
- **Test Case:**  
  1. New user tries simulation  
- **Expected Result:** User can complete basic tasks without help

**Test Scenario 8.2: User feedback on learning**  
- **Test Case:**  
  1. User completes simulation  
  2. Gives feedback  
- **Expected Result:** User reports increased understanding of trading

---

### 9. Overall Program Functionality

**Test Scenario 9.1: Run full program**  
- **Test Case:**  
  1. Use all main features in sequence  
- **Expected Result:** All features work together without errors

**Test Scenario 9.2: Error handling**  
- **Test Case:**  
  1. Cause errors (invalid input, network issues)  
- **Expected Result:** Program handles errors gracefully
