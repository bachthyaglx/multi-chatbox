multi-chatbox
├── backend/
│   ├── package.json
│   ├── server.js                      // Express + Socket.IO + Apollo GraphQL Server
│   ├── redisClient.js
│   ├── graphql/
│   │   ├── schema.js                  // GraphQL schema (typeDefs + resolvers)
│   │   ├── resolvers/
│   │   │   ├── guest.js               // Guest mutations/queries
│   │   │   ├── admin.js               // Admin queries
│   ├── sockets/            
│   │   ├── index.js                   // Socket.IO events (guest/admin chat)
│   └── utils/
│       ├── sessionStore.js            // Redis logic
├── frontend/
│   ├── package.json
│   ├── next.config.js
│   ├── tsconfig.json
│   ├── pages/
│   │   ├── index.tsx                  // Guest chatbox → call GraphQL mutations
│   │   ├── admin.tsx                  // Admin login + panel → GraphQL query list guest
│   ├── components/
│   │   ├── GuestChatbox.tsx
│   │   ├── AdminPanel.tsx
│   │   ├── AdminChatbox.tsx
│   │   ├── Pagination.tsx
│   ├── utils/
│   │   ├── socket.ts                  // Socket.IO client
│   │   ├── apolloClient.ts            // Apollo client setup
├── README.md
