# Rental Lead Map

An interactive map for tracking rental listings you have contacted and where each one stands, built during a real apartment hunt when the list of landlords, texts, and half-answered pet questions outgrew every spreadsheet.

**Live demo:** open `index.html` in a browser (or serve the folder with any static host).

## What it does

- Plots every rental lead as a numbered pin on an OpenStreetMap (Leaflet) map
- Color codes each lead by status:
  - ⚫ **Black: waiting** — inquiry sent, no reply yet
  - 🟡 **Yellow: considering** — they answered, still deciding
  - 🟢 **Green: strong lead** — good back and forth, high on the list
- Add a rental with an address and it is located on the map automatically (Nominatim geocoding)
- Click a card or pin to jump between the list and the map
- Change a lead's status with one tap, edit its details, or delete it when it becomes a dead end
- Filter the list by status; leads sort strongest first, then cheapest
- Each lead stores rent, contact, the pet-policy answer, and free notes
- Data persists in the browser (localStorage). No accounts, no server, no tracking

Ships with two clearly labeled demo entries so the map is not empty on first open. Delete them and add your own.

## Tech

Plain HTML, CSS, and JavaScript. [Leaflet](https://leafletjs.com/) for the map, OpenStreetMap tiles, Nominatim for geocoding. No build step and no dependencies to install.

## Why

Rental hunting by inbox is chaos: dozens of near-identical listings, landlords who answer half a question, and no single view of what is alive, what is waiting, and what is dead. This puts the whole search on one map, in three colors.
