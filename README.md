# React Configs for VS Code

These are just some basic config settings that make working with React in VS Code super awesome.

Kudos to Thibaud Ducasse who shared this config here:

https://itnext.io/create-react-app-with-vs-code-1913321b48d

## Enabling SSL for localhost Development

Create React App uses Webpack-Dev-Server to host the development site locally. Internally it checks for the **HTTPS=true** environment variable (in the .env file in the project root). If this has been set, then the webpack-dev-server will launch using HTTPS, with a self signed certificate.

Chrome will complain that the certificate is not valid, in which case you can do one of the following:

- Enable a built in Chrome flag to ignore invalid certificates for localhost: chrome://flags/#allow-insecure-localhost
- Import the certificate to Trusted Root Certificate Store:
  1.  Run local dev server and visit the page with invalid certificate
  2.  Click the **Not Secure** warning next to the browser URL bar, then press **Certificate**
  3.  Click on the **Details** tab and then **Copy to File**
  4.  Selecty **Next** > **DER Encoded binary X.509 (.CER)** > **Next** > Select a location to save the certificate.
  5.  Continue with **Next** through the wizard to finish the export.
  6.  Open the newly saved **localhost.cer** file > **Install Certificate** > **Local Machine** > Place all certificates in the following store: **Trusted Root Certification Authorities** > Complete the import
  7.  Restart Chrome, and now when you visit https://localhost:3000, it should be using a valid certificate

## Popular React Tools

List of popular tools to use with React (so I dont forget!)

- **React Router**
- **Ramda** (Functional programming)
- **Lodash** (Utilities)
- **Glamorous** (maintainable CSS with React)
- **Styled Components** (CSS for React)
- **CSS Modules**
- **Gatsbyjs** (Static web site generator for React)
- **Next.js** (Server side rendering)
- **Material UI** (React Component UI based on Google Material)
- **Semantic UI** (React Component UI for)
- **Reselect** (Selectors and improving Redux performance)
- **Redux-Thunk** (Simple handling of Redux asynchronous actions)
- **Redux-Saga** (Handles Redux asynchronous actions)
- **Immutablejs** (Helps for enforcing immutable collections)
- **why-did-you-update** (Will list components in console which are updating perhaps unnecessarily)
