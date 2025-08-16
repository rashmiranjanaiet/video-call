# LoveLink - Modern Dating Website

A modern, responsive dating platform for users aged 16-30 with video chat capabilities, built with React, TypeScript, and Tailwind CSS.

## 🚀 Live Demo

[View Live Site](https://yourusername.github.io/lovelink-dating-site)

## ✨ Features

- 🎯 **User Profiles & Authentication** - Complete registration and login system
- 💬 **Real-time Messaging** - Chat interface with message history
- 📹 **Video Call Integration** - WebRTC-ready video calling system
- 💰 **Subscription System** - 1 day free trial + $1/month pricing
- 📱 **Responsive Design** - Works perfectly on all devices
- 🔒 **Safe Environment** - Profile verification and reporting features
- 🎨 **Modern UI/UX** - Clean, Instagram-like interface
- ⚡ **Fast Performance** - Optimized with Vite and modern React

## 🛠️ Tech Stack

- **Frontend**: React 18, TypeScript
- **Styling**: Tailwind CSS
- **Build Tool**: Vite
- **Icons**: Lucide React
- **Deployment**: GitHub Pages, Netlify, Vercel

## 📦 Installation

### Prerequisites

- Node.js 18 or higher
- npm or yarn

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/lovelink-dating-site.git
   cd lovelink-dating-site
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start development server**
   ```bash
   npm run dev
   ```

4. **Open your browser**
   ```
   http://localhost:3000
   ```

## 🚀 Deployment

### GitHub Pages (Automatic)

1. **Update repository name** in `package.json` and `vite.config.ts`
2. **Push to GitHub**
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```
3. **Enable GitHub Pages** in repository settings
4. **Site will auto-deploy** via GitHub Actions

### Manual Deployment

```bash
# Build for production
npm run build

# Deploy to GitHub Pages
npm run deploy

# Deploy with custom base path
npm run deploy:github
```

### Other Platforms

#### Netlify
1. Build: `npm run build`
2. Publish directory: `dist`

#### Vercel
1. Connect GitHub repository
2. Build command: `npm run build`
3. Output directory: `dist`

#### Firebase Hosting
```bash
npm run build
firebase deploy
```

## 📁 Project Structure

```
lovelink-dating-site/
├── public/                 # Static assets
│   ├── vite.svg
│   └── favicon.ico
├── src/                    # Source code
│   ├── components/         # React components
│   │   ├── Header.tsx
│   │   ├── Hero.tsx
│   │   ├── ProfileCard.tsx
│   │   ├── ChatInterface.tsx
│   │   ├── VideoCallModal.tsx
│   │   ├── AuthModal.tsx
│   │   ├── ProfileGallery.tsx
│   │   ├── PricingSection.tsx
│   │   ├── AboutPage.tsx
│   │   ├── FAQPage.tsx
│   │   ├── ContactPage.tsx
│   │   └── Footer.tsx
│   ├── data/              # Mock data and types
│   │   └── mockProfiles.ts
│   ├── App.tsx            # Main app component
│   ├── main.tsx           # Entry point
│   └── index.css          # Global styles
├── .github/workflows/     # GitHub Actions
│   └── deploy.yml
├── package.json           # Dependencies and scripts
├── vite.config.ts         # Vite configuration
├── tailwind.config.js     # Tailwind CSS config
├── tsconfig.json          # TypeScript config
└── README.md              # This file
```

## 🎨 Customization

### Colors & Branding
Edit `tailwind.config.js` to customize the color scheme:

```javascript
theme: {
  extend: {
    colors: {
      primary: '#your-color',
      secondary: '#your-color'
    }
  }
}
```

### Mock Data
Update `src/data/mockProfiles.ts` to customize user profiles and demo content.

### Features
All components are modular and can be easily customized or extended.

## 🔧 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint
- `npm run deploy` - Deploy to GitHub Pages
- `npm run clean` - Clean build cache
- `npm run type-check` - Check TypeScript types

## 🌟 Key Components

### Authentication System
- Registration with profile creation
- Secure login modal
- User session management

### Profile System
- Detailed user profiles
- Photo galleries
- Interest tags and bio

### Messaging & Video
- Real-time chat interface
- Video call modal with controls
- Message history and timestamps

### Subscription System
- Free trial (1 day)
- Premium subscription ($1/month)
- Feature comparison

## 🔒 Security Features

- Profile verification system
- Report and block functionality
- Safe browsing environment
- Privacy-focused design

## 📱 Responsive Design

- Mobile-first approach
- Tablet and desktop optimized
- Touch-friendly interface
- Cross-browser compatibility

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

- 📧 Email: support@lovelink.com
- 💬 Issues: [GitHub Issues](https://github.com/yourusername/lovelink-dating-site/issues)
- 📖 Docs: [Wiki](https://github.com/yourusername/lovelink-dating-site/wiki)

## 🙏 Acknowledgments

- React team for the amazing framework
- Tailwind CSS for the utility-first CSS framework
- Lucide for the beautiful icons
- Vite for the lightning-fast build tool

---

Made with ❤️ for meaningful connections