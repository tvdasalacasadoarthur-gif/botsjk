# WhatsApp Bot for Laundry and Delivery Services

## Overview
This is a WhatsApp bot application that manages two main services:
1. **Lavanderia (Laundry)** - Manages laundry queue and scheduling
2. **Encomendas (Deliveries)** - Handles package delivery tracking and management

The bot automatically detects groups by name and provides specific functionality for each service type.

## Recent Changes (September 29, 2025)
- Imported from GitHub and configured for Replit environment
- Updated web server to bind to 0.0.0.0:5000 for proper Replit hosting
- Configured workflow to run the bot with webview output
- Set up VM deployment configuration for continuous operation

## Project Architecture
- **Main File**: `index.js` - Core WhatsApp bot logic and web server
- **Modules**:
  - `lavanderia.js` - Laundry service management
  - `encomendas.js` - Delivery service management
  - `lembretes.js` - Reminder functionality
- **Authentication**: WhatsApp session stored in `/auth` folder
- **Data Storage**: Groups configuration in `grupos.json`
- **External APIs**: 
  - SheetDB for logging and data persistence
  - WhatsApp Web via Baileys library

## Dependencies
- Node.js application using npm
- Key libraries: @whiskeysockets/baileys, express, axios, mongodb
- Web server runs on port 5000
- Uses QR code terminal for WhatsApp authentication

## Configuration
- Deployment: VM (virtual machine) for continuous operation
- Workflow: "WhatsApp Bot" running `npm start`
- Port: 5000 with webview output for status monitoring
- Host: 0.0.0.0 for Replit proxy compatibility

## Features
- Automatic group detection and registration
- Welcome/goodbye messages for group participants
- Laundry queue management with time scheduling
- Delivery tracking and confirmation system
- Data logging to external spreadsheets
- Web status endpoint for monitoring