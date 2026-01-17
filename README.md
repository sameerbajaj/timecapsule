# Time Capsule ⏳

> **A letter from your future self, written by product legends.**

Get personalized career advice from founders and product leaders who were in your **exact situation** — powered by 269 episodes of Lenny's Podcast.

![Time Capsule Preview](https://via.placeholder.com/800x400?text=Time+Capsule+Preview)

## ✨ What is this?

You tell us where you are in your career. We find leaders from Lenny's Podcast who were in that same spot years ago. Then we generate a letter with their hard-won wisdom — like a time capsule from your future self.

**Featured guests include:**
- Brian Chesky (Airbnb)
- Julie Zhuo (Facebook Design)
- Shreyas Doshi (Stripe, Twitter)
- Claire Hughes Johnson (Stripe)
- And 265+ more...

## 🚀 Try It

**Live:** [sameerbajaj.com/tools/timecapsule](https://sameerbajaj.com/tools/timecapsule)

## 🛠️ Run Locally

```bash
# Clone the repo
git clone https://github.com/sameerbajaj/timecapsule.git
cd timecapsule

# Install dependencies
cd app
npm install

# Add your Gemini API key
# Get a free key at https://aistudio.google.com/apikey
echo "GEMINI_API_KEY=your_key_here" > .env.local

# Run the dev server
npm run dev

# Open http://localhost:3000/tools/timecapsule
```

## 📦 Tech Stack

- **Next.js 16** — App Router, API Routes
- **TypeScript** — Type safety
- **Tailwind CSS** — Styling
- **Framer Motion** — Beautiful animations
- **Google Gemini 2.0 Flash** — AI letter generation
- **gray-matter** — Markdown parsing

## 🎯 How It Works

1. **User completes a sentence:** "I'm a [role] who just [situation] and I'm struggling with [challenge]"
2. **We match relevant transcripts:** Based on role and struggle, we select ~8 podcast transcripts from guests who've been there
3. **AI generates personalized advice:** Gemini reads the transcripts and finds quotes that speak directly to the user's situation
4. **Beautiful letter display:** Animated, shareable result

## 🏗️ Project Structure

```
lennys-transcripts/
├── app/                    # Next.js application
│   ├── app/
│   │   ├── api/generate/   # Gemini API route
│   │   ├── page.tsx        # Main app page
│   │   └── globals.css     # Styling
│   ├── components/         # React components
│   └── types/              # TypeScript types
└── data/                   # Podcast transcripts (gitignored, see below)
```

## 📚 Transcript Data

The transcripts come from [ChatPRD/lennys-podcast-transcripts](https://github.com/ChatPRD/lennys-podcast-transcripts).

To set up locally:
```bash
git clone https://github.com/ChatPRD/lennys-podcast-transcripts.git data
```

## 🚢 Deployment

### Vercel

1. Push to GitHub
2. Import to Vercel
3. Set environment variable: `GEMINI_API_KEY`
4. Configure base path if hosting at a subpath

### For subpath hosting (e.g., `/tools/timecapsule`):

The app is pre-configured with `basePath: "/tools/timecapsule"` in `next.config.ts`.

## ✍️ Inspiration

Built for the [Lenny's Podcast Transcripts Hackathon](https://github.com/ChatPRD/lennys-podcast-transcripts).

The idea: What if you could get a letter from your future self, written using wisdom from the best product minds in the world?

## 📝 License

MIT — Built with ❤️ for the product community

---

**Share your letter:** [@yourusername](https://twitter.com/yourusername)
