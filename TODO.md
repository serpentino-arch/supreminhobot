# Season Update Guide

The season URLs are currently hardcoded in `main.py`. When a new season starts (e.g., Fall/Winter 2026), you'll need to update them manually.

## When to Update

- **Spring/Summer** seasons typically start in February
- **Fall/Winter** seasons typically start in August

Check [SupremeCommunity](https://www.supremecommunity.com/) to see when the new season page is live.

## What to Change

Open `main.py` and find these two lines:

### Line ~366 (in `get_drop_dates` function)
```python
url: str = "https://www.supremecommunity.com/season/spring-summer2026/droplists/"
```

### Line ~457 (in `fetch_items` function)
```python
f"https://www.supremecommunity.com/season/spring-summer2026/droplist/{drop_date}"
```

## How to Update

1. Open `main.py` in a text editor
2. Press `Ctrl+H` (Find & Replace)
3. Replace `spring-summer2026` with the new season (e.g., `fall-winter2026`)
4. Save the file
5. Restart the bot

## Season URL Format

| Season | URL Format |
|--------|------------|
| Spring/Summer 2026 | `spring-summer2026` |
| Fall/Winter 2026 | `fall-winter2026` |
| Spring/Summer 2027 | `spring-summer2027` |

## Future Improvement

A season selector dropdown could be added to the UI to switch seasons without editing code. This would require modifying the `get_drop_dates` and `fetch_items` functions to accept a season parameter.
