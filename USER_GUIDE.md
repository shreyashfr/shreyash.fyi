# Website User Guide

## 🌐 Your Website is Live!

**URLs:**
- Temporary: https://shreyashfr.github.io/shreyash.fyi/
- Custom (after DNS): https://shreyash.fyi

---

## 🎨 What's New

### 1. **Two-Column Layout**
- **Left side**: Your title, headline, and bio (sticky on desktop)
- **Right side**: Cal.com booking widget
- Responsive design collapses to single column on mobile

### 2. **Mentorship Page Authentication**
Your mentorship page is now protected! Here's how it works:

**For users to access `/suchi.html`:**
1. Click "mentorship" in navigation
2. Enter token: `suchi`
3. Enter email: `suchitiwari0509@gmail.com`
4. Enter password: `suchi9832`
5. They get access to the full mentorship plan

### 3. **Admin Panel** 🔐

**Access:** https://shreyash.fyi/admin.html

**Password:** `shreyashisadmin`

**What you can edit:**
- Main title (default: "fyi by shreyash")
- Subtitle/headline
- Bio paragraph 1
- Bio paragraph 2

**Features:**
- ✅ Live preview as you type
- ✅ Save/discard changes
- ✅ Changes persist across sessions (localStorage)
- ✅ Instant updates on homepage

---

## 📝 How to Use the Admin Panel

1. **Go to** https://shreyash.fyi/admin.html
2. **Enter password**: `shreyashisadmin`
3. **Edit your content** in the form fields
4. **Watch live preview** update in real-time below
5. **Click "Save Changes"** when done
6. **Refresh homepage** to see updates

---

## 🔐 Credentials Summary

### Admin Panel
- URL: `/admin.html`
- Password: `shreyashisadmin`

### Mentorship Page (Suchi)
- Token: `suchi`
- Email: `suchitiwari0509@gmail.com`
- Password: `suchi9832`

---

## 🛠️ Making Changes

### To update content (easy way):
Use the admin panel at `/admin.html`

### To update structure (advanced):
1. Edit HTML files locally
2. Commit:
   ```bash
   git add .
   git commit -m "Update website"
   git push origin main
   ```
3. Live in 1-2 minutes

---

## 📱 Testing Checklist

- [ ] Visit homepage - check layout
- [ ] Try booking widget
- [ ] Click mentorship - test authentication
- [ ] Access admin panel - edit content
- [ ] Check on mobile device
- [ ] Verify DNS propagation (after Namecheap setup)

---

## 🎯 Next Steps

1. **Configure Namecheap DNS** (see SETUP_NOTES.md)
2. **Test the admin panel** - try editing your bio
3. **Test mentorship auth** - make sure Suchi can access
4. **Share your link** - https://shreyash.fyi

---

## ⚠️ Important Notes

- Admin changes save to **localStorage** (browser storage)
- Each browser stores its own version
- Changes apply to anyone visiting from that browser
- For permanent changes, use the admin panel from the browser you'll use most
- Or edit HTML files directly for version-controlled changes

---

## 🐛 Troubleshooting

**Admin panel not loading?**
- Clear browser cache
- Try incognito mode
- Check if JavaScript is enabled

**Mentorship page redirecting?**
- Authentication clears on browser close
- Users need to re-authenticate each session

**Content not updating?**
- Hard refresh (Ctrl+Shift+R / Cmd+Shift+R)
- Clear localStorage in browser console: `localStorage.clear()`

---

## 📞 Support

For technical issues, check the GitHub repo:
https://github.com/shreyashfr/shreyash.fyi

Your website is ready to use! 🎉
