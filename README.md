# NexDrop - Secure File Sharing Platform

NexDrop is a modern, fast, and secure file-sharing web application that allows users to upload images, videos, and audio files and generate protected shareable links.

## Features
- **Upload Files**: Support for JPG, PNG, MP4, MOV, MP3, WAV up to 500MB.
- **Drag & Drop**: Modern UI with a glassmorphism effect and glowing borders.
- **Secure Links**: Unique UUID-based shareable links.
- **Password Protection**: Option to protect links with a password.
- **Expiration Control**: Set links to expire after 1 hour, 24 hours, 7 days, or 30 days.
- **Download Limits**: Set a maximum number of downloads for a link.
- **Real-time Progress**: Visual upload progress tracking.
- **Modern UI**: Dark mode, responsive design, and smooth animations using Tailwind CSS and Framer Motion.
- **QR Code Sharing**: Generate QR codes for easy mobile sharing.

## Tech Stack
- **Frontend**: React, Vite, Tailwind CSS, Framer Motion, Lucide React.
- **Backend**: Node.js, Express, MongoDB.
- **Security**: bcrypt for password hashing, UUID for private links.
- **Storage**: Configurable for Local Storage or AWS S3/Cloudflare R2.

## Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (Local or Atlas)

### Installation

1. **Clone the project**
2. **Setup Backend**
   ```bash
   cd backend
   npm install
   ```
3. **Configure Environment Variables**
   Create a `.env` file in the `backend` folder:
   ```env
   PORT=5000
   MONGODB_URI=your_mongodb_connection_string
   FRONTEND_URL=http://localhost:5173
   ```
4. **Start Backend**
   ```bash
   npm start
   ```
5. **Setup Frontend**
   ```bash
   cd ../frontend
   npm install
   ```
6. **Start Frontend**
   ```bash
   npm run dev
   ```

## Security Features
- **Hashed Passwords**: Passwords are never stored in plain text.
- **Private Link IDs**: Unique identifiers prevent guessing link URLs.
- **Automatic Cleanup**: Files and links are automatically deleted upon expiration using MongoDB TTL indexes.

## UI Design
- **Glassmorphism**: Soft blurred backgrounds and translucent elements.
- **Glow Effects**: Interactive glowing borders for the upload area.
- **Responsive**: Fully optimized for mobile, tablet, and desktop views.
