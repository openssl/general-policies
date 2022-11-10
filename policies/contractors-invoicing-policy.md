# Contractors Invoicing Policy

The OpenSSL organization is purely remote without any office. The organization has only paid resources (contractors). Each contractor is obliged to submit their invoices to the OSS as per their contracts. **The submission should be done no later than the "Submission due dates" in the table "Payment Run Schedule" below for the given invoicing period or the payment will be subject to the next run (likely next month)**.

## Contractor Invoice Submission

1. Contractors send their invoices via the [Online Form] or send them directly to **finance@openssl.org** in the format and providing the information as detailed below. If an invoice is submitted via the form, notification to the finance@openssl.org mailing list will be sent automatically. 

In the form:
   * Select the month for your invoice.
   * Type the number of worked hours in the given month. (If contractor is on a fixed monthly rate, the number is not important and any number can be entered).
   * Add the invoice which should be in the a .pdf format and named as follows: **[YYYYMMDD]-[name-surname]-[invoicemonth][invoice year].pdf.**
 > eg: **20220813-Martin-Koci-Jul2022.pdf** or **20220913-Martin-Koci-JunJulAug2022.pdf** for invoicing more months

## Processing Submitted Invoices

2. Manager ensures invoices are correct (where applicable - right amounts for days worked and the requested amount, invoice is within the 3-month window, 1800 worked hours limit, ...). 

3. Correct invoices will be committed to the oss/financial/. repository with the correct filename format

4. Manager prepares the payments CSV file and commits this to the repo as soon as all eligible and correct invoices have been received for the given invoicing period or no later than the **Payment Run Date**. 

   * The payments CSV batch file will be created and committed for payment no later than **Payment Run Date** as listed in the [Payment Run Schedule Table].
   * If there is an exception, requestor should send it to their manager and to the **finance@openssl.org** mailing list.

5. Manager emails the treasurer (TO'ing) and finance@openssl.org (CC'ing) advising that the CSV Batch file is ready to be processed.
<br><br>

* Additional expenses as approved can be included, subject to the expenses reimbursement process to ensure the expenses are itemized in the right way for tax (etc). These additional expenses should be submitted via a google form that is created for this purpose. This will automatically send a notification to the finance@openssl.org mailing list too.
* Manager to batch payments (contractors expenses, invoices) as much as possible, to have a maximum of two potential payment dates a month, and communicate that to contractors.

[Payment Run Schedule Table]: (.../general-policies/policy-supplemental/Payment-Run-Schedule-Table.md)
[Online Form]: (.../docs.google.com/forms/d/e/1FAIpQLSeArUbveC_v_k39khbBc_PgE_qLRk3kBAd_j-0tc-knx-0bYA/viewform)
