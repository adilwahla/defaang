# defaang.io

A website that will curate recently-asked interview questions from FAANG+ to help people practice &amp; prep!

The questions will be submitted anonymously, or at least semi-anonymously. We'll ensure that no matter who submits them, we won't reveal the usernames, emails or any other personal info unless they explicitly choose to do so.

## Demo

https://defaang.io/

![image](https://user-images.githubusercontent.com/48839911/196244948-dbf9c375-c0e8-4165-ba20-224746149d3c.png)
![image](https://user-images.githubusercontent.com/1811651/190091032-73164fed-e5d9-4614-a2a1-2c2d144ebbaa.png)

## How to start frontend (Next.js + Tailwind CSS)

Make sure you have [git](https://git-scm.com/) and [npm](https://docs.npmjs.com/cli/init) installed in your local machine.

The repository has a `.vscode` folder that contains `settings.json` and `extensions.json`. The `settings.json` file configures your VS Code editor to use `eslint` and `prettier` on every code save action (`ctrl + s`). The `extension.json` file contains a list of VS Code extensions, VS Code will show these extensions as suggestions in the extensions tab. After installing these extensions, auto linting and formatting should start working.

### Steps:

1. Clone this repo

   ```sh
   git clone https://github.com/ykdojo/defaang.git
   ```

2. Go into the project root directory

   ```sh
   cd defaang
   ```

3. Install all the dependencies

   ```sh
   npm install
   ```

4. Start the application development server

   ```sh
   npm run dev
   ```

## How to deploy the application to Vercel

1. Ensure you have a vercel account. If not, sign up for one [here](https://vercel.com/).

2. Import the project into vercel.

3. Give vercel the nessecary permissions, deploy the projects and voila the deployment is done.

## How to set up Supabase

1. Sign up on Supabase [here](https://supabase.com/).

2. Create a new Project inside Supabase.

3. Go to `Settings` -> `API` and copy the Project `URL` and `anon`.

4. Create a new file named `.env.local` in the root directory.

5. Paste the `URL` and `annon` in the `.env.local` file like so:

```
NEXT_PUBLIC_SUPABASE_URL=YOUR_SUPABASE_URL
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_SUPABASE_ANON_KEY
```

6. Go to the [SQL Editor](https://app.supabase.com/project/_/sql) tab inside the Supabase dashboard.

7. Copy the SQL queries from [here](supabase.sql) and paste them in the SQL Editor.

8. Run the queries and you're done.

For more reference, read the [Next Quickstart for Supabase](https://supabase.com/docs/guides/with-nextjs)

Alternatively, you can immediately open the workspace on Gitpod by clicking the button below:

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/ykdojo/defaang)

## Contributing

After you have installed defaang on your local machine, head over to our [CONTRIBUTING.md](https://github.com/ykdojo/defaang/blob/main/CONTRIBUTING.md) guide to assist with all you need to know before getting started with making changes to the codebase.

## Discord

Join us [here](https://discord.gg/nNtVfKddDD).

## Streaming

I (YK) stream almost every day showing my progress on this project on Twitch [here](https://twitch.tv/ykdojo).
