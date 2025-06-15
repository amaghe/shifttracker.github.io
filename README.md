# 📅 Shift Schedule Dashboard

A dynamic, interactive web-based dashboard for managing employee shift schedules, calculating categorised work hours, and estimating compensation based on base salary. Designed for ease of use with intuitive visual elements, real-time updates, and CSV export functionality.

![screenshot](https://github.com/user-attachments/assets/d5d89531-8642-42f8-9783-f004fc77d4f2)

---

## 🚀 Features

- **Interactive Calendar**  
  Click to toggle shift days. Holidays and weekends are auto-highlighted.

- **Customizable Base Salary**  
  Adjust base salary and watch all pay calculations update in real-time.

- **Automated Calculations**  
  Breakdown of:
  - Shift Days
  - Holiday Count
  - Hours per Rate Category:
    - **Rate 1**: Mon–Fri 18:00–24:00
    - **Rate 2**: Mon–Sat 00:00–07:00
    - **Rate 3**: Sat 07:00–24:00 & all Sunday
    - **Holiday**: Full-day compensation
  - Corresponding pay per rate

- **Charts**  
  Visual representation of:
  - Monthly work hours per rate
  - Monthly pay breakdown

- **CSV Export**  
  Download a year’s data, including all hours, shift days, and pay totals.

---

## 🛠️ How It Works

### 📅 Calendar Logic
- Shift days are manually toggled by clicking calendar cells.
- Holidays are auto-detected (fixed + movable Swedish public holidays).
- Weekends are styled differently (Saturday, Sunday).

### 🧮 Compensation Rules
| Category | Time Range           | Multiplier (based on base salary) |
|----------|----------------------|-----------------------------------|
| Rate 1   | Mon–Fri 18:00–24:00  | ÷ 600                             |
| Rate 2   | Mon–Sat 00:00–07:00  | ÷ 400                             |
| Rate 3   | Sat 07:00–24:00, Sun | ÷ 300                             |
| Holiday  | Full shift           | ÷ 150                             |

Each selected day adds corresponding hour credits to its category.

---

## 📦 File Structure

```bash
Shift_Schedule_Dashboard.html  # Main HTML file with embedded JS and CSS
