# Motivationbuddy

Motivation Buddy is a web app and Telegram bot that delivers personalised motivational messages to subscribers at their chosen times. Users sign up on the website, receive a unique code, and link their Telegram account to receive daily motivation.

## Table of Contents
- [Features] (#features)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Usage](#usage)

## Features

- Users subscribe via a web form, specifying their name, interest areas and preferred message times.
- Unique code generation for secure Telegram linking.
- Telegram bot sends motivational messages at user-specified times.
- Users can like/dislike messages; feedback is stored for future work to personalise further.
- Easy unsubscribe and resubscribe workflow.

## Installation

### Clone the repository

### Install dependencies

```
npm install
```

### Set up environment variables

Set the following environment variables (e.g., in a `.env` file):
- `DATABASE_URL`
- `TELEGRAM_BOT_TOKEN`

### Set up the database

```
npx prisma migrate deploy
```

```
node prisma/seed.js
```

### Start the app

```
node server.js
```

## Project structure
├── prisma/
│ ├── schema.prisma # Prisma database schema
│ └── seed.js # Seed script for messages
├── public/
│ ├── script.js # Frontend JS
│ └── styles.css # Frontend CSS
├── views/
│ └── index.ejs # Main web page template
├── telegram.js # Telegram bot logic
├── server.js # Express web server
├── prisma.js # Prisma Client instance
├── checkFeedback.js # Feedback from users
├── package.json
└── README.md

## Usage
- User visits the website and subscribes with their name and preferred times.
- User receives a unique code and a link to the Telegram bot.
- User starts the bot on Telegram and enters their unique code.
- Bot sends motivational messages at the specified times.
- User can like/dislike messages; feedback is stored for personalisation.
- User can unsubscribe anytime via the /unsubscribe command.
