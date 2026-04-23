# Module 3: Automating Your Business

## Welcome

In Module 2, you set up your tools. Now we're going to make them work while you sleep.

Automation is where AI goes from "neat trick" to "actual business impact." This module walks you through building specific automations that run on their own — following up with leads, reminding customers about appointments, collecting reviews, and keeping your business moving even when you're off the clock.

---

## Lesson 1: The Lead Response Machine

The fastest way to lose a customer? Make them wait.

Here's the reality:

| Response Time | Chance of Closing |
|---------------|-------------------|
| Under 5 minutes | 9x more likely |
| Under 1 hour | 7x more likely |
| Under 24 hours | 5x more likely |
| Over 24 hours | Almost zero |

Most local businesses take 12-48 hours to respond to leads. By then, the customer has already called someone else.

**The fix:** An automation that responds instantly and keeps following up until they book or say no.

### Building Your Lead Response Automation

In GoHighLevel:

**Step 1: Create the workflow**
1. Go to Automation → Workflows → Create New
2. Name it "New Lead Response"
3. Set the trigger: "Contact tag added" → tag name: "new-lead"

**Step 2: Instant response (0 minutes)**
1. Add action: Send SMS
2. Message: "Hi {first_name}! Thanks for reaching out to [Business Name]. I got your message and I'll be in touch shortly. In the meantime, feel free to book a time that works for you here: [booking link]"
3. Add action: Internal notification (email to you) — "New lead: {first_name} {last_name} — {phone} — {email}"

**Step 3: Follow-up 1 (24 hours later, if no appointment booked)**
1. Add action: Wait → 24 hours
2. Add condition: "Has appointment booked?" → No
3. Add action: Send SMS
4. Message: "Hi {first_name}, just checking in! I wanted to make sure you had everything you need. Do you have any questions I can help with?"

**Step 4: Follow-up 2 (3 days later, if still no appointment)**
1. Add action: Wait → 3 days
2. Add condition: "Has appointment booked?" → No
3. Add action: Send SMS
4. Message: "Hey {first_name}, I know things get busy! Just wanted to remind you that I'm here whenever you're ready. Here's my booking link again if that's easier: [link]"

**Step 5: Follow-up 3 (7 days later — final nudge)**
1. Add action: Wait → 7 days
2. Add condition: "Has appointment booked?" → No
3. Add action: Send SMS
4. Message: "Hi {first_name}, this is my last message — I don't want to bug you! If you still need help with [your service], just reply to this text anytime. Have a great week!"

**Step 6: End or move to nurture**
1. Add tag: "follow-up-complete"
2. Optionally move to a monthly newsletter list

### What This Replaces

| Before | After |
|--------|-------|
| Manually checking for new leads | Automatic instant notification |
| Remembering to follow up | Automatic timed follow-ups |
| Copying and pasting the same texts | Pre-written messages sent automatically |
| Losing leads while you're busy/sleeping | 24/7 response, no matter what |

**Time saved:** 4-6 hours per week for most businesses.

---

## Lesson 2: The Appointment Reminder System

No-shows and last-minute cancellations cost local businesses thousands per month. The average no-show rate for service businesses is 20-30%.

An automated reminder system drops that to under 5%.

### Building Your Reminder Sequence

**Step 1: Create the workflow**
1. Go to Automation → Workflows → Create New
2. Name it "Appointment Reminders"
3. Trigger: "Appointment booked"

**Step 2: Confirmation (immediate)**
1. Send SMS: "You're all set, {first_name}! Your appointment with [Business Name] is confirmed for {appointment_date} at {appointment_time}. Reply CONFIRM to keep your spot or RESCHEDULE if you need to change it. See you then!"

**Step 3: Reminder 1 (48 hours before)**
1. Wait until 48 hours before appointment
2. Send SMS: "Reminder: You have an appointment with [Business Name] tomorrow at {appointment_time}. We're looking forward to seeing you! Reply CANCEL if you need to reschedule."

**Step 4: Reminder 2 (2 hours before)**
1. Wait until 2 hours before appointment
2. Send SMS: "See you in 2 hours, {first_name}! Our address is [address]. If you need to reach us, call [phone]."

**Step 5: Post-appointment follow-up (1 hour after)**
1. Wait until 1 hour after appointment end time
2. Send SMS: "Thanks for coming in today, {first_name}! We hope everything went great. If you have any questions, don't hesitate to reach out."
3. Wait 1 hour
4. Trigger review request (see Lesson 3)

### Pro Tips

- **Allow easy cancellation.** "Reply CANCEL" seems like it would increase cancellations, but it actually reduces no-shows. People who would have ghosted you instead cancel, which opens that slot for someone else.
- **Include the address.** People forget where you are. Sounds obvious, but a surprising number of no-shows are because people couldn't find the location.
- **Personalize when possible.** If you know what service they're booked for, include it: "Your [deep cleaning] appointment is tomorrow."

---

## Lesson 3: The Review Collection Machine

Reviews are the currency of local business. Here's how to automate collecting them.

### Why This Matters

| Google Reviews | Impact |
|----------------|--------|
| 0-10 reviews | Blending in with competitors |
| 25-50 reviews | Starting to stand out |
| 50-100 reviews | Noticeably more trusted |
| 100+ reviews | Dominating your local market |

Most happy customers will leave a review if you ask. Most businesses never ask.

### Building Your Review Request Automation

**Step 1: Create the workflow**
1. Go to Automation → Workflows → Create New
2. Name it "Review Request"
3. Trigger: "Tag added" → tag: "job-complete" (or whatever you use to mark finished work)

