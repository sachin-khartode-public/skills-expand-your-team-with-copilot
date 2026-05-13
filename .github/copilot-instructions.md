### Copilot Instructions

You are helping maintain the Mergington High School Extracurricular Activities website. This is a FastAPI-based web application that allows students to view and sign up for school activities.

## Project Overview

- **Purpose**: Provide a simple web interface for students to browse and register for extracurricular activities at Mergington High School.
- **Tech Stack**: Python FastAPI backend, MongoDB database, static HTML/CSS/JS frontend.
- **Key Features**: Activity listing, filtering by day/time, student signup (teacher-authenticated).

## Development Environment

For detailed setup and development instructions, please refer to our [Development Guide](../docs/how-to-develop.md).

### User Interaction

Consider the following when communicating with the staff.

- The staff is not technical. Explain in simple terms as much as possible and avoid software jargon.
- Any new code must be easy to maintain and understand, without significant coding experience.

## Program architecture

- The website users are the students and teachers. Make sure the user experience is simple.
- Do not make additional apps or services.
- Do not make command line tools.
- Do not create a long single file application. Always use an easy-to-understand directory structure.
- Only use HTML, CSS, Javascript, and Python. No other languages.

## Architecture

- `src/app.py`: Main FastAPI application with routing
- `src/backend/database.py`: MongoDB setup and initial data
- `src/backend/routers/`: API endpoints (activities, auth)
- `src/static/`: Frontend files (HTML, CSS, JS)
- Data stored in MongoDB with activities and teacher accounts

## Standards and Conventions

- Use descriptive variable/function names
- Follow Python PEP 8 style
- Include docstrings for functions
- Handle errors gracefully with appropriate HTTP status codes
- Validate input data
- Keep activities data consistent

## Common Tasks

Teachers may request:
- Adding new activities (name, description, schedule, max participants)
- Updating activity details (schedule changes, capacity adjustments)
- Modifying descriptions for better appeal
- Adding/removing participants (with teacher authentication)

When adding activities:
- Include schedule_details with days array, start_time, end_time (24-hour format)
- Set appropriate max_participants
- Start with empty participants list
- Ensure description is engaging and student-friendly

## Development Workflow

- Test changes locally before proposing
- Ensure database schema consistency
- Validate API responses
- Check for any breaking changes
