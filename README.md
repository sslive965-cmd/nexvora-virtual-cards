# NEXVORA Virtual Cards Platform — new standalone project
This is a separate starter bundle and does not connect to or change your existing website.

## Setup
1. Create a **new** GitHub repository and a **new** Supabase project. Do not reuse your existing site's project.
2. Open SQL Editor in the new Supabase project and run `schema.sql`.
3. In `config.js`, replace `PASTE_NEW_SUPABASE_PROJECT_URL` and `PASTE_NEW_SUPABASE_PUBLISHABLE_KEY` with the new project's URL and publishable/anon key. Never use a service-role key in frontend code.
4. In Supabase Auth settings, turn off email confirmation if you want register to work without OTP/email confirmation.
5. Create a new Vercel project linked only to this new repository; upload all files at repository root.
6. Register/login using `virexabusiness143@gmail.com` and your chosen password to access the private control button. Add products there.

Features: animated 3D entry screen; login/register; RuPay, Visa, Mastercard and American Express categories; flip cards; INR prices; amount-specific UPI intent and QR; 15-minute client-side timer; UTR and screenshot upload; order dashboard; admin product/order controls.

Payment caveats: UPI app support differs by device. Check the amount before authorizing. UTR/screenshot are not proof by themselves—verify receipt in your UPI/bank account before approving. The timer is client-side, not a server-enforced deadline. Admin view currently shows screenshot path; secure preview/signed URL can be added before launch. Test all RLS/auth/storage policies with separate test accounts before real use.
