# Birthday Reminder Script

## Overview

This Python script helps to manage and automate birthday reminders for colleagues. It takes a list of users with their birth dates and returns a list of upcoming birthdays within a specified number of days. If a birthday falls on a weekend, the script adjusts the date to the next working Monday.

## Features

1.Converts date strings into Python date objects.
2.Checks for upcoming birthdays within a given number of days.
3.Adjusts birthdays that fall on weekends to the next Monday.
4.Handles past birthdays and moves them to the next year if needed.

## Usage

```
users = [
    {"name": "Bill Gates", "birthday": "1955.3.25"},
    {"name": "Steve Jobs", "birthday": "1955.3.21"},
    {"name": "Jinny Lee", "birthday": "1956.3.22"},
    {"name": "Sarah Lee", "birthday": "1957.3.23"},
    {"name": "Jonny Lee", "birthday": "1958.3.22"},
    {"name": "John Doe", "birthday": "1985.01.23"},
    {"name": "Jane Smith", "birthday": "1990.01.27"}
]

prepared_users = prepare_user_list(users)
upcoming_birthdays = get_upcoming_birthdays(prepared_users, days=7)
print(upcoming_birthdays)
```

Example Output

```
If today is March 20, 2024, the output may look like this:

[
    {"name": "Steve Jobs", "congratulation_date": "2024.03.21"},
    {"name": "Jinny Lee", "congratulation_date": "2024.03.22"},
    {"name": "Sarah Lee", "congratulation_date": "2024.03.25"}
]
```

## Notes

1.Ensure dates are formatted correctly in YYYY.M.D format.
2.If a birthday has already passed this year, it will be moved to the next year.
3.Birthdays falling on weekends are shifted to the next Monday.