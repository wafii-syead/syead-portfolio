# Syead Afridi Wafi — Full-Stack Portfolio CMS

A working full-stack portfolio starter built with Next.js, TypeScript, Prisma and SQLite.

## Included

- Responsive public portfolio
- Dark and light mode
- Blog listing and article pages
- Portfolio listing and project pages
- Contact form saved to the database
- Secure admin login
- Admin dashboard
- Blog create, edit, publish and delete
- Project create, edit, publish and delete
- Image and PDF uploads
- Contact-message management
- Database seed with an initial administrator
- SEO metadata support

## 1. Install

```bash
npm install
```

## 2. Create environment file

Copy `.env.example` to `.env` and change `AUTH_SECRET` and `ADMIN_PASSWORD`.

```bash
cp .env.example .env
```

On Windows PowerShell:

```powershell
Copy-Item .env.example .env
```

## 3. Create the database

```bash
npm run db:push
npm run seed
```

## 4. Start the website

```bash
npm run dev
```

Open:

- Public website: `http://localhost:3000`
- Admin panel: `http://localhost:3000/admin/login`

Use the `ADMIN_EMAIL` and `ADMIN_PASSWORD` values from `.env`.

## Uploads

Development uploads are stored in `public/uploads`. For production deployments on serverless hosting, replace local file storage with Cloudinary, Amazon S3 or another persistent object-storage service.

## Database

The included project uses SQLite so it runs immediately. To use PostgreSQL:

1. Change the Prisma datasource provider from `sqlite` to `postgresql`.
2. Set `DATABASE_URL` to the PostgreSQL connection string.
3. Run `npm run db:push`.
4. Run `npm run seed`.

## Production checklist

- Use a long random `AUTH_SECRET`.
- Change the admin password.
- Use PostgreSQL.
- Use Cloudinary or S3 for uploads.
- Add login rate limiting.
- Add CAPTCHA to the contact form.
- Configure automated database backups.
- Run `npm run build` before deployment.

## Main folders

- `app/` — frontend pages and backend API routes
- `components/` — reusable public and admin UI
- `lib/` — authentication, database and utilities
- `prisma/` — database schema and seed
- `public/uploads/` — local development uploads

## One-click Render configuration

The project now includes `render.yaml`, `scripts/render-start.sh`, and `DEPLOY-RENDER.md`. Upload the project to GitHub and create a Render Blueprint from that repository. Render will prompt for the private administrator values and create the persistent disk automatically.
