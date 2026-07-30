# Summary: Calls with Lev Rudky - 15 April 2026

Two calls recorded back-to-back (1h 1m and 17m). Conducted primarily in Russian. Participants: Val Levitan and Lev Rudky. Topics focus on Microsoft Dynamics 365 Business Central configuration and procurement processes at JVL.

---

## 1. Progress Payment Add-on (AP Commerce) - Status & History

- The progress payment invoicing add-on from **AP Commerce** was purchased and installed around **February 2026**. Igor tested it; Lev deemed it acceptable for accounting purposes and trained Chris on it.
- Within 1-2 weeks, Chris reported it stopped working. Lev investigated and eventually brought in Microsoft support, the Minsk admin team, and the AP Commerce vendor.
- Root cause was never fully identified. The vendor recommended **unsubscribing and resubscribing** to the add-on, which fixed it. The fix has been in place since approximately **mid-March**.
- **Communication gap:** Val was frustrated because in a Monday (April 14) conversation, Lev left the impression the add-on still wasn't working. Lev clarified it has been functional for about a month and apologized for the miscommunication.

## 2. Payment Terms Table - Cleanup Needed

- Val and Lev reviewed the **payment terms configuration table** in Business Central, which governs due date calculations for both payables and receivables.
- Val flagged that the existing codes are **inconsistently named** (mixed capitalization, spacing) and the table is confusing to interpret.
- Lev added **new payment terms** assigned to specific customers/vendors but left the old (potentially incorrect) terms in the system.
- **Action needed:** Old/unused payment terms must be cleaned up (deleted) to avoid confusion. Only the newly created, correctly configured terms should remain.
- **Calculation error identified:** On a "zero down, 2-month grace period, 6 equal payments" term, the first payment was set at 60 days instead of 90 days, and the percentage was divided by 6 instead of correctly reflecting the payment schedule after the grace period.

## 3. Progress Payment vs. Installment Payment - Key Architectural Difference

- **Installment payments** (sales/customer side): **Time-driven** - payments occur at fixed calendar intervals (e.g., every 30 days for 9 payments). Predictable and auto-calculated.
- **Progress payments** (purchase/vendor side): **Event-driven** - payments are triggered by milestones (purchase order issuance, shipment, receipt of goods). Cannot be predicted by calendar alone.
- This is why both AP Commerce add-ons were needed - the installment add-on could not be repurposed for vendor-side progress payments as Lev originally hoped.
- **Val's insight for future negotiations:** If JVL negotiated vendor payment terms as **calendar-driven** (tied to shipment date) rather than event-driven milestones, it would significantly reduce manual posting work and human error risk. Val wants to move toward this approach for future purchase orders.

## 4. Purchase Process Events & Invoice Posting

- Every payment event in the purchase lifecycle must be recorded via a **posted purchase invoice** in Business Central to create proper entries in the **vendor ledger** and **general ledger (GL)**.
- Standard purchase flow events: (1) Purchase Order issued, (2) Vendor invoice received, (3) Purchase Receipt (goods received).
- When progress payments are involved, each milestone payment requires its own purchase invoice to be posted - even when the vendor doesn't provide a separate invoice for each milestone. JVL **emulates this internally** by posting purchase invoices against the purchase order for each payment tranche.
- Val now understands that "purchase invoice" in this context refers to the **posting process** in BC, not necessarily a document received from the vendor.

## 5. Sales People Licensing

- Sales staff need **Microsoft Business Central licenses** (not AP Commerce licenses) to create sales orders. They don't need the progress payment add-on.
- BC licenses are **annual commitments** that can be reassigned between users but cannot be cancelled mid-term. A shorter (6-month) option exists but isn't much cheaper.
- Lev experienced an issue where **license reassignment took 2.5 days** to sync (normally 15-30 minutes). A Microsoft support ticket was opened, but it eventually resolved on its own.

## 6. Sales Person Data Segregation - Unresolved

- Val wants each sales person to **only see their own customers** and not be able to create sales orders for other reps' customers.
- Lev has been working on this using **permission sets with security filters** in Business Central.
- **Current status: Not working.** The issue is that higher-level permission sets (e.g., "super" permissions) override the security filters, making the restrictions ineffective. Conflicting permission sets nullify the field-level filters.
- Val expressed frustration and **parked this topic** for a future discussion.

---

## Open Action Items

| # | Item | Owner |
|---|------|-------|
| 1 | Clean up old/unused payment terms from the payment terms table | Lev |
| 2 | Fix the 60-day vs 90-day first-payment calculation on grace-period terms | Lev |
| 3 | Resolve sales person data segregation (permission set security filters) | Lev |
| 4 | Explore calendar-driven payment terms for future vendor negotiations | Val |
| 5 | Val to review and digest the purchase process/event flow, may have follow-up questions | Val |
