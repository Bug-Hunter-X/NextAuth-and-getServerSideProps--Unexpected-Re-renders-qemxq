# NextAuth and getServerSideProps: Unexpected Re-renders

This repository demonstrates a bug encountered when using NextAuth.js's `unstable_getServerSession` within a page's `getServerSideProps` function. The About page unexpectedly re-renders multiple times after the initial load, even if the session status doesn't change.

## Bug Description
The issue is observed with Next.js 13 and NextAuth.js. The About page, fetching session data via `getServerSideProps` and `unstable_getServerSession`, continuously re-renders, consuming unnecessary resources. This only happens after successful authentication and navigation to the About page. The issue doesn't appear when directly accessing the About page after a full page reload.