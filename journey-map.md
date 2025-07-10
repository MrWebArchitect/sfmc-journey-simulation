# Velocity Motors - Customer Journey Simulation 

**Objective:** Convert online car configuatior users into test drives using automated, behovior-based email sequences.

---

## Entry Source 

**Date Extension:** `CarConfigurator_Leads`

Triggered when a customer completes a vehicle configuration but doesn't book a test drive.

Fields: 
- `FirstName`
- `Email`
- `VehicleInterest`
- `Zipcode`
- `PreferredDealer`
- `LeadSource` (e.g. Web, Mobile App)

---

## Journey Steps

### Step 1: Welcome / Thank You Email
- **Send Email:** `welcome.html`
- Personalized subject line: 
    > 'Thanks for building your dream [VehicleInterest], [FirstName]!'
- Content: Confirm submission, showcase key features of configured vehicle
- CTA: "Schedule a test Drive"

### Step 2: Wait 2 Days

---

### Step 3: Decision Split - Has Booked Test Drive?

**Yes →** Exit Journey
**No →** Continue

---

### Step 4: Onboarding Email
- **Send Email:** `onboarding.html`
- Highlights: Dealer location, top reviews, financing options
- CTA: "See Your Dealer Offers"

---

### Step 5: Wait 3 Days

---

### Step 6: Decision Split - Has Opened Previous Email?

**Yes →** Send Promo Offer  
**No →** Send Re-engagement Email

---

### Step 7a: Promo Offer Email
- **Send Email:** `promo-offer.html`
- Offer: $250 bonus toward down payment or accessory package
- CTA: "Claim Your Exclusive Offer"

---

### Step 7b: Re-engagement Email
- **Send Email:** `re-engagement.html`
- Subject: "Still thinking it over, [FirstName]?"
- CTA: "Revisit Your [VehicleInterest]"

---

### Exit Criteria: 
- Customer schedules test drive
- 10 days pass with no engagement
- Unsubscribes

---

## Notes: 

- Wait steps allow for natural timing without overwhelming the user
- Personalization is driven by AMPscirpt-style logic (see `personalization-rules.md`)
- Dynamic content used for vehicle model, dealer info and offer tier
