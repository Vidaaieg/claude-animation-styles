# 🎬 10 ستايلات أنيميشن بـ Claude عشان الريل بتاعك يكسر الدنيا

<p align="center">
  <a href="#prompt"><img src="https://img.shields.io/badge/%E2%9A%A1%20GET%20THE%20PROMPT-COPY%20%26%20PASTE-F97316?style=for-the-badge" alt="خد الـ Prompt على طول" height="44"></a>
  <a href="#fill"><img src="https://img.shields.io/badge/%F0%9F%93%9D%20FILL%20YOUR%20DETAILS-NAME%20%C2%B7%20NICHE%20%C2%B7%20TEXT-2563EB?style=for-the-badge" alt="املا بياناتك" height="44"></a>
</p>

<p align="center"><b>👆 دوس على الزرار البرتقاني وهتروح للـ Prompt على طول — املا الخانات والصقه في Claude.</b></p>

عايز تعمل أنيميشن شكله غالي ومش عارف After Effects؟
Claude Code بيكتب كود الأنيميشن بنفسه، و Remotion بيطلّعه فيديو MP4 جاهز للريلز.

هنا هتلاقي **الـ Prompts العشرة**، نفس الستايلات اللي في الريل، وكل واحد معاه شرح بيعمل إيه وامتى تستخدمه.

> 💡 انسخ الـ Prompt زي ما هو، وغيّر بس الحاجات اللي بين `[ ]`.

> ⚠️ كل Prompt هيديك نتيجة قريبة من الستايل، مش نفس الفيديو بالظبط. عادي تحتاج مرة أو اتنين تقوله "صلّح كذا".

---

## 🔌 الأول: جهّز الأدوات

1. نزّل Node.js و Google Chrome على جهازك.
2. نزّل Claude Code وسجّل دخول بحسابك.
3. اعمل فولدر فاضي، وافتح Claude Code جواه، والصق الـ Prompt.

شرح Claude Code الرسمي: https://support.claude.com
شرح Remotion الرسمي: https://www.remotion.dev/docs

---

<a id="fill"></a>

## 📝 املا بياناتك الأول (مرة واحدة بس)

كل الـ Prompts تحت بتستخدم نفس الخانات دي، فاملاها مرة واحدة واستخدمها في كله.

| الخانة | تكتب فيها إيه | مثال |
|---|---|---|
| `[YOUR NAME]` | اسمك أو الـ handle بتاعك | `@steventawfik` |
| `[CONTENT TYPE]` | نوع المحتوى أو البيزنس بتاعك | `AI automation` |
| `[AUDIENCE]` | بتكلم مين | `Egyptian small business owners` |
| `[LANGUAGE]` | لغة الكلام اللي على الشاشة | `Egyptian Arabic` |
| `[SUBJECT]` | بطل الفيديو، حاجة واحدة بس | `a red Egyptian tuk-tuk with a yellow stripe` |
| `[ACTION]` | الحاجة المفاجئة اللي بتحصل | `fires thrusters under its wheels and flies up` |
| `[PLACE]` | المكان | `a street in Cairo at sunset, with a minaret behind` |
| `[CAPTION]` | كلمة أو جملة قصيرة في الآخر | `طار!` |

<a id="prompt"></a>

### ⚡ Prompt واحد شامل — املا والصق

املا الخانات والصق ده، وهيعملك الـ 10 ستايلات في مشروع واحد.

