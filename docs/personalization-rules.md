# Personalization Rules - Velocity Motors

This file outlines the personalization logic used accross the Velocity Motors journey emails, inspired by AMPscript practices in Salesforce Marketing Cloud (SFMC).

---

## Global Personalization Variables 

```ampscript
%%[
    SET @FirstName = [FirstName]
    SET @VehicleInterest = [VehicleInterest]
    SET @ZipCode = [ZipCode]
    SET @PreferredDealer = [PreferredDealer]
    SET @OfferTier = [OfferTier]
]%%
```

These values are pulled from the CarConfigurator_Leads Data Extension and used throughout the journey to tailor content.

---

## Welcome Email (welcome.html)

### Subject Line:
```ampscript
%%[
   %%=Concat("Thanks for building your dream ", @VehicleInterest, ", ", ProperCase(@FirstName), "!")=%%
]%%
```

### Headline: 
<h1>Welcome, %%=ProperCase(@FirstName)-%%!</h1>

### Dynamic CTA Button Text:

```ampscript
%%[
    IF @VehicleInterest == "Vanguard ST" THEN
        SET @CTA = "Book Your Vanguard Test Drive"
    ELSEIF @VehicleInterest == "Atlas Range" THEN
        SET @CTA = "Explore SUV Specials"
    ELSE
        SET @CTA = "Schedule Your Test Drive"
    ENDIF
]%%
```

<a href="%%=RedirectTo(@CTA_URL)=%%" class="cta-button">%%-v(@CTA)=%%</a>