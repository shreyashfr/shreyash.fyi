# DNS Setup Instructions

## ⚠️ Current Status

The CNAME file has been **temporarily removed** to stop the redirect loop.

**Current URL**: https://shreyashfr.github.io/shreyash.fyi/

This URL works perfectly now! Use it until your custom domain DNS is ready.

---

## 🌐 Setting Up Custom Domain (shreyash.fyi)

### Step 1: Configure Namecheap DNS

1. **Login to Namecheap** → Domain List → Manage `shreyash.fyi`
2. Go to **Advanced DNS** tab
3. **Delete all existing records** (parking page, URL redirects, etc.)
4. Add these records:

**A Records** (add all 4):
```
Type: A Record | Host: @ | Value: 185.199.108.153 | TTL: Automatic
Type: A Record | Host: @ | Value: 185.199.109.153 | TTL: Automatic
Type: A Record | Host: @ | Value: 185.199.110.153 | TTL: Automatic
Type: A Record | Host: @ | Value: 185.199.111.153 | TTL: Automatic
```

**CNAME Record**:
```
Type: CNAME | Host: www | Value: shreyashfr.github.io. | TTL: Automatic
```

5. **Save All Changes**

### Step 2: Wait for DNS Propagation

- Takes **30 minutes to 48 hours**
- Usually live in 1-2 hours
- Check status: https://www.whatsmydns.net/
  - Enter: `shreyash.fyi`
  - Type: `A`
  - Should see GitHub IPs: 185.199.108.153, etc.

### Step 3: Test DNS is Working

Open terminal and run:
```bash
nslookup shreyash.fyi
```

You should see GitHub Pages IP addresses (185.199.108.153, etc.)

### Step 4: Add CNAME File Back

Once DNS is fully propagated (you see green checkmarks on whatsmydns.net):

1. Create file named `CNAME` (no extension)
2. Add single line: `shreyash.fyi`
3. Commit and push:

```bash
echo "shreyash.fyi" > CNAME
git add CNAME
git commit -m "Re-add CNAME after DNS propagation"
git push origin main
```

4. Wait 2-3 minutes for GitHub Pages to rebuild
5. Visit https://shreyash.fyi - should work!

### Step 5: Enable HTTPS (Important!)

1. Go to: https://github.com/shreyashfr/shreyash.fyi/settings/pages
2. Wait for green checkmark next to "Custom domain"
3. Check the box: **"Enforce HTTPS"**
4. Done! Your site is secure.

---

## 🐛 Troubleshooting

### Still getting redirect loop?
- Clear browser cache and cookies
- Try incognito mode
- Make sure DNS has fully propagated (check whatsmydns.net)
- Wait 10-15 minutes after adding CNAME file

### DNS not propagating?
- Double-check all 4 A records are correct
- Make sure you deleted old Namecheap parking page records
- Some ISPs cache DNS longer - try using Google DNS (8.8.8.8)

### GitHub Pages says "DNS check unsuccessful"?
- Make sure CNAME record points to `shreyashfr.github.io.` (note the dot at end)
- Wait another hour - DNS can be slow

---

## 📌 Quick Reference

| Setting | Value |
|---------|-------|
| **Current working URL** | https://shreyashfr.github.io/shreyash.fyi/ |
| **Target custom URL** | https://shreyash.fyi |
| **GitHub repo** | https://github.com/shreyashfr/shreyash.fyi |
| **DNS check tool** | https://www.whatsmydns.net/ |

---

## ✅ Checklist

- [ ] Add 4 A records in Namecheap
- [ ] Add CNAME record in Namecheap
- [ ] Delete old parking page records
- [ ] Wait for DNS propagation (check whatsmydns.net)
- [ ] All locations show green checkmarks
- [ ] Add CNAME file to repo
- [ ] GitHub Pages detects custom domain
- [ ] Enable HTTPS in GitHub Pages settings
- [ ] Test https://shreyash.fyi

---

**For now**: Use https://shreyashfr.github.io/shreyash.fyi/ - it works perfectly! 🚀
