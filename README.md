# Payal's Things ✨

A colorful, fun, and artistic personal website to track recipes, workouts, books, and create a vision board! Now powered by Firebase for real-time sync across all devices.

## Features

- 🍳 **Recipes**: Save and organize your favorite recipes with ingredients, instructions, and URLs
- 💪 **Workouts**: Track your workout routines and mark them as complete
- 📚 **Books**: Keep a reading list with ratings, notes, and cover images
- 🎨 **Vision Board**: Create an inspiring vision board with goals, dreams, and affirmations
- 📸 **Image Gallery**: Upload and display images on the homepage
- ➕ **Custom Categories**: Create up to 10 custom category pages
- 🦋 **Beautiful Design**: Purple theme with animated butterflies, "meep" and "moop" floating text

## 🔥 Firebase Integration

All data is stored in Firebase Firestore and syncs automatically across all your devices! Any changes you make on one device will instantly appear on all others.

### Collections Used:
- `recipes` - All your recipes
- `workouts` - Workout routines
- `books` - Reading list
- `visionBoard` - Vision board items
- `homeImages` - Homepage gallery images (URLs only)
- `settings/categories` - Navigation categories

### Image Handling:
Images are added via URL only (no file uploads). You can:
- Upload images to [Imgur](https://imgur.com) or [ImgBB](https://imgbb.com)
- Copy the image URL
- Paste into the website

This keeps the site 100% free with no payment method required!

## How to Deploy to GitHub Pages

### Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right and select "New repository"
3. Name your repository (e.g., `payals-things`)
4. Make it **Public** (required for free GitHub Pages)
5. Click "Create repository"

### Step 2: Upload Your Files

**Option A: Using GitHub's Web Interface**
1. Click "uploading an existing file" link
2. Drag and drop all the HTML files:
   - `index.html`
   - `recipes.html`
   - `workouts.html`
   - `books.html`
   - `vision-board.html`
3. Click "Commit changes"

**Option B: Using Git Command Line**
```bash
# Navigate to the payals-things folder
cd /path/to/payals-things

# Initialize git
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit with Firebase"

# Add your repository as remote (replace YOUR-USERNAME and REPO-NAME)
git remote add origin https://github.com/YOUR-USERNAME/REPO-NAME.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click "Settings" (top menu)
3. Click "Pages" (left sidebar)
4. Under "Source", select "main" branch
5. Click "Save"
6. Wait a few minutes for deployment

### Step 4: Access Your Site

Your site will be available at:
```
https://YOUR-USERNAME.github.io/REPO-NAME/
```

For example: `https://payal.github.io/payals-things/`

## 🔒 Firebase Security

The current Firebase setup uses test mode rules which allow anyone to read and write. This is fine for personal use, but if you want to restrict access:

### Option 1: Simple Protection (Anyone can read, only you can write)
Go to Firestore Database → Rules and use:
```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read: if true;
      allow write: if request.auth != null;
    }
  }
}
```

Then add Firebase Authentication to your site.

### Option 2: Keep it fully open (current setup)
Good for personal use when you don't want to add login complexity.

## Data Storage Details

### Firestore Database
- **Free tier**: 1GB storage, 50K reads/day, 20K writes/day, 10GB/month downloads
- All data syncs in real-time across devices
- Data persists permanently (unlike localStorage)
- **No payment method required!**

### Images
- Images are stored as URLs in Firestore
- Use free image hosting services like [Imgur](https://imgur.com) or [ImgBB](https://imgbb.com)
- Copy/paste URLs into the site

## Customization

### Change Colors
Each page has its own color scheme in the `<style>` section:
- **Recipes**: Pink/coral gradient (`#f093fb` to `#f5576c`)
- **Workouts**: Blue gradient (`#4facfe` to `#00f2fe`)
- **Books**: Green gradient (`#43e97b` to `#38f9d7`)
- **Vision Board**: Orange/yellow gradient (`#fa709a` to `#fee140`)

### Modify Layout
All pages use CSS Grid for responsive layouts. Adjust the `grid-template-columns` property to change how items display.

## Browser Compatibility

Works on all modern browsers:
- Chrome/Edge (recommended)
- Firefox
- Safari
- Opera

## Support

If you have issues:
1. Make sure your repository is public
2. Check that GitHub Pages is enabled in Settings → Pages
3. Wait a few minutes after enabling Pages
4. Clear your browser cache if changes don't appear

Enjoy organizing your things! 🎉
