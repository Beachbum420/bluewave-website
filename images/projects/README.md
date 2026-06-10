# Project photos

Drop completed-project photos in this folder, then add a tile in `index.html`
inside the `<div class="gallery">` block:

```html
<a class="shot" href="images/projects/your-photo.jpg">
  <img src="images/projects/your-photo.jpg"
       alt="Short description — e.g. Kitchen remodel, Redondo Beach"
       loading="lazy" />
</a>
```

Tips for a clean look:

- **Aspect ratio:** tiles crop to 4:3. Landscape photos look best.
- **Size:** export around 1200–1600px wide, JPG quality ~80%. Keep each file
  under ~400 KB so the page stays fast.
- **Naming:** lowercase, hyphenated, descriptive — `kitchen-redondo-2026.jpg`.
- **Alt text:** always fill it in. It helps SEO and accessibility.

Once you have 3+ real photos, delete the two `.shot.placeholder` tiles in
`index.html`. The grid stays centered and intentional at any count.
