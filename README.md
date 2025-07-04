# mtg-card-track-js
A web application for managing Magic: The Gathering card collections, built with Node.js, Express, and MongoDB.

# Built With

[TOC] 

## Features

**Core CRUD Features**
    - [x] Add Cards: Manually input new cards with all relevant attributes
    - [x] View Collection: Browse all cards in your collection
    - [x] Search Functionality: Filter cards by name, type, color, etc.
    - [x] Edit Cards: Update any field of existing cards
    - [x] Delete Cards: Remove cards from your collection

- **User System**
    - [x] User registration and authentication
    - [x] Role-based access control (Admin/User)    
    - [ ] Profile customization
    - [ ] Collection statistics

- **Collection Statistics**
    - [x] Total cards count
    - [ ] Value estimation
    - [ ] Breakdown by rarity
    - [ ] Color distribution

- **Deck Management**
    - [ ] Create and manage decks
    - [ ] Track card availability
    - [ ] Multiple format support
    - [ ] Deck statistics

## Prerequisites

- Node.js (v14 or higher)
- MongoDB
- npm or yarn

## Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/mtg-collection-js.git
cd mtg-collection-js
```

2. Install dependencies
```bash
npm install
```

3. Create a `.env` file in the root directory
```env
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
PORT=5000
```

4. Start the server
```bash
npm start
```

## API Endpoints

### Authentication
- `POST /api/auth/login` - User login
- `POST /api/users/register` - User registration

### Cards
- `GET /api/cards/search/:name` - Search cards by name
- `POST /api/cards/scryfall/id/:scryfallId` - Add card by Scryfall ID
- `POST /api/cards/scryfall/name/:cardName` - Add card by name

### Users
- `GET /api/users` - Get all users (Admin only)
- `GET /api/users/:username` - Get user by username
- `PATCH /api/users/:username` - Update user (Admin only)
- `DELETE /api/users/:username` - Delete user (Admin only)