**Step 2: Immediate thank you**
1. Send SMS: "Thank you for choosing [Business Name], {first_name}! It was a pleasure working with you. If you have 30 seconds, would you mind leaving us a quick review? It really helps us out: {review_link}"

**Step 3: Gentle reminder (3 days later, if no review left)**
1. Wait → 3 days
2. Check: Has left review? (You'll need to track this manually or use GHL's reputation tool)
3. If no review: Send SMS
4. Message: "Hi {first_name}, hope you're doing well! If you have a moment, a quick review would mean the world to us: {review_link}. Thank you!"

**Step 4: Stop. Don't ask a third time.**
Two asks is enough. Pestering someone for a review can turn a happy customer into an annoyed one.

### The Review Link

Make it as easy as possible. Your Google review link should take them directly to the review form — no searching required.

To get your link:
1. Go to your Google Business Profile
2. Click "Ask for reviews"
3. Copy the short link
4. That's your `{review_link}` in the automation

### Handling Bad Reviews

The automation only requests reviews from happy customers (after completed jobs). But what if someone leaves a negative review anyway?

1. Respond within 24 hours
2. Be professional and empathetic
3. Take the conversation offline: "We're sorry about your experience. Please call us at [phone] so we can make this right."
4. Never argue publicly

**Template for negative review response:**
> "Hi [Name], thank you for your feedback. We're sorry to hear your experience didn't meet expectations. We'd love the chance to make it right — please reach out to us at [phone/email] so we can discuss this directly. We appreciate your honesty and hope to resolve this for you."

---

## Lesson 4: Social Media on Autopilot

This isn't about setting it and forgetting it. It's about batching your content so you spend 2 hours per month instead of 2 hours per day.

### The Monthly Content Batch

Once per month, sit down and create 30 days of content. Here's how:

**Step 1: Choose your themes**

| Week | Theme | Example Posts |
|------|-------|--------------|
| Week 1 | Educational | Tips, how-tos, myth-busting |
| Week 2 | Behind the scenes | Your team, your process, day in the life |
| Week 3 | Social proof | Reviews, before/after, customer stories |
| Week 4 | Promotional | Offers, seasonal services, calls to action |

**Step 2: Generate with AI**

Open ChatGPT and use this prompt:

> "I run a [type of business] in [city]. My target customers are [describe them]. I need 30 days of social media content for Facebook and Instagram. Use this weekly theme structure: Week 1 - Educational tips, Week 2 - Behind the scenes, Week 3 - Customer stories and reviews, Week 4 - Promotions. Give me the post text, suggested image/visual idea, and best posting time for each day."

Edit the output to sound like you. Add your personality, your specific examples, your local references.

**Step 3: Create visuals in Canva**

Take each post's image idea and create it in Canva. Use your brand colors and fonts consistently. Save all graphics in a folder labeled by week.

**Step 4: Schedule everything**

Go back into GoHighLevel's Social Planner (or use your AI Plug account):
1. Upload all graphics
2. Copy/paste each post's text
3. Schedule for the recommended times
4. Hit save

You now have 30 days of content scheduled in about 2 hours. Check in occasionally to respond to comments, but the posting itself is handled.

### Content Ideas That Actually Work for Local Businesses

Not sure what to post? Here are proven formats:

| Content Type | Why It Works | Example |
|-------------|-------------|---------|
| Before/After | Visual proof of your work | Photo of a dirty carpet → clean carpet |
| Quick Tips | People share helpful content | "3 signs your AC needs servicing before summer" |
| Customer Spotlight | Makes customers feel valued | Photo + quote from a happy customer |
| Myth Busting | Gets engagement and shows expertise | "No, you don't need to replace your water heater every 10 years — here's why" |
| Day in the Life | Builds personal connection | Short video of your morning routine or a typical job |
| Local Pride | Shows you're part of the community | Photos at local landmarks, supporting local events |
| FAQ Answers | Positions you as the expert | "We get this question all the time: [common question]. Here's the answer." |

---

## Lesson 5: Putting It All Together

Here's what a fully automated week looks like:

### Monday Morning
- You wake up to 3 new leads from the weekend
- All 3 already received an instant text response and booking link on Saturday/Sunday
- 1 has already booked an appointment
- You have a notification about who needs your personal follow-up

### During the Week
- Appointment reminders go out automatically — no-shows are rare
- Completed jobs trigger review requests automatically
- Social media posts go out on schedule — you didn't have to think about it
- New leads get the full follow-up sequence without you touching anything

### Friday Evening
- You get a notification: "5 new Google reviews this week"
- Your calendar for next week is full from automated booking
- You spent your time on actual work, not chasing leads or posting content

**Total time spent on "marketing and admin":** 3-5 hours instead of 15-20.

---

## Module 3 Action Items

- [ ] **Build your Lead Response automation** — Follow the steps in Lesson 1
- [ ] **Set up Appointment Reminders** — At minimum, do the 48-hour and 2-hour reminders
- **Create your Review Request workflow** — Get your Google review link and build the automation
- [ ] **Batch your first month of social content** — Use the ChatGPT prompt + Canva + scheduling
- [ ] **Post your first automation win in the community** — We want to see it working!

---

## Quick Reference

**Key Takeaway:** Automate four things and you'll reclaim 10-15 hours per week: (1) instant lead response, (2) appointment reminders, (3) review requests, (4) social media scheduling. All four can be set up in a single afternoon using GoHighLevel.

**What's Next:** Module 4 — Growing Your Online Presence. We'll cover SEO basics, Google Business Profile optimization, and how to show up when local customers search for what you offer.
