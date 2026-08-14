# TPLS Teacher Portal — Public Web Version

This is a standalone teacher portal. It uses the same Supabase project as the existing admin software.

## What it does
- Public teacher sign-in page with The Progress of Life School branding.
- Teacher authentication with Supabase email/password.
- Loads the teacher profile by the authenticated email.
- Loads assigned classes and subjects.
- Automatically shows students belonging to the teacher's assigned classes.
- Loads teacher/student photos from private Supabase Storage buckets.
- Responsive on phone and desktop.
- Includes SEO title/description and robots/sitemap files for the public login page.

## Important
This package does NOT modify the existing admin application or run any database changes.

Before giving this portal to real teachers, the Supabase Row Level Security policies must be hardened so an authenticated teacher can only query their own teacher profile, their assignments, and students in their assigned classes. The existing admin project currently has broad authenticated-user policies, so the front-end filtering alone must not be treated as the final security boundary.

## Deployment
For a static deployment, upload this folder to a static host. Vercel Drop can deploy a ZIP and gives the deployment a public URL. For ongoing updates with the same URL, connect the project to a Git repository.

After deployment, add the deployed URL in Supabase Authentication URL/Redirect settings if password reset or email-link flows are later enabled.


## Added in v4
- Read-only monthly fee status for assigned students.
- Leave application form.
- Suggestion-to-admin form.
- Initial teacher rules/expectations section.
- More polished dashboard cards and responsive layout.

Run TPLS_TEACHER_REQUESTS_SETUP.sql once in Supabase SQL Editor before using the leave/suggestion forms. This creates only the new teacher_requests table and RLS policies.