```text
Here are my details:
- Name: [YOUR NAME]
- Content type: [CONTENT TYPE]
- Audience: [AUDIENCE]
- On-screen language: [LANGUAGE]
- Subject: [SUBJECT]
- Action: [ACTION]
- Place: [PLACE]
- Final caption: [CAPTION]

Build a Remotion project in this folder that shows the same 5-second story in 10 different animation styles. Plan first, then build one style at a time and check each one before moving on.

STORY (identical in every style):
- Frames 0-30: [SUBJECT] is still in [PLACE]. A small crowd watches from the bottom of the frame.
- Frames 30-70: build-up to the action. Small movement, smoke or light starting.
- Frames 70-125: [ACTION]. The crowd raises its arms.
- Frames 125-150: the subject holds with a gentle float, and "[CAPTION]" appears.
Keep the subject, crowd and framing in the same positions across all styles.

TECHNICAL RULES:
- Each style is its own composition: 1080x1920, 30 fps, exactly 150 frames.
- Every animated value must come from useCurrentFrame(). Use a seeded random function only.
- Motion must be smooth: ease in and out, change position on every frame, never hold a pose for several frames, and avoid fast per-frame jitter.
- If [LANGUAGE] uses Arabic script, load an Arabic font and set direction to rtl.
- For 3D styles use three.js directly: create the WebGLRenderer once with preserveDrawingBuffer true, and call render inside useLayoutEffect for each frame. Render them with --gl=angle.
- Never use a real company's name, logo or character.

THE 10 STYLES:
1. Pixel Art: low-resolution canvas scaled up with no smoothing, limited palette, ordered dithering for gradients, retro game HUD.
2. Chalkboard: green board with a wooden frame, chalk-textured lines that draw themselves.
3. Glow Sketch: near-black background, glowing dotted outlines, warm light beams.
4. PS2: early-2000s console 3D, low-poly, blurry low-resolution render, fog.
5. Collage: flat paper colour, halftone cut-outs with white paper edges that slide in and lock.
6. Handwritten: blue ballpoint on lined notebook paper, drawn stroke by stroke with a moving pen.
7. Minimal Line: pure black, thin white lines, one tiny stick figure.
8. CGI: dark realistic 3D, reflective paint, fog, glowing ring on the ground.
9. Bricks: toy-brick world with studs, glossy plastic, smoke made of white bricks.
10. Clay 3D: matte rounded 3D shapes, pastel background, soft shadows.

Then make one extra composition called Montage for my [CONTENT TYPE] page aimed at [AUDIENCE]: each style plays for about 1 second, a numbered list of the style names fills up beside it, and [YOUR NAME] sits at the bottom.

Before the final render, export stills at frames 30, 90 and 140 of each style, look at them, and fix anything clipped, overlapping or unreadable. Render everything to the out folder as MP4.
```

**بيعمل إيه؟** بيبني الـ 10 ستايلات بنفس القصة، وبعدين يجمعهم في ريل واحد فيه قايمة بتتملي. ده أكبر Prompt، فهياخد وقت ومن حدود اشتراكك.

---

## 💬 الـ Prompts خطوة بخطوة

كل Prompt من دول شغال لوحده. ابدأ بواحد، وشوف النتيجة، وبعدين كمّل.

## 👾 1. Pixel Art

لو عايز شكل لعبة قديمة يوقف الـ scroll.

```text
Build one Remotion composition in this folder (create the project if there is none): 1080x1920, 30 fps, exactly 150 frames, on-screen language [LANGUAGE].

Story: frames 0-30 [SUBJECT] is still in [PLACE] with a small crowd at the bottom. Frames 30-70 build-up. Frames 70-125 [ACTION] and the crowd raises its arms. Frames 125-150 the subject floats gently.

Rules: every value comes from useCurrentFrame(), seeded randomness only, smooth eased motion, no real brand names or logos.

Style: 16-bit pixel art.
- Draw everything on a 135x240 canvas and scale it up with image-rendering: pixelated.
- About 32 colours. Make sky gradients with 4x4 Bayer ordered dithering, never smooth blends.
- Build the subject from filled rectangles, about 50 pixels wide, with a dark outline.
- Add a retro game HUD: a small hand-made bitmap font, a height counter and three hearts.
- Put the moving subject on its own canvas layer and move that layer with a CSS transform, so its movement stays smooth instead of stepping.
- End with [CAPTION] on a game-style banner. If the font can't draw it, use a separate text layer.

Export stills at frames 30, 90 and 140, fix any problems, then render out/pixel-art.mp4.
```

**بيعمل إيه؟** بيرسم كل حاجة على صورة صغيرة جدًا ويكبّرها، فتطلع بكسلات حقيقية مش فلتر.
**نصيحة:** لو الحركة بتقطّع، قوله يتأكد إن البطل على layer لوحده.

---

## 🧑‍🏫 2. Chalkboard

لو بتشرح فكرة وعايزها تبان زي درس.

```text
Build one Remotion composition in this folder (create the project if there is none): 1080x1920, 30 fps, exactly 150 frames, on-screen language [LANGUAGE].

Story: frames 0-30 [SUBJECT] is still in [PLACE]. Frames 30-70 build-up. Frames 70-125 [ACTION]. Frames 125-150 the subject floats gently and [CAPTION] is written at the bottom.

Rules: every value comes from useCurrentFrame(), seeded randomness only, smooth eased motion, no real brand names or logos.

Style: chalk on a blackboard, built in SVG.
- Dark green board (#23483A) with a thick wooden frame and two chalk sticks in the tray.
- Every outline uses pathLength=1 and animates stroke-dashoffset, so the drawing writes itself in the first 45 frames.
- Chalk texture: an SVG filter combining feTurbulence grain with a slight feDisplacementMap. Keep the filter seed constant so the lines don't flicker.
- Off-white chalk, with yellow for the title underline and labelled arrows.
- A handwritten title at the top about [PLACE]. If [LANGUAGE] uses Arabic script, use the Aref Ruqaa font.

Export stills at frames 30, 90 and 140, fix any problems, then render out/chalkboard.mp4.
```

