# B.A.D.G.E. – Badge Accountability & Disclosure for General Ethics

> **"Blink Responsibly."**

## What Is B.A.D.G.E.?

**B.A.D.G.E.** is a self-assessment and transparency framework for electronic badge creators—born at DEF CON, but applicable anywhere in the hacker and maker world.

While badges often spark joy, creativity, and community, they can also introduce **safety hazards** and **environmental waste** if poorly designed. **B.A.D.G.E. exists to help badge makers document and disclose how they've designed for human safety and environmental responsibility.**

This project encourages:
- Safer designs through voluntary disclosure
- Transparent documentation of batteries, power systems, materials, and connectivity
- Environmentally conscious choices in manufacturing and disposal
- Empowering users to understand what they’re wearing and how to handle it responsibly

---

## ✅ What Is a "B.A.D.G.E. Sheet"?

Your **B.A.D.G.E. Sheet** is a simple checklist (or table) that shows which safety and environmental best practices your badge follows. You can publish it on your GitHub repo, or print it on materials distributed with your badge. A compliance logo is also provided for this as well, or could be silk screened onto your badge.

Include the ✅ emoji for every item you meet, ❌ for what you intentionally did not include, and ⬜ for items that are not applicable to your badge design.
---

## Sample B.A.D.G.E. Sheet Format

| Category                        | Item                                                | Status | Notes                            |
|--------------------------------|-----------------------------------------------------|--------|-----------------------------------|
| **Human Safety**               |                                                     |        |                                   |
| **Battery & Power Safety**      | Overcharge protection                               | ✅     | TI BQ25895 onboard and built into battery  |
|                                 | Current-limited charging                            | ✅     | Limited by TI BQ25895 config      |
|                                 | Temperature protection                              | ✅     | Built into battery                |
|                                 | Short-circuit protection                            |  ✅    | Built into battery                |
|                                 | Battery physically covered                          | ❌     |                                   |
|                                 | Reverse polarity protection                         | ✅     | Built into battery                |
|                                 | Battery securely adhered                            | ✅     | 4mm adhesive foam                 |
|                                 | Battery brand and chemistry disclosed               | ✅     | YDL 3.7v 3000mA LiPo              |
| **User Safety & EMC**           | No exposed high-voltage pads                        | ✅     | Max voltage = 5V                 |
|                                 | Exposed conductive surfaces minimized               | ✅     | No exposed copper; all pads covered by soldermask; nylon fasteners |
|                                 | Non-conductive housing or enclosure                 | ✅     |                                   |
|                                 | PCB edges rounded or beveled                        | ✅     | Rounded corners                   |
|                                 | Sharp component leads trimmed or insulated          | ✅     |                                   |
|                                 | Battery connectors not user-accessible              | ❌     |                                   |
|                                 | All external ports labeled                          | ✅     |                                   |
|                                 | Heat-tested under continuous use                    | ✅     | Stable under 6+ hrs at max load   |
|                                 | Low-voltage toy-safe design (<24V)                  | ✅     | RP2040 logic                      |
| **Connectivity & RF**           | No wireless (Wi-Fi/BLE/RF)                          | ✅     | No radio components               |
|                                 | USB data lines disabled                             | ❌     | USB only used for charging and reprogramming        |
|                                 | No HID, keyboard, or storage emulation              | ✅     | Storage emulation only for firmware loading in RP2040 bootloader                |
|                                 | Use of off-the-shelf RF modules / ICs               | ⬜     | Not applicable – no RF present    |
|                                 | RF emissions within FCC limits                      | ⬜     | Not applicable – no transmitters  |
|                                 | RF exposure safe for wearable devices               | ⬜     | Not applicable – no RF hardware   |
|                                 | RF modules have shielding cans                      | ⬜     | Not applicable – no RF hardware   |
|                                 | MAC address randomized or disclosed                 | ⬜     | Not applicable - no network       |
|                                 | Transmission duty cycle limited                     | ⬜     | Not applicable – no RF present    |
| **Privacy**                     | No user data stored                                 | ✅     | No flash usage                    |
|                                 | Firmware is open source                             | ✅     |                                   |
|                                 | No persistent user identifiers                      | ✅     |                                   |
|                                 | No telemetry or beaconing                           | ✅     |                                   |
|                                 | QR codes or NFC tags disclosed                      | ✅     |                                   |
| **Environmental Impact**        |                                                     |        |                                   |
| **Materials & Manufacturing**   | RoHS-compliant components                           | ✅     | JLCPCB RoHS BOM                   |
|                                 | REACH-compliant where possible                      | ✅     | Common passive parts              |
|                                 | Lead-free solder used                               | ✅     | SAC305 alloy                      |
|                                 | ENIG finish (no leaded HASL)                        | ✅     | Yes                               |
|                                 | Halogen-free PCB laminate                           | ✅     |                                   |
|                                 | Low-VOC silkscreen ink                              | ✅     |                                   |
|                                 | Conflict minerals sourcing disclosure               | ❌     |                                   |
|                                 | Low-layer-count PCB                                 | ✅     |                                   |
| **Design for Reuse / Repair**   | Badge can be repurposed post-event                 | ✅     | Arduino-compatible firmware       |
|                                 | Modular parts/connectors for reuse                  | ✅     | USB-C, JST-PH                    |
|                                 | Minimal adhesives used                              | ✅     | No glues, only removable tape     |
|                                 | Designed for easy disassembly                      | ✅     | Screws, no welding                |
|                                 | Example code for reuse provided                     | ✅    |                                   |
|                                 | Pinout diagram included                             | ⬜     | Not applicable - no user exposed headers       |
|                                 | OpenSCAD/STEP files for enclosure shared            | ❌     |                                   |
| **End-of-Life Responsibility**  | Battery is removable                                | ✅     | JST-PH connector                  |
|                                 | Disposal guidance provided                          | ❌     |                                   |
|                                 | Plastic marked or recyclable                        | ✅     | PLA shell                         |
|                                 | Battery removal instructions included               | ✅     |                                   |
|                                 | Silkscreen includes recycle/warning icons           | ❌     |                                   |
|                                 | Can be returned, reused, or donated                 | ✅     | Encouraged at next DEF CON        |
| **Supply Chain and Transparency** | BOM and schematic published                        | ❌     |                                   |
|                                 | Traceable part sourcing                             | ✅     | LCSC, DigiKey BOM                 |
|                                 | Local or regional manufacturing preferred           | ❌     | JLCPCB (China)                    |
|                                 | Ethical material sourcing where possible            | ✅     | Lead-free parts and supply chain  |
|                                 | GitHub includes changelog or commit history         | ✅     |                                   |

