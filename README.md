# 🤖 Python With Selenium: Save & Load Cookies for Pinterest

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)](https://www.python.org/)
[![Selenium](https://img.shields.io/badge/Selenium-Automation-brightgreen?logo=selenium)](https://www.selenium.dev/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> Automate login and session management on Pinterest using Python & Selenium.

---

## 📂 Project Structure

| File                                | Purpose                                                   |
|-------------------------------------|------------------------------------------------------------|
| `credentials.py`                    | Stores Pinterest `EMAIL` and `PASSWORD`                   |
| `savecookies.py`                    | Manual login → save cookies                                |
| `loadcookies.py`                    | Auto login with credentials → save cookies                 |
| `editInCodeFile.json` | JSON file where cookies are stored (rename it in codefile                   |

---

### 🔑 Step 1: Set Your Credentials

Create a file named `credentials.py` and add your Pinterest credentials:

```python
EMAIL = "your_email@example.com"
PASSWORD = "your_password"
```

---

### 🧪 Step 2: Save Cookies

This project provides **two ways** to save cookies.

#### 💬 Manual Method

1. Run the script:

    ```bash
    python savecookies.py
    ```

2. A Firefox browser will open.
3. Log in manually to Pinterest within **60 seconds**.
4. Cookies will be saved to a file named:

    ```
    editInCodeFile.json
    ```

#### 🤖 Automatic Method

1. Make sure your `credentials.py` is configured.
2. Run the script:

    ```bash
    python loadcookies.py
    ```

3. It will:
   - Open Pinterest
   - Auto-fill your login info
   - Save the login session as cookies

> No manual login needed with this method.

---

### ♻️ Step 3: Reuse Cookies

Once cookies are saved in:

```
cookies_magicmushroomshop_account.json
```

You can use them in other Selenium scripts to maintain a logged-in session without logging in again.

Example usage:

```python
with open("cookies_magicmushroomshop_account.json", "r") as f:
    cookies = json.load(f)
for cookie in cookies:
    driver.add_cookie(cookie)
```

---

### 💻 Requirements

- Python 3.8+
- Selenium
- Firefox browser
- Geckodriver (must be in your system PATH)

#### 📦 Install Selenium

```bash
pip install selenium
```

---

### 🖼️ Preview

![Social Preview](c5d4474f-bcae-49e9-8a20-204fdc747480.png)

---

### 🌟 Use Cases

- Automate Pinterest login and scraping
- Bypass login prompts in dev/testing
- Create long-lived sessions for bots
- Accelerate Pinterest automation workflows

---

### 🙌 Credits

Built with ❤️ by [@thisisAhsanIqbal](https://github.com/thisisAhsanIqbal)

---

### 🪪 License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT)
