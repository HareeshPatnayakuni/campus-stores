# Campus Stores

## Would I keep it? Yes, with one change

I worked the whole shift: issued the Film Society kit to Kabir at 3:45, took the partial return at 7:30, and closed the adapter loan as the morning clerk at 9:00.

To try my version, open `index.html`. There's a **Proposed / Original** switch at the top, so you can run the same shift both ways.

## What works well

The pickup. Kabir was waiting and the film started at four, and I never had to check the inventory. The projector that's in the workshop (PR-06) never showed up as an option, so I couldn't hand him a broken one. When I tried to issue a camera that wasn't on the form, and then a second adapter, it stopped me both times.

It's a bit slow, since one kit needs three separate slips. But it never let me make a mistake.

## What I'd change

The return at 7:30. Kabir brought back the projector and speaker and said Leela had the adapter and would drop it off at 9 the next morning. The app had no way to record that. The adapter's slip still said "Kabir Sen, due Fri 8 pm", so all I could do was leave it open and write a note in the desk book.

The next morning, that note was the only link. Leela's name wasn't on any slip. I had to go read the desk book, work out that her adapter was AD-12 on Kabir's slip, then come back and close it, right next to Tara's mic slip with the same button. If the evening note had been vague or missing, the morning shift would have been stuck.

![Original register at 9 am](docs/before-9am.png)

## My change

When you record a return, you now get a checklist of everything in the kit. You tick what's on the counter. For anything that isn't there, the app asks who has it and when it'll be back, and it won't save until you answer.

That answer goes on the slip ("With Leela Das, back by Sat 9 am") and into the desk book automatically. There's also a "Who's at the counter?" filter, so the morning clerk can pick Leela's name and go straight to the right kit.

![The new return checklist at 7:30 pm](docs/after-730pm-return.png)

## The same shift with the change

- **3:45 pm:** Issuing works the same as before. The kit shows "Issued 2 of 3" until the adapter goes out, so it's obvious if something is missing.
- **7:30 pm:** I tick the projector and speaker. For the adapter I pick Leela Das and Sat 9 am, then save. No separate note needed.
- **9:00 am:** I pick Leela in "Who's at the counter?" and her adapter shows up highlighted. I check the tag, tick it and save. Kit complete, and I never opened the desk book.

![Morning shift, filtered to Leela](docs/after-9am-counter.png)

## What I kept

One slip per item, the checks at pickup, the desk book for messages that don't fit a form, and the pickup flow itself. I left pickup alone on purpose so this change can be judged on its own.

## How I'd know it helped

I'd watch the morning shift when someone returns an item that isn't in their name. If the clerk finds the right slip without asking "which booking is this for?" or opening the desk book, it worked.

## Things I noticed but didn't change

Pickup could be faster (one form for a whole kit), and the app doesn't check who is allowed to collect for a club. Both are worth doing next, but neither one makes you lose track of equipment.

---

**Files I changed:** `app.js`, `styles.css`, `index.html` (the switch), and screenshots in `docs/`. The original register is still there behind the Original switch.



# Campus Stores

Campus Stores is a Product Engineer work sample set at a fictional campus media equipment desk. Work through a club’s screening, from equipment pickup to a partial return and the next morning’s handover. Open **Candidate brief** in the app for the assignment.

## Run the app

Open `index.html` in a modern browser. The app includes its scripts, styles, and icons and can run offline.

To serve it over local HTTP, run this from the repository folder and visit `http://localhost:8000`.

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Each browser stores its own sample shift locally when browser storage is available. **Restart sample shift** restores the fictional starting records.

## Source

- `index.html` contains the desk layout, candidate brief, and bundled icons.
- `app.js` contains the sample records and interactions.
- `styles.css` defines the desktop and mobile layouts.

Icon license notices are in [third-party/lucide-LICENSE.txt](third-party/lucide-LICENSE.txt).


## Submit your work

1. [Fork Campus Stores](https://github.com/virinchi-healthcare/campus-stores/fork) into your GitHub account. Complete the candidate brief and push your changes to your public fork. In your README, point reviewers to your work and explain the decision you made.
2. In your fork, open **Commits**, select the final commit you want reviewed, and copy the page URL. It should look like `https://github.com/YOUR-USERNAME/campus-stores/commit/COMMIT-SHA`.
3. [Submit your work through the Google Form](https://docs.google.com/forms/d/e/1FAIpQLScvzoh1R4WS-SkiwAVBQbMvniieJYSoOEfLMyVo5CyjOvYUgQ/viewform). Your **roll number**, **email ID**, and **final commit link from your public fork** are required. Enter your roll number and email ID in the form only.