**بيعمل إيه؟** بيخلي الرسمة تتكتب قدام المشاهد بطباشير ليها ملمس حقيقي.

---

## ✨ 3. Glow Sketch

لو عايز شكل فخم على خلفية سودا.

```text
Build one Remotion composition in this folder (create the project if there is none): 1080x1920, 30 fps, exactly 150 frames, on-screen language [LANGUAGE].

Story: frames 0-30 [SUBJECT] is still in [PLACE]. Frames 30-70 build-up. Frames 70-125 [ACTION] and a figure raises its arms. Frames 125-150 the subject floats gently and [CAPTION] fades in.

Rules: every value comes from useCurrentFrame(), seeded randomness only, smooth eased motion, no real brand names or logos.

Style: glowing dotted sketch, built in SVG.
- Near-black background (#06070C).
- All outlines are round dotted strokes (stroke-linecap round, stroke-dasharray "0.1 5") in warm cream (#FFD9A0).
- Add glow with an SVG filter: feGaussianBlur merged twice under the original line.
- Thin vertical beams of warm light fall under the subject, fading to transparent.
- Two dotted ellipses on the ground spread outward during the action.
- [PLACE] appears very faintly in dim blue dots behind everything.

Export stills at frames 30, 90 and 140, fix any problems, then render out/glow-sketch.mp4.
```

**بيعمل إيه؟** بيرسم البطل بنقط منورة كأنها لمبات، وده بيبان غالي جدًا على الموبايل.

---

## 🎮 4. PS2

لو جمهورك كبر على ألعاب أول الألفينات.

```text
Build one Remotion composition in this folder (create the project if there is none): 1080x1920, 30 fps, exactly 150 frames, on-screen language [LANGUAGE]. Install three and @types/three.

Story: frames 0-30 [SUBJECT] is still in [PLACE] with a small crowd in front. Frames 30-70 build-up. Frames 70-125 [ACTION] and the crowd raises its arms. Frames 125-150 the subject floats gently and [CAPTION] appears.

Rules: every value comes from useCurrentFrame(), seeded randomness only, smooth eased motion, no real game names, characters, brands or logos.

3D setup: use three.js directly. Create the WebGLRenderer once with preserveDrawingBuffer true, update objects from the frame number, and call render inside useLayoutEffect. Render with --gl=angle.

Style: early-2000s console 3D.
- Low-poly models, flat shading, MeshLambertMaterial.
- Render at about 0.42 pixel ratio with antialiasing off, then let the browser stretch it so the picture is soft and blocky.
- A tiny 32x32 noise texture on models, using nearest filtering.
- Low-resolution building textures, a gradient sky and heavy distance fog.
- Do not add camera shake.

Export stills at frames 30, 90 and 140, fix any problems, then render out/ps2.mp4.
```

**بيعمل إيه؟** بيعمل 3D حقيقي بس بيرندره بجودة قليلة بالقصد، فيطلع شكل ألعاب زمان.

---

## ✂️ 5. Collage

لو عايز شكل مجلات وإعلانات.

```text
Build one Remotion composition in this folder (create the project if there is none): 1080x1920, 30 fps, exactly 150 frames, on-screen language [LANGUAGE].

Story: frames 0-30 the pieces of [PLACE] and [SUBJECT] slide in from the edges and lock into place. Frames 30-70 build-up. Frames 70-125 [ACTION]. Frames 125-150 the subject floats gently and [CAPTION] slams in on a tilted red card.

Rules: every value comes from useCurrentFrame(), seeded randomness only, no real brand names or logos.

Style: editorial paper collage, built in SVG.
- A flat, strong background colour such as mustard (#E5A92C).
- Halftone cut-outs: an SVG pattern of black dots rotated 45 degrees.
- Every piece has a thick off-white stroke (paint-order: stroke), like cut paper.
- Limited palette: black, off-white, one strong red and one teal.
- Pieces move with smooth easing on every frame. Do not use stop-motion holds or per-frame jitter, because they look like lag.
- If [LANGUAGE] uses Arabic script, use a bold Arabic font and set direction to rtl.

Export stills at frames 30, 90 and 140, fix any problems, then render out/collage.mp4.
```

**بيعمل إيه؟** بيخلي الفيديو شكله قصاصات ورق بتتركب قدامك.
**نصيحة:** ماتخليهوش يعمل stop-motion، لأنه على الموبايل بيبان كأن الفيديو بيقطّع.

