# TrueFit

## What and why?

I want to build **TrueFit**, a mobile web app that lets people preview how an item of clothing will actually fit them before they buy it online.

Online clothing shopping has a trust problem. Sizing is inconsistent across brands, product photos are shot on models who look nothing like the buyer, and the only way to really know if something fits is to order it, wait for it, try it on, and often send it back. Return rates for online apparel are consistently among the highest of any retail category, and every one of those returns costs the buyer time, costs the seller money, and adds unnecessary shipping and packaging waste. The person doing the buying ends up absorbing all the risk.

TrueFit shifts that risk earlier. A user enters their measurements once (and optionally a photo), and from then on, every item they look at shows a fit preview and a per-brand size recommendation before they ever add it to a cart. The goal isn't to replace the checkout experience people already know, it's to remove the guesswork that sits in front of it.

## For whom?

The initial users are people I know personally: friends and family who shop for clothing online regularly and have told me directly that fit uncertainty is their biggest frustration with it. Several of them routinely order the same item in two or three sizes just to see which one fits, then return the rest. Others have given up on certain brands entirely because they got burned by inconsistent sizing once. These are real people I can talk to throughout the semester to test whether TrueFit's fit predictions and recommendations actually match their experience, and to refine the design based on what they find confusing or untrustworthy.

## How?

From a user's perspective, TrueFit works like this:

1. **Profile setup**: A new user enters their body measurements (height, weight, and a few key measurements like chest/bust, waist, and hips) and optionally uploads a reference photo. This is a one-time setup, not something repeated per purchase.
2. **Browse the catalog**: Users browse clothing items much like any shopping app, with photos, descriptions, and pricing.
3. **Fit preview**: On each product page, TrueFit shows a fit preview, a visual estimate of how the garment will sit on the user's body shape, along with a clear recommendation like "Order a size Medium in this brand, it tends to run small."
4. **Size confidence indicator**: Alongside the preview, users see a simple confidence rating (e.g. "high confidence" vs "size varies, check measurements") so they know when to trust the recommendation and when to double check.
5. **Checkout**: Users select their recommended (or preferred) size and complete checkout within the app.
6. **Feedback loop**: After a purchase, users can quickly confirm whether the item actually fit as predicted. This feedback improves future recommendations for that user and that brand.

The end result is that a user should be able to look at any item in the catalog and walk away knowing, with real confidence, whether it will fit, instead of finding out two weeks later when the package arrives.

## Scope

This project is scoped to be achievable by a team of 4 to 6 programmers in one semester by deliberately avoiding the hardest version of the problem. TrueFit does not attempt full 3D body scanning or photorealistic AR try-on, which would require specialized computer vision expertise and hardware access well beyond a semester timeline. Instead, it uses a measurement-based matching model (comparing user measurements against a brand's size chart and garment dimensions) combined with a simplified visual overlay, which is realistic to implement with standard mobile web technologies in the given time.

At the same time, this is not a trivial CRUD app. It requires a real data model for garments and size charts across multiple brands, a recommendation algorithm that improves from user feedback, a believable fit-visualization component, and a full browse-to-checkout shopping flow. That combination of a genuine e-commerce experience plus a meaningful data-driven feature gives a team of this size real, distinct pieces of work to divide and enough depth to iterate on throughout the semester.
