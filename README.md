# SVG Image Filter

A web application that applies halftone effects to images using client-side SVG filters. The app processes images in real-time with no server required, relying solely on the browser’s native capabilities.

## Features

- Real-time halftone filters: Two types of SVG filters (`half-tone` and `half-tone-hd`)
- Color customization: Color picker to adjust the tone of the effect
- Client-side processing: Everything runs directly in the browser
- Minimal interface: Simple controls for image upload, filter selection, and color adjustment

## Technologies

- Frontend: React 18.3.1 + TypeScript 5.5.3
- Build Tool: Vite 5.4.2 with HMR
- Styling: TailwindCSS 3.4.1 + PostCSS
- Icons: Lucide React 0.344.0
- Linting: ESLint 9.9.1 with TypeScript and React rules

## How It Works

The application uses advanced SVG filters to create halftone effects:

1. Luminance extraction: Converts the image to grayscale luminance values
2. Threshold mapping: Splits luminance into 8 discrete levels
3. Pattern generation: Applies circles of varying sizes based on luminance
4. Final composition: Combines all levels to render the halftone effect

### Filter Types

- `half-tone`: 8x8 pixel grid with circles ranging from 0.5 to 4.0 radius
- `half-tone-hd`: 4x4 pixel grid with circles ranging from 0.25 to 2.0 radius for higher detail

## Installation and Development

```bash
# Clone the repository
git clone https://github.com/Charlsz/SVG-image-filter.git
cd SVG-image-filter

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Run linting
npm run lint
```

## Project Structure

```
├── index.html          # Main application with embedded SVG filters
├── package.json        # Dependencies and scripts
├── vite.config.ts      # Vite configuration
├── eslint.config.js    # ESLint configuration
└── tailwind.config.js  # TailwindCSS configuration
```

## Configuration

### Vite
The Vite configuration excludes `lucide-react` from dependency optimization to improve performance.

### ESLint
Configured with TypeScript and React rules, including React Hooks and React Refresh support.

## Usage

1. Upload an image: Use the upload button to select an image from your device.
2. Select a filter: Choose between "None", "half-tone", or "half-tone-hd".
3. Customize color: Adjust the effect color using the color picker.
4. View the result: The image is processed in real time directly in the browser.

## Author

**Charlie**  
[Portfolio](https://charlsz.netlify.app/)  
[GitHub](https://github.com/Charlsz)
