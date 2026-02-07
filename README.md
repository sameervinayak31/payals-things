# Payal's Things ✨

A colorful, fun, and artistic personal website to track recipes, workouts, books, and create a vision board!

## Features

- 🍳 **Recipes**: Save and organize your favorite recipes with ingredients and instructions
- 💪 **Workouts**: Track your workout routines and mark them as complete
- 📚 **Books**: Keep a reading list with ratings and notes
- 🎨 **Vision Board**: Create an inspiring vision board with goals, dreams, and affirmations

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
git commit -m "Initial commit"

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

## How It Works

### Data Storage
- All data is stored in your browser's **localStorage**
- Data persists between sessions on the same browser
- Each page has its own storage:
  - Recipes stored in `localStorage.recipes`
  - Workouts stored in `localStorage.workouts`
  - Books stored in `localStorage.books`
  - Vision board stored in `localStorage.visionBoard`

### Important Notes
- ⚠️ Data is stored **locally in your browser only**
- Clearing browser data will delete your saved items
- Data won't sync between different browsers or devices
- For backup, you can export data from browser's Developer Tools → Application → Local Storage

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