---

## ✍️ 6. Handwritten

لو عايز حاجة قريبة وبسيطة كأنها مرسومة في كشكول.

```text
Build one Remotion composition in this folder (create the project if there is none): 1080x1920, 30 fps, exactly 150 frames, on-screen language [LANGUAGE].

Story: frames 0-60 [SUBJECT] is drawn stroke by stroke in [PLACE]. Frames 60-125 [ACTION]. Frames 125-150 the subject floats gently and [CAPTION] is written in red.

Rules: every value comes from useCurrentFrame(), seeded randomness only, smooth eased motion, no real brand names or logos.

Style: blue ballpoint on a school notebook, built in SVG.
- Cream paper (#FBF8EE), pale blue ruled lines and one red margin line.
- Blue ink (#173B9C). Every outline uses pathLength=1 and animates stroke-dashoffset, one path after another.
- A slight hand wobble using feTurbulence and feDisplacementMap. Keep the seed constant so lines don't flicker.
- Draw a pen whose tip follows the line being drawn, using getPointAtLength.
- Handwritten notes at the top. For Arabic script use the Aref Ruqaa font, direction rtl, and reveal the text from right to left with a moving clip, with the pen following it.

Export stills at frames 30, 90 and 140, fix any problems, then render out/handwritten.mp4.
```

**بيعمل إيه؟** الرسمة بتتكتب حتة حتة وقلم ماشي معاها.
**نصيحة:** الكتابة العربي مش بتترسم حرف حرف، فالـ Prompt بيخليها تظهر من اليمين للشمال ورا القلم.

---

## ➖ 7. Minimal Line

لو عايز شكل هادي وذكي.

```text
Build one Remotion composition in this folder (create the project if there is none): 1080x1920, 30 fps, exactly 150 frames, on-screen language [LANGUAGE].

Story: frames 0-40 [SUBJECT] is drawn in thin lines in [PLACE]. Frames 40-70 build-up. Frames 70-125 [ACTION]. Frames 125-150 the subject floats gently and [CAPTION] fades in.

Rules: every value comes from useCurrentFrame(), seeded randomness only, smooth eased motion, no real brand names or logos.

Style: minimal line art, built in SVG.
- Pure black background and nothing but thin white lines, 1 to 1.5 px.
- Outlines draw themselves with pathLength=1 and stroke-dashoffset.
- Small white dots on the main corners of the subject.
- Faint grey concentric circles behind the subject.
- One tiny stick figure on a single horizon line.
- A row of white dots on thin sticks along the bottom that rise during the action.
- Reduce [PLACE] to a few simple lines. Do not add colour.

Export stills at frames 30, 90 and 140, fix any problems, then render out/minimal-line.mp4.
```

**بيعمل إيه؟** بيشيل كل حاجة زيادة ويسيب خطوط رفيعة بس.

---

## 🎥 8. CGI

لو عايز شكل فيلم.

```text
Build one Remotion composition in this folder (create the project if there is none): 1080x1920, 30 fps, exactly 150 frames, on-screen language [LANGUAGE]. Install three and @types/three.

Story: frames 0-30 [SUBJECT] is still in [PLACE] at night with a small crowd in front. Frames 30-70 build-up. Frames 70-125 [ACTION] and the crowd raises its arms. Frames 125-150 the subject floats gently and [CAPTION] appears.

Rules: every value comes from useCurrentFrame(), seeded randomness only, smooth eased motion, no real brand names or logos.

3D setup: use three.js directly. Create the WebGLRenderer once with preserveDrawingBuffer true and pixel ratio 2, update objects from the frame number, and call render inside useLayoutEffect. Render with --gl=angle.

Style: dark cinematic CGI.
- MeshPhysicalMaterial with clearcoat 1 and low roughness on the subject.
- ACES filmic tone mapping, RoomEnvironment reflections at low intensity, and dark blue fog.
- A dark city background with an emissive window texture.
- Soft smoke using sprites with a radial-gradient texture.
- A thin glowing ring on a wet, reflective ground.
- A warm point light that follows the action.

Export stills at frames 30, 90 and 140, fix any problems, then render out/cgi.mp4.
```

**بيعمل إيه؟** بيعمل مشهد 3D ليلي بانعكاسات ودخان ونور.

---

## 🧱 9. Bricks

لو عايز حاجة لطيفة شكلها لعب أطفال.

