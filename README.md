# hash-gen

**Hash Fingerprint Lab — SHA-256 digital fingerprint visualiser**

## Project history

### Version 1: SHA-256 Hexadecimal Trippy Animation

The first version of `hash-gen` was a simple visual experiment. A user could type text into the page, generate a SHA-256 hash, copy the result, and watch hexadecimal characters dance around the screen in a colourful p5.js animation. It included a central Bitcoin symbol and treated the hash mainly as a visual object: mysterious, mathematical, and slightly psychedelic.

Version 1 worked as a fun browser toy, but it did not fully explain why hashing matters. It generated a hash, but it did not clearly show what a hash is for.

## Version 2.4: Hash Fingerprint Lab

Version 2.4 rebuilds the project as a clearer, more useful single-file web app about **digital fingerprints**.

Instead of only showing one animated hash, the app now lets users compare an **original text** with a **changed text**. It calculates the SHA-256 fingerprint for both versions and shows how even a tiny edit can produce a radically different result. This is known as the **avalanche effect**.

The goal is simple:

> Show how SHA-256 can detect change.

A hash is not encryption. It does not hide a message so it can be decrypted later. It creates a fixed-length fingerprint of the input. If the input changes, the fingerprint changes.

## What the app demonstrates

* **Digital fingerprints**: every input produces a 64-character SHA-256 hash.
* **Change detection**: identical text produces the same fingerprint; edited text produces a different one.
* **Avalanche effect**: one small change can flip many bits in the final 256-bit hash.
* **Tamper evidence**: the app shows why hashes are useful for checking whether something has been altered.
* **Static web app design**: the whole project runs as a single HTML file, suitable for GitHub Pages.

## Interactive features

* Type or edit original text.
* Compare it with a changed/test version.
* Generate SHA-256 fingerprints.
* View a 256-bit visual map of the hash.
* Highlight how many bits changed.
* Try built-in demos:

  * one-character change
  * identical text
  * fake invoice tamper
* Copy the original or changed fingerprint.
* Try the optional “hash lottery” bonus section, which searches for a hash beginning with a chosen number of zeros.

## Why this exists

`hash-gen` is a small educational browser app for understanding hashing through interaction rather than explanation alone.

It can help users understand ideas behind:

* file integrity checks
* tamper detection
* digital fingerprints
* blockchain proof-of-work concepts
* why tiny changes matter in cryptographic systems

It is not a security product, a password manager, a mining tool, or an encryption app. It is a visual learning tool.

## How to use

1. Open the live demo.
2. Read the short explanation at the top.
3. Click **Demo: one-character change**.
4. Watch how the SHA-256 fingerprint changes.
5. Try your own text.
6. Compare the original and changed versions.

## Technologies used

* HTML
* CSS
* JavaScript
* SHA-256 hashing in the browser
* Single-file static web app structure

## Running locally

Download or clone the repository, then open `index.html` in a browser.

```bash
git clone https://github.com/interstellar-hitchhiker/hash-gen.git
cd hash-gen
```

Then open:

```bash
index.html
```

## Design direction

Version 2.4 moves away from a generic “trippy animation” style and toward a clearer forensic-lab interface. The design is meant to match the concept: fingerprints, change detection, bit maps, and tamper evidence.

The project remains playful and visual, but the interface now has a stronger purpose: helping people see what a cryptographic hash actually does.
