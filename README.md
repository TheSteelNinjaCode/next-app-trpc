# next-app-trpc

This is `next-app-trpc`, a Node.js package designed to seamlessly integrate tRPC into existing Next.js projects. It offers a straightforward approach to implementing tRPC, ensuring compatibility with source code using import aliases or custom import aliases, all while being written in TypeScript.

## Description

`next-app-trpc` simplifies the integration of tRPC (TypeScript RPC) into Next.js applications. It's designed to offer a streamlined approach for developers looking to leverage tRPC's capabilities in their existing Next.js projects. The package addresses common challenges such as setting up tRPC clients and servers, managing API routes, and maintaining source code compatibility, especially when using import aliases or custom import aliases.

## Installation

This package is designed for use with `npx`, eliminating the need for global installation. Simply run the command below to use `next-app-trpc`:

```bash
npx next-app-trpc
```

## Dependency Installation

When you run `next-app-trpc`, the following dependencies are automatically installed, ensuring a seamless setup and integration:

- `@trpc/client`: For client-side tRPC communication.
- `@trpc/server`: For creating and managing the tRPC server.
- `@trpc/react-query`: To integrate tRPC with React Query.
- `@tanstack/react-query`: For fetching, caching, and updating data in React apps.
- `decimal.js`: Provides arbitrary-precision decimal arithmetic, useful for precise calculations.
- `superjson`: Extends JSON to support more data types, enhancing data transmission in tRPC applications.

## Project Structure

The typical project structure when using `next-app-trpc` in a Next.js application looks like this:

```bash
Next.JS
.
├── src
│   ├── app
│   │   ├── _trpc  # <-- add `withTRPC()`-HOC here
|   |   |   └── client.ts  # <-- tRPC client
|   |   |   └── TrpcProvider.tsx  # <-- tRPC provider
│   │   ├── api
│   │   │   └── trpc
│   │   │       └── [trpc]
|   |   |           └── route.ts  # <-- tRPC HTTP handler
│   │   └── [..]
│   ├── server
│   │   ├── routers
│   │   │   ├── user.ts  # <-- sub routers
│   │   │   ├── post.ts  # <-- sub routers
│   │   │   └── [..]
│   │   ├── index.ts  # <-- main router
│   │   └── trpc.ts      # <-- procedure helpers
│   └── [..]
└── [..]
```

## Contributing

Contributions to `next-app-trpc` are welcome. If you have any suggestions, bug reports, or pull requests, feel free to open an issue or submit a pull request on the repository.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
