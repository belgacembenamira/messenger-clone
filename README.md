

## :bangbang: Folder Structure

Here is the folder structure of this app.

```bash
messenger-clone/
  |- app/
    |-- (site)/
        |--- components/
        |--- page.tsx
    |-- actions/
        |--- get-conversation-by-id.ts
        |--- get-conversation.ts
        |--- get-current-user.ts
        |--- get-messages.ts
        |--- get-session.ts
        |--- get-users.ts
    |-- api/
        |--- auth/[...nextauth]
        |--- conversations/[conversationId]
        |--- messages/
        |--- pusher/
        |--- register/
        |--- settings/
    |-- components/
        |--- inputs/
        |--- modals/
        |--- sidebar/
        |--- active-status.tsx
        |--- avatar-group.tsx
        |--- avatar.tsx
        |--- button.tsx
        |--- empty-state.tsx
        |--- loading-modal.tsx
    |-- config/
        |--- authOptions.tsx
        |--- site.ts
    |-- context/
        |--- auth-context.ts
        |--- toaster-context.ts
    |-- conversations/
        |--- [conversationId]/
            |---- components/
        |--- components/
        |--- layout.tsx
        |--- loading.tsx
        |--- page.tsx
    |-- hooks/
        |--- use-active-channel.tsx
        |--- use-active-list.tsx
        |--- use-conversation.tsx
        |--- use-other-user.tsx
        |--- use-routes.tsx
    |-- libs/
        |--- prismadb.ts
        |--- pusher.ts
    |-- types/
        |--- index.ts
    |-- users/
        |--- components/
        |--- layout.tsx
        |--- loading.tsx
        |--- page.tsx
    |-- favicon.ico
    |-- globals.css
    |-- layout.tsx
  |- prisma/
    |-- schema.prisma
  |- public/
    |-- images/
        |--- logo.png
        |--- placeholder.jpg
  |- .env
  |- .env.example
  |- .eslintrc.json
  |- .gitignore
  |- middleware.ts
  |- next.config.js
  |- package-lock.json
  |- package.json
  |- postcss.config.js
  |- tailwind.config.ts
  |- tsconfig.json
```

<br />

## :toolbox: Getting Started

1. Make sure **Git** and **NodeJS** is installed.
2. Clone this repository to your local computer.
3. Create `.env` file in root directory.
4. Contents of `.env`:

```bash
# .env

# mongodb url
DATABASE_URL="mongodb://127.0.0.1/messenger-clone"

# client url for next auth
NEXTAUTH_URL=http://localhost:3000

# next auth secret (random strings)
NEXTAUTH_SECRET=<your-nextauth-secret>

# next cloudinary credentials
NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME=xxxxxxxxx
NEXT_PUBLIC_CLOUDINARY_CLOUD_PRESET=xxxxxxxxxx

# pusher credentials
PUSHER_APP_ID=00000000
PUSHER_APP_SECRET=xxxxxxxxxxxxxxxxxxxxxx
NEXT_PUBLIC_PUSHER_APP_KEY=xxxxxxxxxxxxxxxxxxxxx
NEXT_PUBLIC_PUSHER_APP_CLUSTER=xxx

```

5. **MongoDB URL**

   - Install and run MongoDB locally or use a cloud-based MongoDB service.
   - Replace the placeholder in `DATABASE_URL` with your actual MongoDB connection string.

6. **NextAuth Configuration**

   - Set up NextAuth by following the official documentation: [NextAuth.js Documentation](https://next-auth.js.org/getting-started/introduction)
   - Set `NEXTAUTH_URL` to the base URL of your application.
   - Generate a random string for `NEXTAUTH_SECRET`.
