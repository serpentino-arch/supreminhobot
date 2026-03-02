# Supremebot Setup Guide

A step-by-step guide to install and run Supremebot on your computer.

## Requirements

- Windows 10/11, macOS, or Linux
- Internet connection

## Step 1: Install Python

### Windows
1. Go to https://www.python.org/downloads/
2. Download Python 3.11 or newer
3. Run the installer
4. **IMPORTANT**: Check "Add Python to PATH" at the bottom
5. Click "Install Now"

### macOS
1. Open Terminal
2. Run: `brew install python` (or download from python.org)

### Verify Installation
Open Terminal/Command Prompt and run:
```
python --version
```
Should show `Python 3.11.x` or higher.

## Step 2: Get the Code

### Option A: Download ZIP
1. Get the ZIP file from the owner
2. Extract to a folder (e.g., `Desktop/supremebot`)

### Option B: Clone from GitHub (if you have access)
```
git clone https://github.com/serpentino-arch/supreminhobot.git
cd supreminhobot
```

## Step 3: Install Dependencies

1. Open Terminal/Command Prompt
2. Navigate to the bot folder:
   ```
   cd Desktop/supreminhobot
   ```
3. Install required packages:
   ```
   pip install nicegui playwright requests beautifulsoup4 cloudscraper
   ```
4. Install browser for automation:
   ```
   python -m playwright install chromium
   ```

## Step 4: Run the Bot

1. In the same terminal, run:
   ```
   python main.py
   ```
2. Open your browser to: **http://localhost:8080**

## How to Use

### Before Drop Day (Preparation)

1. **Select drop date** from the dropdown
2. **Browse categories** (T-Shirts, Accessories, etc.)
3. **For items you want:**
   - Select color
   - Select size
   - Click "Add to Basket"
4. **Fill checkout form** (scroll down):
   - Email
   - First name, Last name
   - Address, City, Postal code
   - Country
   - Phone number
   - Card number, Expiry, CVV

### On Drop Day (11:00 AM GMT - Thursday)

1. Open Supremebot: `python main.py`
2. Go to http://localhost:8080
3. Verify your basket and checkout info
4. At **exactly 11:00 AM**, click **"Start Supremebot"**
5. Watch the bot add items and fill checkout
6. **Manually click the final submit button** when the bot pauses

## Troubleshooting

### "python not found"
- Reinstall Python and check "Add to PATH"
- Try `python3` instead of `python`

### "pip not found"
- Try `python -m pip install ...` instead of `pip install ...`

### Bot doesn't find items
- Items only appear on Supreme when the drop is live
- Make sure you're running at drop time (11:00 AM)

### Page won't load
- Make sure no other program is using port 8080
- Try closing and reopening the terminal

## Tips for Success

1. **Prepare early** - Add items to basket the night before
2. **Fast internet** - Use wired connection if possible
3. **Be ready at 10:58 AM** - Don't be late
4. **Keep it small** - 2-3 items max for best success
5. **Have backup sizes** - Popular sizes sell out fast

## Important Notes

- Your personal info (card, address) is **never saved to files**
- Data only exists while the app is running
- Each person needs their **own** computer and payment info
- Supreme may cancel orders if they detect automation

Good luck!
