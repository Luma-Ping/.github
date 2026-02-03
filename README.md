# LumaPing

LumaPing is a small system utility for checking power availability at home.

It is designed to be glanceable, quiet, and honest — showing the current state without demanding attention.

---

## What it does

LumaPing shows:
- whether power is available right now
- when it last changed
- how availability behaved throughout the day and week

The focus is on clarity, not interaction:
no chats, no alerts by default, no constant checking.

---

## How it works

LumaPing determines power availability based on simple, external signals sent from a user’s home.

As long as signals arrive regularly, power is considered available.
If signals stop arriving for several minutes, the location is marked as unavailable.

Health-checks are expected roughly once per minute.
Checking more frequently would add unnecessary load without improving accuracy.

---

## Signal sources

LumaPing supports multiple types of signal sources.
You can choose the one that best fits your setup.

### Supported sources

**Health-check callback**  
A simple HTTP request sent periodically from any device.
This is the most flexible option and works well with scripts, servers, or automation tools.

**Single-board computer (SBC)**  
Devices like Raspberry Pi or similar can send regular health-checks while power is available.

**Microcontroller**  
Low-power devices such as ESP32 or ESP8266 can be used as minimal signal sources.

**Router reachability**  
Power availability can be inferred by checking whether a home router is reachable from the outside.
This requires the router to allow external pings.

---

## Design principles

- **Glanceable first**  
  The primary interface consists of widgets and indicators — menu bar, watch, phone, tablet.

- **Quiet by default**  
  Notifications are optional. The product should not create noise or anxiety.

- **Minimal data**  
  No personal addresses or public location maps.
  Only the data required to show the current state is stored.

- **Utility over engagement**  
  LumaPing is not designed to keep users active.
  It exists to be checked when needed.

---

## Status

LumaPing is available to sign in and use.

Some parts of the product are still evolving.
Users can opt in to receive a notification once the product is considered complete and stable.

---

## Non-commercial by design

LumaPing is intentionally non-commercial.
It was built as a utility, not a business.

There are no subscriptions, tiers, or paywalls.

---

## Repositories

This organization contains the source code for LumaPing and its related components.
Each repository includes its own README with technical details.

---

## License

See individual repositories for licensing information.
