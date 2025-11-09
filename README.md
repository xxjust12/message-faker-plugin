# Message Faker Plugin for Kettu/Vendetta

A plugin that allows you to create fake client-sided messages in Discord DMs. Messages appear to be from any user you specify, but they're only visible to you.

## Features

- ✨ Create fake messages from any user
- 📱 Beautiful mobile-friendly settings interface
- 🎨 Optional embed support (title, description, image)
- 📋 Easy paste buttons for user IDs
- ✅ Toast notifications for feedback
- 🧪 Quick test message feature
- 🔧 Console API for advanced usage

## Installation Instructions

### Method 1: Install via URL (Easiest)

1. **Host the plugin files:**
   - Upload the `manifest.json` and `index.js` files to a GitHub repository
   - Make sure the files are in the root of the repo or in a specific folder
   - Get the raw URL to the `manifest.json` file

2. **Install in Kettu:**
   - Open Discord with Kettu installed
   - Go to Settings → Vendetta → Plugins
   - Tap the "+" button
   - Paste the URL to your `manifest.json` file
   - Tap "Install"

### Method 2: Install Locally (For Development)

1. **Prepare the files:**
   - Make sure you have both `manifest.json` and `index.js` in the same folder
   - The folder name should be something like `message-faker`

2. **Host locally or on GitHub:**
   - Option A: Create a GitHub repository and push these files
   - Option B: Use a local file server (advanced)

3. **Install via Vendetta/Kettu:**
   - Follow the same steps as Method 1

### Method 3: Using GitHub (Recommended)

1. **Create a GitHub Repository:**
   - Go to https://github.com and create a new repository
   - Name it something like `kettu-message-faker`
   - Make it public

2. **Upload the files:**
   - Upload `manifest.json` and `index.js` to the repository
   - Commit the files

3. **Get the raw URL:**
   - Click on `manifest.json` in your repository
   - Click the "Raw" button
   - Copy the URL (it should look like: `https://raw.githubusercontent.com/yourusername/kettu-message-faker/main/manifest.json`)

4. **Install in Kettu:**
   - Open Discord on your iOS device with Kettu
   - Go to Settings → Vendetta → Plugins
   - Tap the "+" icon at the top right
   - Paste the raw URL to your `manifest.json`
   - Tap "Install" or "Add"
   - The plugin should now appear in your plugins list!

## How to Use

1. **Open Plugin Settings:**
   - Go to Settings → Vendetta → Plugins
   - Find "Message Faker" in your plugin list
   - Tap the wrench icon (🔧) to open settings

2. **Fill in the fields:**
   - **Target User ID**: The person whose DM you want the message to appear in
   - **From User ID**: The person who the message should appear to be from
   - **Message Content**: The text of the fake message
   - (Optional) Enable embed and fill in embed fields

3. **Send the fake message:**
   - Tap the green "📧 Send Fake Message" button
   - You should see a "✅ Fake message sent!" toast
   - Navigate to the DM with the target user
   - The fake message will appear in the conversation!

## Getting User IDs

To get a user's ID in Discord:

1. Enable Developer Mode:
   - Go to Settings → App Settings → Behavior
   - Enable "Developer Mode"

2. Get the ID:
   - Long press on a user's profile or message
   - Tap "Copy ID"
   - Paste it into the plugin settings using the paste buttons

## Important Notes

- ⚠️ **Client-sided only**: These messages are only visible to you. They don't actually send anything to Discord's servers.
- ⚠️ **DM must exist**: You need to have an existing DM conversation with the target user for the message to appear.
- ⚠️ **Not persistent**: Fake messages may disappear if you restart Discord or clear cache.
- ⚠️ **Use responsibly**: This is for testing and fun purposes only.

## Quick Test Feature

The "✏️ Quick Test Message" button automatically fills in test values so you can quickly see how the plugin works. It will create a fake message from yourself to yourself.

## Console API

For advanced users, you can use the console to inject messages programmatically:

```javascript
// Inject a fake message
window.messageFaker.inject(channelId, authorId, "Message content", embedObject);

// Create a fake message object
window.messageFaker.createMessage(channelId, authorId, "Message content", embedObject);

// Get DM channel ID with a user
window.messageFaker.getDMChannel(userId);
```

## Troubleshooting

**Plugin won't install:**
- Make sure the URL points to the raw `manifest.json` file
- Check that both `manifest.json` and `index.js` are in the same directory
- Try refreshing the plugins page

**Fake message doesn't appear:**
- Make sure you have an existing DM with the target user
- Try opening the DM conversation first, then sending the fake message
- Check that the user IDs are correct (18-19 digit numbers)

**"Could not find DM channel" error:**
- Open a DM conversation with the target user first
- Send them a real message to establish the DM channel
- Then try using the plugin again

**Plugin crashes or doesn't work:**
- Make sure you're using the latest version of Kettu/Vendetta
- Try uninstalling and reinstalling the plugin
- Check the console for error messages

## Support

If you encounter any issues:
1. Check the console for error messages (Settings → Vendetta → Developer → Console)
2. Make sure all fields are filled in correctly
3. Verify that you have an existing DM with the target user
4. Try the "Quick Test Message" feature first to verify the plugin works

## Credits

Created for Kettu/Vendetta mobile Discord clients.

## License

Free to use and modify. Use responsibly!

