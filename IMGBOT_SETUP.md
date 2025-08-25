# How to Use ImgBot as a Collaborator

ImgBot is a friendly GitHub bot that automatically optimizes images in your repository by creating pull requests with compressed versions of your images. This helps reduce your repository size and improve website loading times.

## 🤖 What is ImgBot?

ImgBot automatically:
- Scans your repository for images that can be optimized
- Compresses images without losing visual quality
- Creates pull requests with the optimized images
- Helps reduce your repository size and improve website performance

## 🚀 How to Add ImgBot to Your Repository

### Step 1: Install ImgBot from GitHub Marketplace
1. Go to the [ImgBot GitHub Marketplace page](https://github.com/marketplace/imgbot)
2. Click "Set up a plan" (it's free!)
3. Choose "Install it for free"
4. Select the repositories where you want ImgBot to work
5. Click "Install"

### Step 2: Grant Necessary Permissions
ImgBot needs these permissions to work:
- **Read access** to your repository contents
- **Write access** to create pull requests
- **Issues access** to post updates (optional)

### Step 3: Add ImgBot as a Collaborator (Alternative Method)
If you prefer to add ImgBot manually:
1. Go to your repository settings
2. Click "Manage access" or "Collaborators"
3. Click "Add people"
4. Search for `imgbot[bot]` or `ImgBot`
5. Add with "Write" permissions

## ⚙️ Configuration

This repository includes an `.imgbotconfig` file with the following settings:

```json
{
    "schedule": "daily",
    "compressImagesInSubDirectories": true,
    "aggressiveCompression": false,
    "ignoredFiles": ["*.avif"],
    "minKBReduced": 10,
    "prTitle": "[ImgBot] Optimize images",
    "compressWEBP": true,
    "compressPNG": true,
    "compressJPG": true,
    "compressSVG": true
}
```

### Configuration Explained:
- **schedule**: `"daily"` - ImgBot will check for new images daily
- **compressImagesInSubDirectories**: `true` - Optimizes images in folders like `Thumbnail/` and `profile-picture/`
- **aggressiveCompression**: `false` - Uses lossless compression to maintain quality
- **ignoredFiles**: `["*.avif"]` - Skips AVIF files (already well-optimized)
- **minKBReduced**: `10` - Only creates PRs if at least 10KB can be saved
- **Image formats**: Optimizes WEBP, PNG, JPG, and SVG files

## 📁 Images in This Repository

ImgBot will optimize these images:
- **Logo**: `resources/logo-removebg-preview.png` (92KB) - Good candidate for optimization
- **Thumbnails**: `Thumbnail/*.jpg` files (12KB-40KB) - Can be optimized
- **Profile Pictures**: `profile-picture/*.jpg` files (8KB-20KB) - Can be optimized

## 🔄 How ImgBot Works

1. **Automatic Detection**: ImgBot scans your repository daily for new or modified images
2. **Optimization**: Compresses images using lossless algorithms
3. **Pull Request**: Creates a PR with optimized images
4. **Review**: You review the changes to ensure everything looks good
5. **Merge**: Merge the PR to apply the optimizations

## 📊 Expected Benefits

For your YouTube clone project, ImgBot can:
- Reduce image file sizes by 10-30% on average
- Improve website loading speed
- Reduce bandwidth usage for visitors
- Keep your repository size manageable
- Maintain image quality while reducing file size

## 🔍 What to Review in ImgBot PRs

When ImgBot creates a pull request:
1. **Check the images visually** - Make sure they still look good
2. **Review the file size reduction** - Verify the savings are worthwhile
3. **Test your website** - Ensure images still display correctly
4. **Merge the PR** - If everything looks good!

## 🚫 Troubleshooting

### ImgBot isn't working?
- Check that ImgBot has proper permissions
- Ensure your repository is public or you have a paid GitHub plan
- Verify the `.imgbotconfig` file is valid JSON
- Make sure there are images that meet the `minKBReduced` threshold

### Images not being optimized?
- Check if the file format is supported (PNG, JPG, WEBP, SVG)
- Verify the files aren't in the `ignoredFiles` list
- Ensure the potential savings exceed the `minKBReduced` setting

## 📞 Support

- **ImgBot Documentation**: [imgbot.net/docs](https://imgbot.net/docs)
- **GitHub Issues**: [github.com/dabutvin/ImgBot/issues](https://github.com/dabutvin/ImgBot/issues)
- **ImgBot Website**: [imgbot.net](https://imgbot.net)

---

*Happy optimizing! 🎉*