# Fetch-Data-using-useFetch

A simple React project demonstrating how to fetch data using a custom `useFetch` hook. Built with [Vite](https://vitejs.dev/) and deployed on GitHub Pages.

## Features

- Custom React hook for fetching data from APIs
- Handles loading, error, and data states
- Clean and reusable code structure
- Fast development with Vite

## Demo website
https://hassan2-aamir.github.io/Fetch-Data-using-useFetch/

## Getting Started

### Prerequisites

- Node.js (v16 or higher recommended)
- npm

### Installation

1. Clone the repository:

   ```sh
   git clone https://github.com/hassan2-aamir/Fetch-Data-using-useFetch.git
   cd Fetch-Data-using-useFetch
   ```

2. Install dependencies:

   ```sh
   npm install
   ```

### Running Locally

Start the development server:

```sh
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

### Building for Production

```sh
npm run build
```

### Deploying to GitHub Pages

1. Set the correct `base` in `vite.config.js`:

   ```js
   export default defineConfig({
     // ...other config
     base: '/Fetch-Data-using-useFetch/'
   })
   ```

2. Deploy using your preferred method (e.g., [gh-pages](https://www.npmjs.com/package/gh-pages)).

## Project Structure

```
custom_hook/
├── public/
├── src/
│   ├── components/
│   ├── hooks/
│   │   └── useFetch.js
│   ├── App.jsx
│   └── main.jsx
├── vite.config.js
└── package.json
```

## Example Usage

```js
import useFetch from './hooks/useFetch';

function App() {
  const { data, loading, error } = useFetch('https://api.example.com/data');

  if (loading) return <p>Loading...</p>;
  if (error) return <p>Error: {error.message}</p>;

  return <pre>{JSON.stringify(data, null, 2)}</pre>;
}
```

## License

APACHE 2.0

---