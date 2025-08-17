# How to create application with Hono

## Required
- Hono  `npm install hono`
- Hono Server `npm install @hono/node-server`

## Create application
### Create folder
```bash
mkdir src
```
### Create app instance from `Hono`
```bash
nano src/app.ts
```
```bash
import { Hono } from "hono";

const app = new Hono();

app.get("/", (c) => c.text("Hello World"));

export default app;
```
### Create server instance from `Hono Server`
```bash
nano src/server.ts | code src/server.ts
```
```bash
import { serve } from "@hono/node-server";
import app from "./app";

serve(app, (info) => {
  console.log("Running server on port", info.port);
});
```
