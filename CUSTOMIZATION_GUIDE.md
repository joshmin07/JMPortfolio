# Portfolio Website - Customization Guide

## Features Implemented

### ✨ Expandable Project Section
- Click "View Project" button to expand the Moonveil Studios project
- Shows 3 placeholder images (replace with your actual screenshots)
- Displays Discord and GitHub links with logos
- Click "Hide Details" to collapse the section

### 🎨 Contact Buttons with Logos
- Email button with mail icon
- GitHub button with GitHub logo
- LinkedIn button with LinkedIn logo

## How to Customize

### Replace Project Images
1. Add your actual project screenshots to the `public` folder
2. Update the `images` array in `app/page.js`:
```javascript
images: [
  "/your-screenshot-1.jpg",
  "/your-screenshot-2.jpg",
  "/your-screenshot-3.jpg"
]
```

### Add Links to Other Projects
For projects 2 and 3, add the same structure as project 1:
```javascript
{
  id: 2,
  title: "Your Project Title",
  description: "Your description",
  technologies: ["Tech1", "Tech2"],
  discordLink: "https://discord.gg/your-invite", // optional
  githubLink: "https://github.com/your-repo",     // optional
  images: [
    "/image1.jpg",
    "/image2.jpg"
  ]
}
```

### Update Contact Information
Edit the contact links in `app/page.js` (around line 184):
- Email: Update `href="mailto:your-email@example.com"`
- GitHub: Update `href="https://github.com/your-username"`
- LinkedIn: Update `href="https://linkedin.com/in/your-profile"`

### Customize Colors
Edit `app/page.module.css`:
- Main gradient: Lines 11-12 (currently purple gradient)
- Accent color: Search for `#667eea` and `#764ba2`

## Running the Website

```bash
npm run dev
```

Visit `http://localhost:3000` to see your portfolio.

## Building for Production

```bash
npm run build
npm start
```

## Notes
- Only the first project (Moonveil Studios) has the expandable feature enabled
- Add the same `images`, `discordLink`, and `githubLink` properties to other projects to enable their expansion
- Placeholder images are SVGs in the `public` folder - replace them with actual screenshots
