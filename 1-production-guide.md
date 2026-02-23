# Lifestyle Layer — Production Guide

## Setup

### What You Need
- Adobe Photoshop (latest version with Partner Models enabled)
- Nano Banana Pro (Gemini) selected as your Generative Fill model
- Your property photos (high-res, well-lit, empty or minimally staged)

### How to Enable Nano Banana Pro in Photoshop
1. Update to Photoshop 2026 (v27.0+) via Creative Cloud
2. Open an image, make a selection, click Generative Fill
3. Click the model picker icon (shows "Fi" or "G") next to the prompt field
4. Select "Gemini 2.5 (Nano Banana)" or "Gemini 3 (Nano Banana Pro)"

---

## CRITICAL RULE: Preserve the Original Scene

**The AI must ONLY add people. It must NOT add, remove, or change any furniture, fixtures, decor, or architectural elements in the photo.**

This is controlled by two things: your SELECTION and your PROMPT.

---

## Production Workflow (Per Image)

### Step 1: Prep the Photo
- Open the property photo in Photoshop
- Assess: Where would a person naturally be in this space? (Standing by a window, sitting at a counter, walking through a lobby)
- Assess: What direction is the light coming from? (This is critical for matching)
- Assess: What time of day does the photo feel like? (Morning, afternoon, golden hour, evening)

### Step 2: Select the Area — THIS IS THE MOST IMPORTANT STEP

**The selection controls what the AI can change. Anything OUTSIDE your selection stays untouched.**

