Quick setup

This project uses `bun` but you can use package manager of your preference (tested with `npm` and `yarn`)

Run these commands:

- `bun install`
- `bun run dev`

Q: How is authored CSS transformed into final CSS in the browser?

A: While browser is constructing DOM of a page it encounters a `<link>` element in the `<head>` of the document referencing CSS style sheet e.g. `layout.css`. Browser then sends a request for this recource which returns CSS content.  
The CSS bytes are converted into characters, then tokens, then nodes. Final step is linking them into a tree structure called CSSOM (CSS Object Model)  
Browser goes from top to the bottom. First it applies all styles from body to its children. After it evaluates styles of children it updates styles accordingly e.g. child div will have different color than the one body specified.


Q: Where to find the generated CSS and corresponding source maps in this project?

A: Generated CSS and corresponding source maps can be found by temporarily commenting out `/.svelte-kit` and `.vercel`. Then by searching all files with `a.svelte` you will get something like this `a.svelte-1uha8ag{color:#fff}`.  
For corresponding source maps search for files ending with `.map`.
