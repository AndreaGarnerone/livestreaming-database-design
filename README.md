# Live Streaming Database Design

This repository contains the design of a **database for a live streaming service**, similar in spirit to modern live streaming platforms.

The project focuses on **conceptual and logical data modeling**, defining entities, relationships, constraints, and supported operations for managing users, channels, live streams, videos, and interactions.

This is an academic-style project developed to practice database design principles.

---

## Project Overview

The platform allows users to watch and create live streams on different topics.

- Users can be **viewers**, **streamers**, or both
- Viewers may be registered or anonymous
- Registered users can chat, follow streamers, subscribe to channels, and create live streams
- Streamers own a channel where they can host live streams, videos, and clips

The database is designed to support both **content consumption** and **creator analytics**.

---

## Core Features Modeled

### Users
- Username, password, date of birth
- Contact information (phone number or email)
- Wallet of virtual currency (bits)
- Public chat and private messaging

### Channels
- One channel per streamer
- Channel description, profile image, trailer
- Associated social media links
- Follower count

### Content
- Live streams (with title, duration, category, tags)
- Videos (past live streams)
- Clips (short videos)
- Live streams may or may not become videos
- URLs are stored instead of actual media files

### Statistics
- Average number of viewers for live streams
- View count for videos and clips
- Total minutes streamed
- Number of live streams performed
- Average concurrent viewers per streamer

---

## Monetization and Engagement

- Viewers can follow channels
- Paid subscriptions grant special privileges
- Users can donate virtual currency (bits) to streamers
- Followers and subscriptions are tracked per channel

---

## Affiliate Program

A streamer becomes an **affiliate** when all of the following conditions are met:

- At least **500 minutes streamed**
- An average of **3 or more concurrent viewers**
- At least **50 followers**

The database supports a **daily check** of these conditions.

---

## Scheduling and Ranking

- Streamers can schedule future live streams using a calendar
- Weekly rankings of the most followed streamers are supported

---

## Supported Operations

The database is designed to efficiently support:

- Daily affiliate qualification checks
- Weekly ranking of most-followed streamers
- Viewer follow lists
- Stream scheduling
- Aggregated statistics and analytics

---

## Scope and Assumptions

- Multimedia content is handled by an external hosting platform
- Only media URLs are stored in the database
- The project focuses on data modeling, not application logic or UI

---

## License

This project is intended for educational purposes.
