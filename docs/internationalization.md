# 🌍 Internationalization and Localization

## Current state

The current page is primarily authored in English. The repository does not contain a translation catalog, locale switcher, language negotiation, or internationalized content pipeline.

## Preparation for future localization

- Set the document language accurately on the root HTML element.
- Keep user-facing copy separate from code where a translation workflow is introduced.
- Avoid concatenating sentence fragments to form translated messages.
- Format dates, numbers, currencies, and times with locale-aware browser APIs.
- Check text expansion in buttons, navigation, cards, and narrow layouts.
- Use fonts that support the target scripts.
- Provide a clear language switcher if multiple translations are published.
- Do not infer a visitor's language from sensitive or unreliable signals.

## Translation quality

Translations should be reviewed by a fluent human familiar with the intended audience and business terminology. Machine translation may be used as a draft, not as unreviewed final copy for legal, privacy, pricing, or service commitments.

## Accessibility

Language changes should be announced clearly and the page's language metadata should match the visible content. Avoid flag icons as the only language labels.

## Adoption checklist

Before adding another language, define supported locales, translation ownership, review process, fallback behavior, URL strategy, and how translated pages will be tested.
