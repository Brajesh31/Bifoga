# ⚡ Performance Guide

## 1. Performance profile

The current application is a small static website. Its performance is primarily affected by HTML size, stylesheet size, image dimensions, font loading, third-party requests, and browser-side JavaScript. There is no server rendering, API latency, database query, or model inference pipeline in the repository.

## 2. Asset optimization

- Keep image dimensions close to their rendered size.
- Prefer modern compressed formats for new photographic assets when browser support and hosting allow.
- Avoid shipping large images for small decorative elements.
- Provide explicit image dimensions or aspect ratios to reduce layout shifts.
- Use descriptive filenames and meaningful alternative text.
- Do not add large demo videos or screenshots without a clear visitor benefit.

## 3. CSS and Tailwind

The Tailwind content configuration should scan the actual HTML files that contain utility classes. If a new page or template is added, verify that its classes are included in the generated output.

The current npm Tailwind command is a watch task. It is intended for development and should not be confused with a production optimization pipeline. Before changing the output strategy, document the new build command and deployment artifact.

## 4. JavaScript

The current JavaScript surface is small. Keep interactions lightweight and avoid introducing large libraries for simple DOM behavior. Load scripts without blocking initial page parsing when the markup and initialization strategy permit it. Avoid repeated layout reads/writes in loops if the page grows more interactive.

## 5. Fonts and external resources

- Prefer a small number of font families and weights.
- Check the actual network waterfall for external font requests.
- Avoid unnecessary third-party scripts.
- Use appropriate font-display behavior for web fonts.
- Document external resources and their privacy/performance impact.

## 6. Measurement

Use browser developer tools or Lighthouse against a real served build. Record the tested URL, device profile, date, and measured metrics. Useful indicators include:
- Largest Contentful Paint (LCP).
- Cumulative Layout Shift (CLS).
- Interaction to Next Paint (INP).
- Total transferred bytes.
- Number of requests.
- Console and network failures.

No benchmark score is claimed by this document. Measure before and after each meaningful optimization.
