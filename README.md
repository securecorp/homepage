# Securecorp Static Website

This is a static website for **Securecorp (시큐어코퍼)**, a security consulting and MSSP firm. The project has been enhanced with a modern cybersecurity aesthetic.

## ☁️ AWS S3 Deployment Guide

This website is optimized for **AWS S3 Static Website Hosting**.

### Steps to Deploy:
1. **Create Bucket**: Create a new S3 bucket (e.g., `www.your-domain.com`).
2. **Upload Files**: Upload `index.html` and `error.html` to the root of the bucket.
3. **Enable Static Hosting**:
   - Go to **Properties** tab -> **Static website hosting**.
   - Select **Enable**.
   - Index document: `index.html`
   - Error document: `error.html`
4. **Set Permissions** (If not using CloudFront):
   - Uncheck "Block all public access".
   - Add a Bucket Policy to allow public read access:
     ```json
     {
         "Version": "2012-10-17",
         "Statement": [
             {
                 "Sid": "PublicReadGetObject",
                 "Effect": "Allow",
                 "Principal": "*",
                 "Action": "s3:GetObject",
                 "Resource": "arn:aws:s3:::YOUR-BUCKET-NAME/*"
             }
         ]
     }
     ```

## 🚀 Features

- **Responsive Design**: Fully responsive layout that works on desktop, tablet, and mobile.
- **Cybersecurity Aesthetic**: 
  - Interactive particle network background using `particles.js`.
  - Glassmorphism (frosted glass) UI elements.
  - Neon accent colors (`#00f2ff`) and glowing effects.
- **Professional Typography**: Uses `Lexend` for body text and `JetBrains Mono` for technical details.
- **Iconography**: Integrated `FontAwesome` for professional security-related icons.

## 📁 File Structure

- `index.html`: The main single-page website containing all HTML, CSS, and JavaScript.

## 🛠 Libraries Used (via CDN)

- [Particles.js](https://vincentgarreau.com/particles.js/) - For the network background effect.
- [FontAwesome](https://fontawesome.com/) - For interface icons.
- [Google Fonts](https://fonts.google.com/) - `Lexend` and `JetBrains Mono`.

## 🎨 Design System

- **Primary Color**: Deep Navy (`#050a14`)
- **Accent Color**: Neon Cyan (`#00f2ff`)
- **Text Color**: Light Grey (`#f1f5f9`) with Dim Grey (`#94a3b8`) for secondary text.

## 📝 Usage

Simply deploy the `index.html` file to any static hosting service (Netlify, Vercel, GitHub Pages, or AWS S3).
