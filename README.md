![zavy-icon](https://raw.githubusercontent.com/chingu-voyages/v41-bears-team-32/main/public/favicon.ico)

# Zavy - An ecommerce store

🚀 **Deploying at:** [https://zavy.netlify.app/](https://zavy.netlify.app/)  
⚠ **Status:** In development

Zavy is an ecommerce store in development by `v41-bears-team-32`.

## Local Development:

### Database Setup:

This project uses PostgreSQL as the database. The easiest way to install it is using docker. Enter the following command on your terminal if you already have docker installed. This will install and run the latest version of postgreSQL.

$ `docker run --name zavy -e POSTGRES_PASSWORD=password -p 5432:5432 -d --rm postgres`

### Project Setup

This project uses [pnpm](https://pnpm.io/) for managing dependancies. If you don't already have it installed, install it using `npm install -g pnpm` or choose other available methods [here](https://pnpm.io/installation) and then:

- `git clone` this repo & `cd v41-bears-team-32`
- `pnpm install`
- `pnpm exec prisma migrate dev` (_Will apply migrations, make sure database setup is completed_)
- `pnpm dev`

### Environment Variables:

`.env.example` file is present in the root directory of project and includes all required envirnoment variables. Following values will get you started:

```
# NEXTAUTH_SECRET can be generated using "openssl rand -base64 32"

DATABASE_URL=postgresql://postgres:password@localhost:5432/postgres
GOOGLE_CLIENT_SECRET=<client-secret>
GOOGLE_CLIENT_ID=<client-id>
FACEBOOK_CLIENT_SECRET=<fb-client-secret>
FACEBOOK_CLIENT_ID=<fb-client-id>
NEXTAUTH_URL=http://localhost:3000/
NEXTAUTH_SECRET=VJ13WCJAjH1SNoLpvUUIWhvk9+cEfsnOMnjssSsvzJQ=
NEXTAUTH_LOGIN=http://localhost:3000/api/login
NEXTAUTH_SIGNUP=http://localhost:3000/api/signup
CURRENT_ENV=dev
```
