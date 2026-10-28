# CodeWall

A classroom code-sharing wall hosted on GitHub Pages with Firebase Authentication and Cloud Firestore.

## Publish on GitHub Pages
1. Upload `index.html` to the root of the `CodeWall` repository.
2. Commit the change to the `main` branch.
3. In repository Settings → Pages, choose Deploy from a branch, `main`, `/(root)`.
4. Open `https://venomawit0.github.io/CodeWall/` after deployment finishes.

## Firebase requirements
- Firebase web app config is in `index.html`.
- Firestore collection: `posts`.
- Firebase Authentication: Email/Password enabled.
- Firestore rules must allow public reads, validate creates, and restrict updates/deletes to the owner UID configured in the rules and HTML.

## Important security note
The shared classroom password in this static frontend is only a convenience prompt and can be discovered or bypassed. Anyone can create posts if Firestore rules allow unauthenticated creates. Do not use this approach for sensitive data or if posting must be restricted. Owner update/delete permissions are enforced by Firestore rules.

This site uses Firebase's browser SDK via CDN and Highlight.js via CDN; it needs an internet connection.
