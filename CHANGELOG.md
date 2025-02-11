1.0.0
Introduced a Flutter package that leverages json_dynamic_widget to dynamically render pages from JSON data. The package fetches all pages from a server when the app launches and provides a function to get a specific page by its name while caching the fetched data using SharedPreferences.
Included required API response format for consistency.
Added RenderPage widget to dynamically render JSON data with support for loading indicators and error handling.
Implemented a versioning system to minimize unnecessary API requests by checking versionConfig.json before fetching pages, comparing local and server versions.
Updated Express API route for serving versionConfig.json.
Optimized caching using SharedPreferences to store versioning data and page responses.
Added support for version-mapping based on appVersion, enhancing versioning flow using a version-mapping endpoint to fetch version-specific folder names for page retrieval.
Updated API routes to fetch pages based on folder names tied to app versions, improving scalability through folder-based page fetching.
Optimized JSON parsing and caching logic for large datasets.
Bug fixes:
Resolved conflicts caused by multiple registry creation.
Fixed issue in fetching pages from the cache.
Allowed x.x.x versioning format in versionConfig.json.
Fixed issue in fetching version-mapping on some servers.
Addressed an issue where pages failed to fetch when no local versioning was available.