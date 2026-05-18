# Landing Page

A beautiful, responsive landing page built with Node.js and Express, ready to deploy on Cloudflare Pages.

## Features

- Clean and modern design
- Fully responsive layout
- Fast and lightweight
- Easy to customize
- Ready for Cloudflare Pages deployment

## Local Development

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn

### Installation

1. Install dependencies:
```bash
npm install
```

2. Start the development server:
```bash
npm start
```

3. Open your browser and visit:
```
http://localhost:3000
```

## Project Structure

```
.
├── public/
│   ├── index.html      # Main HTML file
│   └── styles.css      # Stylesheet
├── server.js           # Express server
├── package.json        # Project dependencies
├── wrangler.toml       # Cloudflare configuration
└── README.md          # This file
```

## Deployment to Cloudflare Pages via GitHub

### Step 1: Push to GitHub

1. Create a new repository on GitHub (don't initialize with README)

2. Add all files and commit:
```bash
git add .
git commit -m "Initial commit: Landing page"
```

3. Add your GitHub repository as remote and push:
```bash
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git branch -M main
git push -u origin main
```

### Step 2: Deploy to Cloudflare Pages

1. Log in to your [Cloudflare Dashboard](https://dash.cloudflare.com/)

2. Go to **Pages** in the sidebar

3. Click **Create a project**

4. Select **Connect to Git**

5. Authorize Cloudflare to access your GitHub account

6. Select your repository from the list

7. Configure your build settings:
   - **Project name**: Choose a name (this will be your subdomain)
   - **Production branch**: `main`
   - **Build command**: Leave empty or use `npm install`
   - **Build output directory**: `public`

8. Click **Save and Deploy**

9. Wait for the deployment to complete (usually takes 1-2 minutes)

10. Your site will be live at: `https://YOUR_PROJECT_NAME.pages.dev`

### Step 3: Custom Domain (Optional)

1. In your Cloudflare Pages project, go to **Custom domains**
2. Click **Set up a custom domain**
3. Enter your domain name
4. Follow the DNS configuration instructions

## Updating Your Site

After making changes to your code:

```bash
git add .
git commit -m "Your commit message"
git push
```

Cloudflare Pages will automatically rebuild and deploy your changes.

## Customization

### Changing Colors

Edit the colors in [public/styles.css](public/styles.css):
- Primary color: `#2563eb` (blue)
- Gradient: `#667eea` to `#764ba2` (purple gradient)

### Changing Content

Edit the content in [public/index.html](public/index.html):
- Update the brand name, headings, and text
- Modify the feature cards
- Add or remove sections as needed

### Adding Images

1. Add your images to the `public/` directory
2. Reference them in your HTML:
```html
<img src="/your-image.jpg" alt="Description">
```

## Environment Variables (if needed)

For Cloudflare Pages, you can add environment variables:

1. Go to your project in Cloudflare Pages
2. Navigate to **Settings** > **Environment variables**
3. Add your variables for Production/Preview environments

## Troubleshooting

### Build fails on Cloudflare Pages

- Make sure your build output directory is set to `public`
- Check that all files are committed to your repository
- Review the build logs in the Cloudflare dashboard

### Changes not showing

- Clear your browser cache
- Check that your changes were pushed to GitHub
- Verify the deployment completed successfully in Cloudflare

## License

MIT