- **ONLY select empty space** where a person would naturally stand or sit
- Use the **Lasso Tool** (L) for precise, organic selections — trace around ONLY the empty floor/air space where the person will be
- **DO NOT select furniture, countertops, fixtures, walls, or any existing objects** — if they're inside your selection, the AI may alter or replace them
- **DO NOT select the entire canvas** (Ctrl/Cmd+A) — this gives the AI permission to change everything
- Include a small amount of floor at the bottom of your selection (the AI needs this to ground the person's feet and cast shadows)
- If someone will be sitting on an existing chair/couch, select ONLY the area above the seat surface — the body shape — not the furniture itself
- Feather the selection 3-5px for natural edge blending (Select → Modify → Feather)

**Selection Examples:**
- Person standing in a kitchen: Select an upright rectangle of empty floor space next to the counter. Do NOT include the counter, cabinets, or appliances in the selection.
- Person sitting on a couch: Select the air space above the couch cushion where the torso/head would be, plus a small overlap onto the cushion edge. Do NOT select the whole couch.
- Person by a pool: Select a section of empty pool deck. Do NOT include loungers, tables, or pool edge features.

**Test your selection:** Before generating, look at the marching ants. If any furniture or fixtures are inside the selection, shrink it. It's better to make the selection too tight (the person might get cropped) than too loose (furniture gets altered). You can always redo with a slightly larger selection.

### Step 3: Generate
- Click Generative Fill in the contextual taskbar
- Switch model to Nano Banana Pro
- Enter prompt (see templates below)
- **IMPORTANT: Your prompt should describe ONLY the person.** Do not describe the room, furniture, or surroundings — the AI will try to generate those too.
- Generate → Review → Generate again if needed (you get 3 variations per generation)
- **After each generation, immediately check:** Did any furniture change? Did anything get added or removed? If yes, Undo (Cmd+Z), tighten your selection, and try again.

### Step 4: Refine
- If needed, mask out any artifacts using a layer mask
- Adjust color/tone with a Curves or Hue/Saturation adjustment layer clipped to the generated layer
- Match the color temperature to the rest of the photo
- Check: Do the shadows match? Is the scale right? Do the hands look normal?

### Step 5: Export
- Flatten or merge layers
- Export as:
  - Landscape: 16:9 (crop accordingly)
  - Square: 1:1
  - Vertical: 9:16
- Save as high-quality JPEG (quality 10-12) or PNG
- File naming: `[PropertyName]_LL_[SceneType]_[Format].jpg`
  - Example: `TheLindley_LL_MorningCoffee_16x9.jpg`

---

## Quality Checklist (Check Every Image Before Delivery)

### FIRST CHECK — Scene Preservation (Check This Before Anything Else)
- [ ] **No furniture was added** that wasn't in the original photo
- [ ] **No furniture was removed** or altered from the original photo
- [ ] **No objects were changed** — countertops, appliances, fixtures, decor all match the original
- [ ] **Architectural elements are intact** — walls, windows, doors, moldings unchanged
- [ ] **Floor/ground texture is consistent** — no weird patches or material changes where the person meets the floor

### SECOND CHECK — Person Quality
- [ ] Hands look natural (correct number of fingers, natural positioning)
- [ ] Feet/shoes connect properly to the floor
- [ ] Shadows fall in the same direction as existing shadows in the photo
- [ ] Scale is correct (people aren't too large or small for the space)
- [ ] Skin tones look natural under the existing lighting
- [ ] Clothing looks realistic (no weird folds or floating fabric)
- [ ] Eyes are natural (no uncanny valley stare)
- [ ] Hair looks realistic (no melting or floating strands)
- [ ] Person doesn't unnaturally overlap or clip through existing furniture
- [ ] Color temperature of the person matches the rest of the image
- [ ] No obvious AI artifacts (extra limbs, duplicated objects)
- [ ] The pose looks candid, not stiff or stock-photo-ish

**If the scene was altered in ANY way, reject the generation. Undo, tighten your selection, and regenerate.**

---

## Prompt Templates — Multifamily Spaces

Organized around the 4 spaces you shoot at every property:
1. **Model Unit** — Living Room, Kitchen, Bedroom
2. **Gym / Fitness Center**
3. **Club Room / Common Area**
4. **Pool Area**

### CRITICAL PROMPTING RULES

1. **Describe ONLY the person** — their body, pose, clothing, expression
2. **DO NOT describe the room, furniture, or surroundings** — the AI will try to generate them and alter what's already there
3. **DO NOT say things like "in a modern kitchen" or "at a dining table"** — the room already exists in the photo
4. **DO include lighting language** — this helps the AI match the person's lighting to the scene without changing the scene itself
5. **DO include camera/lens language** — this keeps the person looking like part of the same photograph
6. **Add the safety phrase** at the end of every prompt (see below)
7. **NEVER describe people sitting or lying on counters, tables, or surfaces** — the AI will put them on top of furniture. Use "standing" or "seated" without naming what they're on.

### Prompt Formula:
```
[Person description] + [pose/action] + [clothing] + [expression] +
[lighting on the person] + [camera style] +
"Do not change the background or surroundings. Do not place
people on top of tables or counters."
```

### Adapt Per Photo:
- **Lighting**: "lit by warm natural light from the left" → match the actual light direction in YOUR photo
- **Clothing tier**: Luxury = linen/designer casual. Multifamily = comfortable modern. Senior = smart casual.

---

## SPACE 1: MODEL UNIT

The model unit is your hero content — living room, kitchen, and bedroom shots that help prospects imagine themselves living in the space.

### Living Room

**LR-1 — Morning Coffee (Solo)**
```
A woman in her late 20s standing and holding a ceramic coffee mug with
both hands, wearing an oversized cream sweater and joggers, relaxed
morning expression, looking slightly to the side. Lit by warm soft
morning light, natural skin tones, 35mm lens, shallow depth of field,
photorealistic. Do not change the background or surroundings. Do not
place people on top of tables or counters.
```

**LR-2 — Morning Coffee (Solo — Male)**
```
A man in his early 30s standing casually holding a coffee mug in one
hand, wearing a heather gray t-shirt and dark joggers, looking down
at his phone with a relaxed expression. Lit by warm morning light,
soft shadows on face, 35mm lens, photorealistic. Do not change the
background or surroundings. Do not place people on top of tables or
counters.
```

**LR-3 — Work From Home (Man)**
```
A man in his mid-30s seated and looking at a laptop screen, wearing a
casual button-down shirt with sleeves rolled up, focused expression,
one hand on keyboard. Lit by natural window light from the side, soft
shadows, 50mm lens, shallow depth of field, photorealistic. Do not
change the background or surroundings. Do not place people on top of
tables or counters.
```

**LR-4 — Work From Home (Woman)**
```
A woman in her early 30s seated with a laptop open in front of her,
wearing a simple blouse, thoughtful expression, one hand on the
trackpad. Natural side light on her face, 35mm lens, photorealistic.
Do not change the background or surroundings. Do not place people on
top of tables or counters.
```

**LR-5 — Couple Relaxing**
```
A couple in their early 30s standing close together, the woman holding
a coffee mug and the man with his arm resting casually, both in casual
morning clothes, smiling at each other. Warm morning light on their
faces, soft shadows, 35mm lens, photorealistic, candid. Do not change
the background or surroundings. Do not place people on top of tables
or counters.
```

**LR-6 — Senior Couple (Senior Housing)**
```
A couple in their late 60s standing together, the woman holding a mug
with both hands and the man holding a folded newspaper, relaxed content
expressions, comfortable smart casual clothing. Warm soft morning light
on their faces, 50mm lens, photorealistic. Do not change the background
or surroundings. Do not place people on top of tables or counters.
```

**LR-7 — Senior with Tablet (Senior Housing)**
```
A man in his early 70s seated comfortably holding a tablet, wearing a
light collared shirt and reading glasses, relaxed focused expression.
Warm natural light on his face, 50mm lens, photorealistic, warm tones.
Do not change the background or surroundings. Do not place people on
top of tables or counters.
```

---

### Kitchen

**K-1 — Morning Routine (Solo)**
```
A woman in her late 20s standing and holding a coffee mug in one hand,
wearing a casual t-shirt and shorts, relaxed morning expression,
leaning slightly. Warm soft morning light on her face, 35mm lens,
photorealistic. Do not change the background or surroundings. Do not
place people on top of tables or counters.
```

**K-2 — Couple Cooking**
```
A couple in their mid-30s standing together, the man holding a cutting
board and the woman holding a wooden spoon, casual comfortable clothing,
laughing together. Warm light on faces, 35mm lens, photorealistic,
candid. Do not change the background or surroundings. Do not place
people on top of tables or counters.
```

**K-3 — Family Meal Prep**
```
A parent in their late 30s standing with a child around age 10, the
parent holding a mixing bowl and the child watching with an excited
expression, casual comfortable clothing. Warm overhead light on them,
35mm lens, photorealistic, candid. Do not change the background or
surroundings. Do not place people on top of tables or counters.
```

---

### Bedroom

**BR-1 — Morning Light (Solo)**
```
A woman in her early 30s standing near the window stretching with arms
raised, wearing a soft oversized t-shirt, peaceful morning expression,
backlit silhouette. Warm golden morning light on her outline, 50mm
lens, shallow depth of field, photorealistic. Do not change the
background or surroundings. Do not place people on top of tables or
counters.
```

**BR-2 — Reading / Relaxing**
```
A man in his early 30s seated in a relaxed position holding an open
book, wearing a casual henley shirt and sweats, content focused
expression. Warm soft light on his face, 50mm lens, photorealistic.
Do not change the background or surroundings. Do not place people on
top of tables or counters.
```

**BR-3 — Couple Morning**
```
A couple in their early 30s, the woman standing and stretching while
the man holds a coffee mug, both in comfortable sleepwear, relaxed
happy expressions, morning energy. Warm soft morning light on them,
35mm lens, photorealistic, candid. Do not change the background or
surroundings. Do not place people on top of tables or counters.
```

---

## SPACE 2: GYM / FITNESS CENTER

Fitness amenities are a top-3 decision factor for multifamily renters. These prompts bring the gym to life.

**GYM-1 — Cardio Together (2 people)**
```
Two people in their early 30s, a man and a woman, both mid-stride in
active cardio poses, wearing athletic wear, focused energized
expressions. Bright even lighting on their bodies, 35mm lens,
photorealistic. Do not change the background or surroundings. Do not
place people on top of tables or counters.
```

**GYM-2 — Weight Training (2-3 people)**
```
Three people in their mid-30s, two men and one woman, in various
weight-lifting poses holding dumbbells, wearing fitted athletic shirts
and shorts, focused determined expressions. Bright even lighting on
their bodies, 35mm lens, photorealistic. Do not change the background
or surroundings. Do not place people on top of tables or counters.
```

**GYM-3 — Yoga / Stretching (2-3 people)**
```
Two women in their late 20s in standing yoga poses, wearing athletic
leggings and tank tops, calm centered expressions, balanced postures,
side by side. Soft natural light on their bodies, 50mm lens,
photorealistic. Do not change the background or surroundings. Do not
place people on top of tables or counters.
```

**GYM-4 — Group Fitness Class (4-6 people)**
```
A group of five people in their 20s-30s in active exercise poses, mixed
genders, wearing athletic wear, focused expressions, mid-movement in
unison. Bright even lighting on their bodies, 35mm lens, photorealistic.
Do not change the background or surroundings. Do not place people on
top of tables or counters.
```

**GYM-5 — Active Seniors (2 people, Senior Housing)**
```
Two seniors in their late 60s, a man and a woman, in active walking
strides side by side, wearing comfortable athletic clothing, relaxed
steady expressions. Bright even lighting on their bodies, 35mm lens,
photorealistic. Do not change the background or surroundings. Do not
place people on top of tables or counters.
```

---

## SPACE 3: CLUB ROOM / COMMON AREA

The club room is where community happens. These prompts show the space as a social hub — coworking, game nights, resident events, and casual hangouts.

**CR-1 — Coworking**
```
Two people in their late 20s seated near each other, one with a laptop
and the other looking at a tablet, smart casual clothing, focused but
relaxed expressions, natural posture. Warm ambient light on their faces,
50mm lens, photorealistic. Do not change the background or surroundings.
Do not place people on top of tables or counters.
```

**CR-2 — Friends Hanging Out**
```
A group of three friends in their early 30s, two seated and one
standing, holding drinks, casual modern clothing, mid-conversation with
natural laughter. Warm evening lighting on their faces, 35mm lens,
photorealistic, candid. Do not change the background or surroundings.
Do not place people on top of tables or counters.
```

**CR-3 — Game Night**
```
Four residents in their 30s-40s gathered together, two men and two
women, playing a board game, casual comfortable clothing, engaged
competitive expressions, one person pointing at the game. Warm overhead
light on them, 35mm lens, photorealistic, candid and fun. Do not change
the background or surroundings. Do not place people on top of tables
or counters.
```

**CR-4 — Social Event / Wine Night**
```
A small group of four people in their 30s-40s, two standing and two
seated, holding cocktail glasses, smart casual evening attire, natural
laughter and conversation. Warm ambient lighting on their faces, 50mm
lens, photorealistic. Do not change the background or surroundings.
Do not place people on top of tables or counters.
```

**CR-5 — Solo Reading**
```
A woman in her early 40s seated in a comfortable position reading a
book, wearing a casual sweater and jeans, relaxed content expression,
legs tucked to one side. Warm soft light on her, 50mm lens, shallow
depth of field, photorealistic. Do not change the background or
surroundings. Do not place people on top of tables or counters.
```

**CR-6 — Video Call / Remote Work**
```
A woman in her mid-30s seated with a laptop, wearing a professional
blouse, engaged expression, one hand gesturing as if on a video call.
Bright even lighting on her face, 50mm lens, photorealistic. Do not
change the background or surroundings. Do not place people on top of
tables or counters.
```

**CR-7 — Resident Event (6-8 people)**
```
A group of seven residents in their 20s-40s, some standing and some
seated, holding drinks and small plates, mix of casual and smart casual
clothing, animated conversations in small clusters, natural body
language. Warm ambient lighting on their faces, 35mm lens,
photorealistic, editorial lifestyle. Do not change the background or
surroundings. Do not place people on top of tables or counters.
```

**CR-8 — Movie / Watch Party (5-6 people)**
```
A group of five residents in their 20s-30s seated together, some
holding drinks and snacks, casual comfortable clothing, relaxed engaged
expressions, looking in the same direction. Warm low ambient light on
their faces, 35mm lens, photorealistic, candid. Do not change the
background or surroundings. Do not place people on top of tables or
counters.
```

**CR-9 — Senior Social (Senior Housing)**
```
A group of three seniors in their 60s-70s seated together, one woman
and two men, holding coffee cups, smart casual clothing, warm
conversation and smiling. Soft warm light on their faces, 50mm lens,
photorealistic, welcoming and natural. Do not change the background
or surroundings. Do not place people on top of tables or counters.
```

**CR-10 — Senior Card Game (Senior Housing)**
```
A group of four seniors in their 60s-70s seated together, two men and
two women, holding playing cards, casual comfortable clothing, engaged
and smiling. Warm light on their faces, 35mm lens, photorealistic. Do
not change the background or surroundings. Do not place people on top
of tables or counters.
```

---

## SPACE 4: POOL AREA

Pool and outdoor amenity shots sell the lifestyle more than any other space. These prompts bring the pool deck to life.

**POOL-1 — Solo Lounging**
```
A woman in her late 20s in a relaxed reclining pose, wearing a light
swimsuit coverup and sunglasses on her head, holding a magazine. Bright
afternoon sunlight on skin, warm golden tones, defined shadows, 35mm
lens, photorealistic. Do not change the background or surroundings.
Do not place people on top of tables or counters.
```

**POOL-2 — Couple Poolside**
```
A couple in their early 30s, the woman seated with feet dangling and
the man standing nearby holding two drinks, casual swimwear, relaxed
happy expressions. Bright afternoon sunlight on skin, warm tones, 35mm
lens, photorealistic. Do not change the background or surroundings.
Do not place people on top of tables or counters.
```

**POOL-3 — Friends Group**
```
Three friends in their late 20s, one standing and two seated, casual
summer clothing, holding drinks, natural laughter. Bright sunlight on
skin, warm golden tones, soft shadows, 35mm lens, photorealistic. Do
not change the background or surroundings. Do not place people on top
of tables or counters.
```

**POOL-4 — Solo Relaxing (Male)**
```
A man in his early 30s in a relaxed seated pose, wearing swim trunks
and an open button-down shirt, sunglasses on, holding a drink, looking
off to the side. Bright afternoon sunlight on skin, warm golden tones,
35mm lens, photorealistic. Do not change the background or surroundings.
Do not place people on top of tables or counters.
```

**POOL-5 — Pool Party (6-8 people)**
```
A group of six friends in their late 20s to early 30s, some standing
and some seated, casual summer clothing and swimwear, holding drinks,
animated conversation and laughter in small clusters. Bright afternoon
sunlight on skin, warm golden tones, 35mm lens, photorealistic,
editorial lifestyle. Do not change the background or surroundings. Do
not place people on top of tables or counters.
```

**POOL-6 — Golden Hour Couple**
```
A couple in their early 30s seated close together, the woman leaning
into the man, both holding drinks, casual summer clothing, relaxed
happy expressions. Warm golden hour light on their faces and skin,
85mm lens, shallow depth of field, photorealistic. Do not change the
background or surroundings. Do not place people on top of tables or
counters.
```

---

## EHO Diversity Variants

For every scene, generate at minimum 3 demographic variants. Use these modifier swaps in your prompts:

### Age Swaps
- "in her late 20s" → "in her early 40s" → "in her late 60s"
- "in his mid-30s" → "in his early 50s" → "in his early 70s"

### Gender Swaps
- "A woman" → "A man"
- "A couple" → "Two women" / "Two men"
- "the woman... the man" → swap roles

### Family Structure Swaps
- "parents with two children" → "a single parent with a child"
- "A couple" → "A multigenerational family"
- "friends" → vary the mix

### Important Notes
- Do NOT specify race or ethnicity in prompts — generate multiple batches and curate diverse results naturally
- If results skew toward one demographic, re-generate until you have a diverse set
- For each property delivery, ensure the final image set includes visible diversity across the images
- Aim for representation across: age, gender, family structure, and ethnicity

---

## Batch Production Plan (For Building Your Portfolio)

### Pick 5 Past Multifamily Properties. For Each:
1. Select your best photos across the 4 spaces (model unit, gym, club room, pool)
2. Apply 2-3 prompts per photo from the matching space section above
3. Generate 2 demographic variants per scene
4. QA and cull to your best 40-50 for the portfolio

### Suggested Photo Mix Per Property:
- 2 living room shots
- 1 kitchen shot
- 1 bedroom shot
- 1 gym shot
- 1 club room / common area shot
- 1 pool area shot

### Time Estimate:
- ~10-15 minutes per final image (including generation iterations and QA)
- Total portfolio build: ~10-15 hours of focused work
- Spread over 2 weeks = very manageable

---

## Troubleshooting: AI Changed the Furniture/Scene

If the AI keeps altering the background despite a tight selection:

1. **Make the selection smaller** — you're probably including too much of the scene
2. **Add "do not add or change any furniture, objects, or surroundings" to the end of your prompt**
3. **Try a simpler prompt** — sometimes shorter is better. Just "A woman in her 30s standing, casual clothing, photorealistic" can work
4. **Use the generated layer mask** — after generation, use a soft brush on the layer mask to paint back any original elements that got changed
5. **Try a different model** — if Nano Banana keeps altering the scene, try Flux Kontext which tends to preserve backgrounds better
6. **Generate multiple times** — sometimes 1 of 3 variations preserves the scene while the others don't. Pick the clean one.
