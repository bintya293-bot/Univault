# UniVault PWA Starter

Mobile-first Progressive Web App starter for Eastern University. This is a starter, not a finished production service.

## 1. Publish the app free with GitHub Pages
1. Upload the contents of this folder to the root of your public GitHub repository (not the ZIP itself).
2. Open repository Settings → Pages.
3. Under Build and deployment, choose Deploy from a branch, branch `main`, folder `/(root)`, then Save.
4. Wait for the published URL shown on the Pages screen. Open it on Android Chrome and use menu → Add to Home screen.

## 2. Configure free Supabase cloud services
1. Create a project at https://supabase.com.
2. In Project Settings → API, copy Project URL and anon/publishable key.
3. Replace the two placeholders at the top of `app.js`. Never put a service_role/secret key in this app.
4. In Supabase SQL Editor, run `supabase_setup.sql`.
5. In Storage, create a private bucket named `course-pdfs`.
6. After creating your own account in UniVault, run the admin insert statement in the SQL comments, replacing YOUR_EMAIL with your email.

## Important limitations
- Free service plans have quotas and can change; they are not guaranteed unlimited or permanently free.
- Admin moderation currently uses the `admins` table; admin review can be done in Supabase table editor by changing a row's status to `approved` or `rejected`.
- This starter does not yet include a full admin dashboard, preloaded departments/courses, full offline PDF downloads, or a native APK.
- Test with non-sensitive sample PDFs before inviting other students. Do not upload copyrighted or private student records without permission.
