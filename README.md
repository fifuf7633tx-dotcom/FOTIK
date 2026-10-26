# FOTIK — সেটআপ গাইড

## ১. Firebase Console (project: wi-pot-d802d)
1. **Authentication → Sign-in method** → Email/Password চালু করুন।
2. **Authentication → Settings → Authorized domains** → আপনার Vercel ডোমেইন (যেমন `fotik.vercel.app`) যোগ করুন।
3. **Realtime Database → Rules** → `database.rules.json` এর কন্টেন্ট পেস্ট করে Publish।
4. **Storage → Get started** (নতুন প্রজেক্টে Blaze প্ল্যান লাগতে পারে) → **Rules** এ `storage.rules` পেস্ট করে Publish।
5. (ঐচ্ছিক) Project settings → Add app → **Web** — যে `appId` দেবে সেটা `index.html` এর `appId` এর জায়গায় বসান।

## ২. Watermark ডাউনলোডের জন্য CORS (একবারই)
Google Cloud Shell খুলে `cors.json` আপলোড করে চালান:
```
gsutil cors set cors.json gs://wi-pot-d802d.firebasestorage.app
```

## ৩. GitHub → Vercel
1. এই ফোল্ডারের সব ফাইল একটি GitHub repo তে আপলোড করুন।
2. vercel.com → Add New Project → repo Import → Framework: **Other** → Deploy।

## নোট
- ডাউনলোডে ভিডিও রিয়েল-টাইমে রি-এনকোড হয় (১ মিনিটের ভিডিও ≈ ১ মিনিট), ট্যাব খোলা রাখতে হবে।
- আপলোড লিমিট ১০০MB।
