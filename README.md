# Tailwind CSS Production Build Issue

This repository demonstrates a bug where Tailwind CSS classes fail to apply correctly in a production build, while working as expected during local development.

## Bug Description

Tailwind CSS classes are defined and function correctly during local development. However, after building the project for production (using a build process like Webpack or Vite), the classes are not applied, resulting in unexpected styling. 

## Reproduction Steps

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm run dev` to start the development server (this should work correctly).
4. Run `npm run build` to create a production build.
5. Serve the production build (e.g., using `serve -s build`) and observe that Tailwind classes are not applied.

## Potential Causes

* Incorrect build configuration: The build process might not be properly processing Tailwind CSS.
* PurgeCSS or similar issues:  A build optimization step (like PurgeCSS) might be removing unused CSS, even though it's necessary.
* Incorrect paths or imports:  The path to the Tailwind CSS files may be incorrect in the production build.