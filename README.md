# Frontity Builder

Deploy your [Frontity](https://frontity.org) project to Vercel with Node 20.

## Before deploying

1. Include the following settings in your projects `vercel.json` file:

```json
{
  "builds": [
    {
      "src": "package.json",
      "use": "@baalspots/frontity-builder"
    }
  ],
  "buildCommand": "node -v && npx frontity build && node -v",
  "devCommand": "npx frontity dev",
  "framework": null,
  "installCommand": "npm i",
  "outputDirectory": "build"
}
```

2. Update your Frontity projects local dev environment to use Node 20.

3. Update `package.json` at the root of your project to use the following Node engine and scripts:

```json
"engines": {
 "node": "20.x"
},
"scripts": {
 "dev": "npx frontity dev",
 "build": "node -v && npx frontity build && node -v",
 "serve": "npx frontity serve"
},
```

4. Remove all `package-lock.json` files and `node-modules` folders in your Frontity project.

5. Remove `package-lock.json` from your projects `.gitignore` file

6. Run `npm i` at the root of your project.
