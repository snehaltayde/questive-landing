# Tailwind CSS Boilerplate

This project provides a quick start boilerplate for using Tailwind CSS with minimal setup. Tailwind CSS is a utility-first CSS framework for rapidly building custom designs directly in your markup.

## Prerequisites

- Node.js (recommended latest version)
- npm (Node Package Manager)

## Installation

To use this boilerplate, you need to install the Tailwind CSS CLI. Below are the installation steps specific to macOS ARM64 architecture. Visit [Tailwind CSS Standalone CLI](https://tailwindcss.com/blog/standalone-cli) for other architectures.

### macOS ARM64 Setup

1. **Download the CLI**:

   ```bash
   curl -sLO https://github.com/tailwindlabs/tailwindcss/releases/latest/download/tailwindcss-macos-arm64
   ```

2. **Make the binary executable**:

   ```bash
   chmod +x tailwindcss-macos-arm64
   ```

3. **Rename the binary** (optional):

   ```bash
   mv tailwindcss-macos-arm64 tailwindcss
   ```

### Configuration File

Create a `tailwind.config.js` file to configure your project settings:

```bash
./tailwindcss init
```

The generated file will include necessary configurations to use Tailwind CSS effectively in your project.

## Usage

### Development

Start the Tailwind CSS watcher to automatically compile changes made to your CSS during development:

```bash
./tailwindcss -i ./src/input.css -o ./src/output.css --watch
```

### Production

For production, compile and minify your CSS:

```bash
./tailwindcss -i ./src/input.css -o ./src/output.css --minify
```

## Tailwind Configuration (`tailwind.config.js`)

Here is a basic example of what your `tailwind.config.js` file might look like:

```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ['./src/**/*.{html,js}'],
  theme: {
    extend: {},
  },
  plugins: [require('@tailwindcss/forms'), require('@tailwindcss/typography')],
};
```

This configuration enables the Tailwind CSS forms and typography plugins and extends the default theme based on your project needs.

## Contributing

Contributions are welcome! Feel free to open a pull request or an issue if you have suggestions or find a bug.

## License

This project is open source and available under the [MIT License](LICENSE.md).
