# Deploy to Render

This repository includes `render.yaml`, which defines the web service, a 1 GB persistent disk, the SQLite database location, persistent uploads, and required environment variables.

## What you must do

1. Create a new empty GitHub repository.
2. Upload all files from this project to the repository root. `render.yaml` and `package.json` must be visible at the root.
3. Sign in to Render and choose **New > Blueprint**.
4. Connect the GitHub repository.
5. Render will read `render.yaml` automatically.
6. Enter the prompted secret values:

   - `ADMIN_NAME`: Syead Afridi Wafi
   - `ADMIN_EMAIL`: get.syeadafridi@gmail.com
   - `ADMIN_PASSWORD`: create a strong, unique password
   - `NEXT_PUBLIC_SITE_URL`: initially enter the expected Render URL, such as `https://syead-portfolio.onrender.com`. If Render assigns another URL, update this variable after the first deployment and redeploy.

7. Confirm the paid **Starter** service and 1 GB persistent disk.
8. Select **Apply** to deploy.

`AUTH_SECRET` is generated automatically by Render.

## After deployment

- Public website: `https://YOUR-SERVICE.onrender.com`
- Admin login: `https://YOUR-SERVICE.onrender.com/admin/login`

Test these actions:

1. Log in to the admin panel.
2. Upload an image.
3. Create and publish a blog post.
4. Create and publish a portfolio project.
5. Submit the public contact form.
6. Manually redeploy and confirm the content remains available.

## Custom domain

In the Render service, open **Settings > Custom Domains**, add your domain, and copy the displayed DNS records into your domain provider.

## Important

- The attached disk is required because this version uses SQLite and local uploads.
- Do not switch the service to a free plan; free services cannot use this persistent-disk configuration.
- Never commit your real admin password to GitHub.
