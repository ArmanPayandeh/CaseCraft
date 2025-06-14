# CaseCraft - A Modern Fullstack E-Commerce Shop for Custom Phone Cases

Built with the Next.js 14 App Router, Postgres, TypeScript, Tailwind & Kinde Auth

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Features

- 🛠️ Complete SaaS built in modern Next.js
- 💻 Beautiful landing page included
- 🎨 Custom artworks made by a professional illustrator
- ✉️ Real-time event messages via Discord
- 🖥️ Clean & intuitive event monitoring dashboard
- 💳 Secure payments using Stripe
- 🛍️ Customers can purchase your PRO plan
- 🌟 Clean, modern UI on top of shadcn-ui
- 🔑 Authentication using Clerk
- ⌨️ 100% written in TypeScript
- 🎁 ...much more


## Getting Started

### Prerequisites
- Node.js 18+
- Stripe account
- Kinde account
- Neon account
- Resend account
- Uploadthing account

### Installation
```bash
git clone https://github.com/ArmanPayandeh/CaseCraft.git
cd CaseCraft
cp .env.example .env
```

Configure required environment variables in `.env`:
```env
# Retrieved from our auth provider Kinde
KINDE_CLIENT_ID=
KINDE_CLIENT_SECRET=
KINDE_ISSUER_URL=https://<your-kinde-app>.kinde.com
KINDE_SITE_URL=http://localhost:3000
KINDE_POST_LOGOUT_REDIRECT_URL=http://localhost:3000
KINDE_POST_LOGIN_REDIRECT_URL=http://localhost:3000/

NEXT_PUBLIC_SERVER_URL=http://localhost:3000

# Retrieved from our payment provider stripe
STRIPE_SECRET_KEY=
STRIPE_WEBHOOK_SECRET=

# Retrieved from file uploading service uploadthing
UPLOADTHING_SECRET=
UPLOADTHING_APP_ID=

# Retrieved from our hosted database at neon.tech
DATABASE_URL=

# (optional) Your email to access the secret admin dashboard
ADMIN_EMAIL=

# (optional) Retrieved from email sending service resend
RESEND_API_KEY=
```

Install dependencies and setup database:
```bash
npm install
npm run dev
npx prisma migrate dev --name "init"

```
```bash
yarn install
yarn dev
npx prisma migrate dev --name "init"
```
## Deployment


### Deployment Options
1. **Vercel** (Recommended):
   ```bash
   vercel deploy --prod
   ```
2. **Docker Container**:
   ```dockerfile
   FROM node:18-alpine
   WORKDIR /app
   COPY . .
   RUN npm ci --only=production
   CMD ["npm", "start"]
   ```

## Support & Troubleshooting

### Getting Help
- 🐛 [Open a GitHub Issue](https://github.com/ArmanPayandeh/CaseCraft/issues)
- 📧 Enterprise Support: arman.payandeh.2025@gmail.com


## License
Distributed under the MIT License. See `LICENSE` for more information.

## Acknowledgements
- Authentication by [Kinde](https://kinde.com)
- Authentication by [Neon](https://neon.com/)
- Payment processing by [Stripe](https://stripe.com)
- UI components from [shadcn/ui](https://ui.shadcn.com)
- Illustrations by [Undraw](https://undraw.co)
- Authentication by [Uploadthing](https://uploadthing.com)
- Authentication by [Resend](https://resend.com)