**Legend:**  
✅ = Compliant or included in design  
❌ = Not included / does not meet standard  
⬜ = Not applicable to this badge  
---

## How to Use This Framework

![B.A.D.G.E. Compliant – Blink Responsibly](images/badge-compliant-logo-light.svg)
![B.A.D.G.E. Compliant – Blink Responsibly](images/badge-compliant-logo-dark.svg)

1. **Start With Your Design**  
   - Plan for safety: test for heat, secure the battery, limit current.
   - Choose RoHS/REACH-compliant parts when possible.
   - Label components, voltages, and connection points.

2. **Build Your B.A.D.G.E. Sheet**  
   - Use the table above as a template.
   - Mark what applies ✅ or doesn't ❌.
   - Add notes, part numbers, or links.

3. **Publish It Publicly**  
   - Include your B.A.D.G.E. Sheet in your GitHub repo, silkscreen, QR code, or printed insert.
   - **Proud of your compliance? Display the B.A.D.G.E. Compliant logo** (like the one above) on your README, badge materials, badge, or website.
   - Help others understand your badge’s safety and environmental design at a glance.

4. **Promote the Framework**  
   - Use the tagline: **"Blink Responsibly"**
   - Encourage other badge makers to adopt and share their own B.A.D.G.E. Sheets.

---

## Why It Matters

- **Human safety**: DEF CON badges go around necks, into backpacks, and into hands of attendees young and old.
- **Environmental impact**: These devices blink for a weekend, but the components may sit in a landfill for 500 years.
- **Transparency builds trust**: If you're proud of your work, show your receipts. Let users know what’s inside.

---

## B.A.D.G.E. Resources

- [B.A.D.G.E. Sheet Template (Markdown)](./TEMPLATE.md)
- [Example B.A.D.G.E. Sheet (O.R.E.O. Badge)](./examples/oreo-badge.md)
- [The SEC Village Badge GitHub Repo](https://github.com/secommunity/SEC-DEF-CON-33-Oreo-Badge)
- [Electronics Waste Recycling Guidance (EPA)](https://www.epa.gov/recycle/electronics-donation-and-recycling)

---

## License & Attribution

This framework is open source under the MIT License.  
Created by [Brent Dukes](https://twitter.com/TheDukeZip) for the [Social Engineering Community](https://se.community/) at DEF CON 33.  

> Inspired by a simple idea:  
> **"I want everyone to go home from DEF CON in the same condition they showed up in."**  
> — and for the Earth to do the same.

---

