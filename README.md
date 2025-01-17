# React Router v6 path="/*" Route Issue

This repository demonstrates a common issue encountered when using the `path="/*"` route in React Router v6. The catch-all route is intended to handle any unmatched paths, but it can unintentionally intercept other routes, leading to unexpected redirects to the 404 page.

The issue occurs when the catch-all route is placed before other routes.  React Router processes routes in order, and the `path="/*" ` route will always match before any subsequent routes.

The solution involves carefully ordering the routes, placing the catch-all route at the very end.