```text
Build one Remotion composition in this folder (create the project if there is none): 1080x1920, 30 fps, exactly 150 frames, on-screen language [LANGUAGE]. Install three and @types/three.

Story: frames 0-30 [SUBJECT] is still in [PLACE] with a small crowd in front. Frames 30-70 build-up. Frames 70-125 [ACTION] and the crowd raises its arms. Frames 125-150 the subject floats gently and [CAPTION] appears.

Rules: every value comes from useCurrentFrame(), seeded randomness only, no real brand names or logos.

3D setup: use three.js directly. Create the WebGLRenderer once with preserveDrawingBuffer true and pixel ratio 2, update objects from the frame number, and call render inside useLayoutEffect. Render with --gl=angle.

Style: toy bricks. Never use a toy company's name, logo or figure shape.
- Everything, including the subject and the characters, is built from boxes with round studs on top.
- Glossy plastic: MeshPhysicalMaterial with clearcoat around 0.85.
- A green studded baseplate using InstancedMesh for the studs.
- Stacked coloured brick towers to suggest [PLACE].
- Smoke is made of white bricks, not soft particles.
- Soft shadows from one directional light.
- Motion stays smooth on every frame. No stop-motion holds.

Export stills at frames 30, 90 and 140, fix any problems, then render out/bricks.mp4.
```

**بيعمل إيه؟** بيبني العالم كله من مكعبات، حتى الدخان.
**نصيحة:** ماتكتبش اسم شركة ألعاب في الفيديو، اكتب Bricks وخلاص.

---

## 🍡 10. Clay 3D

لو عايز شكل دافي ولطيف.

```text
Build one Remotion composition in this folder (create the project if there is none): 1080x1920, 30 fps, exactly 150 frames, on-screen language [LANGUAGE]. Install three and @types/three.

Story: frames 0-30 [SUBJECT] is still in [PLACE] with a small crowd in front. Frames 30-70 build-up. Frames 70-125 [ACTION] and the crowd raises its arms. Frames 125-150 the subject floats gently and [CAPTION] appears.

Rules: every value comes from useCurrentFrame(), seeded randomness only, smooth eased motion, no real brand names or logos.

3D setup: use three.js directly. Create the WebGLRenderer once with preserveDrawingBuffer true and pixel ratio 2, update objects from the frame number, and call render inside useLayoutEffect. Render with --gl=angle.

Style: soft matte clay.
- MeshStandardMaterial with roughness around 0.96 and no reflections.
- Use RoundedBoxGeometry and spheres, so nothing has a sharp edge.
- A pastel background and pastel simplified shapes for [PLACE].
- PCFSoftShadowMap with a large shadow radius.
- Smoke is made of big smooth cream spheres that grow.

Export stills at frames 30, 90 and 140, fix any problems, then render out/clay-3d.mp4.
```

**بيعمل إيه؟** بيخلي كل حاجة شكلها معمولة من صلصال.

---

## 🇪🇬 تقدر تكتبله بالمصري كمان

```text
اعملي فيديو أنيميشن بـ Remotion، مقاسه 1080x1920، و30 فريم في الثانية، ومدته 5 ثواني.

البطل: [البطل بتاعك]
المكان: [المكان]
اللي بيحصل: [الحاجة المفاجئة]
الكلمة اللي تظهر في الآخر: [الكلمة]

الستايل: كشكول مدرسة وقلم جاف أزرق، والرسمة تترسم قدامنا حتة حتة وقلم ماشي معاها.

خلي الحركة ناعمة ومفيهاش تقطيع، وكل حاجة تتحسب من رقم الفريم. طلّعلي صور من 3 لحظات وبصلها وصلّح أي غلط، وبعدين اعمل Render للفيديو.
```

---

## ⚠️ نصايح مهمة

- ابدأ بستايل واحد، وبعدين كمّل، عشان ماتضيعش حدود اشتراكك.
- ماتستخدمش اسم شركة أو لوجو أو شخصية مش بتاعتك في الفيديو.
- لو في تقطيع، قوله: `Make the motion smooth on every frame and remove any held poses or jitter`.
- لو الكتابة العربي طالعة مقطعة أو بالعكس، قوله يحمّل font عربي ويخلي الـ direction بتاعها `rtl`.
- لو هتستخدم Remotion في شركة، راجع الـ license بتاعته: https://www.remotion.dev/license

## 🚀 الخلاصة

| قبل | بعد |
|---|---|
| After Effects وساعات شغل | Prompt واحد و Claude Code |
| ستايل واحد في كل الريلز | 10 ستايلات لنفس الفكرة |
| فيديو شكله زي أي حد | بطل ومكان من عندك |
| تدفع لمونتير لكل تجربة | تجرب وتغيّر في دقايق |

---
لو استفدت، تابعني عشان فيه Prompts وأتمتة أكتر جاية 🔥

**Steven Ayman — Vida AI**
