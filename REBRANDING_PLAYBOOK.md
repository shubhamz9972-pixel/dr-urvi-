# Rebranding Playbook

This document serves as a master checklist for rebranding this dental clinic website. When updating the website for a new doctor, clinic name, or location, only modify the variables and assets outlined below.

---

## 1. Core Branding Assets
The website uses two main image assets that must be updated when changing the practitioner:

*   **Doctor Portrait**: 
    *   **File paths**: 
        *   [client.jpeg](file:///c:/Users/ASUS/nani%20ki%20website/donation/lumora-dental/assets/img/client.jpeg)
        *   [variant-blue/client.jpeg](file:///c:/Users/ASUS/nani%20ki%20website/donation/lumora-dental/variant-blue/assets/img/client.jpeg)
    *   **Action**: Overwrite these files with the new doctor's portrait (preferably a high-quality vertical portrait).
*   **Instagram Feed Preview**:
    *   **File paths**: 
        *   [instapage.jpeg](file:///c:/Users/ASUS/nani%20ki%20website/donation/lumora-dental/assets/img/instapage.jpeg)
        *   [variant-blue/instapage.jpeg](file:///c:/Users/ASUS/nani%20ki%20website/donation/lumora-dental/variant-blue/assets/img/instapage.jpeg)
    *   **Action**: Overwrite these files with a mobile screenshot of the new doctor's Instagram profile page.

---

## 2. Global Text & Code Replacements
Scan and replace the following text values across all 18 HTML files:

| Target Component | Previous Value (Dr. Naina) | Action / Target Replacement |
| :--- | :--- | :--- |
| **Doctor Name** | `Dr. Naina Sachdeva` | Replace with new doctor's name |
| **Clinic / Hub Name** | `Dr. Naina Sachdeva's Dental Hub` | Replace with new clinic name |
| **Email Address** | `nainasachdeva226@gmail.com` | Replace with new email in mailto links & visible text |
| **Phone Number (Text)** | `07470000006` | Replace with new visible phone format |
| **Phone Link (tel)** | `tel:07470000006` | Replace with new dial link format |
| **WhatsApp Redirection** | `wa.me/917470000006` | Replace with new WhatsApp API target number |
| **Instagram Profile Link** | `https://www.instagram.com/drnainasachdeva/` | Replace with new Instagram URL |
| **Instagram Handle** | `@drnainasachdeva` | Replace with new username handle |
| **Clinic Location / Address** | `45 Guru Angad Dev Nagar, Flower Enclave, Dugri, Ludhiana` | Replace with new physical address (on about pages) |
| **Footer Developer Credit** | `Crafted by Shubham` | Keep as `Crafted by Shubham` unless requested otherwise |

---

## 3. Navbar and Footer Logo Layout
The website uses text-based logo branding in the top navigation bar and footer.
*   **Top Navbar brand tag**: Contains a `<span>` element with the doctor's name:
    *   *Root pages*: `<span style="... color: #24a3b1; ...">Dr. Naina Sachdeva</span>`
    *   *Variant-blue pages*: `<span style="... color: #2f80ff; ...">Dr. Naina Sachdeva</span>`
*   **Footer brand tag**: Contains a `<span>` element with the doctor's name:
    *   *All pages*: `<span style="... color: #ffffff; ...">Dr. Naina Sachdeva</span>`
*   **Action**: Update the inner text of these spans to the new doctor's name. Do not add `<img>` tags unless explicitly asked to restore image logos.

---

## 4. Verification Check list
After completing any rebranding:
1.  Run the verification script `scratch/verify.py` (updated with the new name, email, and phone number parameters) to ensure no residual traces of the old brand remain in the codebase.
2.  Check for clean encoding (verify no `â€™`, `â€œ`, `â€`, or `Â ` sequences exist in HTML files).
3.  Deploy to Vercel and verify the live production build at `https://lumora-dental-eight.vercel.app`.
