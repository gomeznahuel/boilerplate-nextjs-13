## How to create a Next.js project with TypeScript

Create a package.json file in the root of your project.

```shell
{
  "scripts": {
    "dev": "next",
    "build": "next build"
  },
  "dependencies": {
    "next": "^13.1.1",
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
  }
}
```

Create a pages directory in the root of your project and add an index.tsx file inside it.

`./pages/index.tsx`

```shell
export default function Page () {
  return <h1>Hello, World!</h1>
}
```

Create a `tsconfig.json` file in the root of your project.

Install the TypeScript compiler.

```shell
npm install --save-dev typescript @types/react @types/node
```

Execute the following command to start the development server and open `http://localhost:3000` in your browser.

```shell
npm run dev
```

The file `tsconfig.json` will be completed with the following content and the file `next-env.d.ts` will be created.

`./tsconfig.json`

```shell
{
  "compilerOptions": {
    "target": "es5",
    "lib": ["dom", "dom.iterable", "esnext"],
    "allowJs": true,
    "skipLibCheck": true,
    "strict": false,
    "forceConsistentCasingInFileNames": true,
    "noEmit": true,
    "incremental": true,
    "esModuleInterop": true,
    "module": "esnext",
    "moduleResolution": "node",
    "resolveJsonModule": true,
    "isolatedModules": true,
    "jsx": "preserve"
  },
  "include": ["next-env.d.ts", "**/*.ts", "**/*.tsx"],
  "exclude": ["node_modules"]
}
```

For build the project, execute the following command.

```shell
npm run build
```

Thanks for reading! If you have any questions, please leave a comment below.

### Author 
[Nahuel Gómez](https://www.nahue.dev)