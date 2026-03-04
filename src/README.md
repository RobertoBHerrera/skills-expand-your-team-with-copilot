# Mergington High School Activities

A website application that allows students to view and sign up for extracurricular activities at Mergington High School.

## Features

- View all available extracurricular activities
- Filter activities by category (Sports, Arts, Academic, Community, Technology)
- Filter activities by day of the week
- Filter activities by time of day (Before School, After School, or Weekend)
- Search activities by name
- Teacher login/logout for authenticated actions
- Sign up students for activities (requires teacher authentication)
- Unregister students from activities (requires teacher authentication)

## Tech Stack

- **Backend**: FastAPI (Python)
- **Database**: MongoDB
- **Frontend**: Vanilla HTML, CSS, and JavaScript

## Available Activities

| Activity | Category | Schedule |
|----------|----------|----------|
| Chess Club | Academic | Mondays and Fridays, 3:15 PM - 4:45 PM |
| Programming Class | Technology | Tuesdays and Thursdays, 7:00 AM - 8:00 AM |
| Morning Fitness | Sports | Mondays, Wednesdays, Fridays, 6:30 AM - 7:45 AM |
| Soccer Team | Sports | Tuesdays and Thursdays, 3:30 PM - 5:30 PM |
| Basketball Team | Sports | Wednesdays and Fridays, 3:15 PM - 5:00 PM |
| Art Club | Arts | Thursdays, 3:15 PM - 5:00 PM |
| Drama Club | Arts | Mondays and Wednesdays, 3:30 PM - 5:30 PM |
| Math Club | Academic | Tuesdays, 7:15 AM - 8:00 AM |
| Debate Team | Academic | Fridays, 3:30 PM - 5:30 PM |
| Weekend Robotics Workshop | Technology | Saturdays, 10:00 AM - 2:00 PM |
| Science Olympiad | Academic | Saturdays, 1:00 PM - 4:00 PM |
| Sunday Chess Tournament | Academic | Sundays, 2:00 PM - 5:00 PM |
| Manga Maniacs | Arts | Tuesdays, 5:00 PM - 6:00 PM |

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/activities` | Get all activities; optional query params: `day`, `start_time`, `end_time` |
| GET | `/activities/days` | Get a list of all days that have activities scheduled |
| POST | `/activities/{activity_name}/signup` | Sign up a student for an activity; query params: `email`, `teacher_username` (required) |
| POST | `/activities/{activity_name}/unregister` | Remove a student from an activity; query params: `email`, `teacher_username` (required) |
| POST | `/auth/login` | Login as a teacher; query params: `username`, `password` |
| GET | `/auth/check-session` | Check if a session is valid; query param: `username` |

## Development Guide

For detailed setup and development instructions, please refer to our [Development Guide](../docs/how-to-develop.md).
