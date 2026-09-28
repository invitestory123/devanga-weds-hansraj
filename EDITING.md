# Editing Guide — Toran Telugu

Fast customer customization guide for `toran-telugu` (Tamil / South Indian wedding template).

## Primary Customer Data

All text, dates, events, venue, story milestones, and images live in:
- `editable/wedding-data.js`

### What to edit in `editable/wedding-data.js`:
- **Brand & Couple**:
  - `brand`: Invitation branding tag
  - `couple.bride`: Bride's name (e.g. `"Tarunika"`)
  - `couple.groom`: Groom's name (e.g. `"Abbhi"`)
  - `couple.coupleLine`: Array `["Groom", "Bride"]`
  - `couple.hashtag`: Couple hashtag (e.g. `"#AbbhiWedsTarunika"`)
  - `couple.intro`: Family introduction line
- **Wedding Date & City**:
  - `wedding.iso`: ISO timestamp for countdown (e.g. `"2026-11-22T06:30:00+05:30"`)
  - `wedding.dateLabel`: `{ day, number, monthYear, time }`
  - `wedding.city`: Host city name (e.g. `"Coimbatore"`)
- **Venue**:
  - `venue.name`, `venue.address`, `venue.lat`, `venue.lng`, `venue.mapQuery`
- **Events**:
  - `events[]`: List of events with `id`, `name`, `tamil`, `description`, `start`, `end`, `venue`, `address`, `dressCode`, `dressColor`
- **Story Milestones**:
  - `story[]`: Array of milestones with `year`, `title`, and `text`
- **Families & Contacts**:
  - `families[]`: Bride and groom parents
  - `contacts[]`: RSVP contacts
- **Assets & Gallery**:
  - `assets.heroFlatlay`: Path to top flatlay background
  - `assets.jasmineStrand`: Path to jasmine garland graphic
  - `assets.gopuram`: Path to temple gopuram graphic
  - `gallery[]`: Array of `{ src, alt }` items

## Replacing Assets

Drop customer replacement images into `editable/assets/`:
- `editable/assets/couple-1.jpg` … `couple-4.jpg` — Moments swipe gallery
- `editable/assets/hero-flatlay.jpg` — Flatlay decorative image
- `editable/assets/gopuram.png` — Gopuram line illustration

## Testing

```bash
node --check editable/wedding-data.js
```
Open `http://localhost:9030/` in browser (note: use `/` root route, not `/index.html`).
