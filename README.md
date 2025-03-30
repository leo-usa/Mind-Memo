# Mind Memo

Mind Memo is a modern note-taking application that helps you organize and summarize your thoughts using AI. Built with Next.js 14, TypeScript, and Tailwind CSS, it offers a seamless experience for creating, managing, and analyzing your notes.

## Features

- 📝 Create and manage notes with a clean, intuitive interface
- 🤖 AI-powered note summarization
- 🔍 Smart search functionality
- 🎨 Modern, responsive design with Tailwind CSS
- 🌙 Dark mode support
- 🔒 Secure authentication with Firebase
- 💾 Real-time data synchronization
- 🌐 Multi-language support

## Tech Stack

- **Frontend**: Next.js 14, React, TypeScript
- **Styling**: Tailwind CSS, Radix UI
- **Authentication**: Firebase Auth
- **Database**: Firebase Firestore
- **AI Integration**: Replicate API
- **State Management**: React Context
- **Deployment**: Vercel

## Getting Started

### Prerequisites

- Node.js 18.x or later
- npm or yarn
- Firebase account
- Replicate API key

### Installation

1. Clone the repository:
```bash
git clone https://github.com/leo-usa/Mind-Memo.git
cd Mind-Memo
```

2. Install dependencies:
```bash
npm install
# or
yarn install
```

3. Create a `.env.local` file in the root directory and add your environment variables:
```env
NEXT_PUBLIC_FIREBASE_API_KEY=your_firebase_api_key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_firebase_project_id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_firebase_storage_bucket
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_firebase_messaging_sender_id
NEXT_PUBLIC_FIREBASE_APP_ID=your_firebase_app_id
REPLICATE_API_TOKEN=your_replicate_api_token
```

4. Run the development server:
```bash
npm run dev
# or
yarn dev
```

5. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Next.js](https://nextjs.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Firebase](https://firebase.google.com/)
- [Replicate](https://replicate.com/)
- [Radix UI](https://www.radix-ui.com/)
