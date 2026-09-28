HAMID METAL INDUSTRIES — SECURE WEBSITE V3

Files:
- index.html = public website; visitors can only view gallery.
- admin.html = protected admin page; requires Supabase Auth login.
- supabase.sql = database table + Row Level Security policies.

Setup (one-time):
1. Create a Supabase project.
2. Run supabase.sql in SQL Editor.
3. In Authentication, create ONE admin user with your email/password.
4. Copy Project URL and anon/publishable key into BOTH HTML files:
   YOUR_SUPABASE_URL
   YOUR_SUPABASE_ANON_KEY
5. Publish index.html and admin.html on GitHub Pages.

Security:
- Never put the admin password in the code.
- Public visitors do not get edit/delete controls.
- Database writes require an authenticated Supabase user through RLS.
- For a stricter single-admin setup, we can add an admin-role table/policy before launch.
