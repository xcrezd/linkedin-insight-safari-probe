# LinkedIn Insight Tag Safari probe

Public, noindex HTTPS landing page for a synthetic Safari 27 experiment.

- Uses production `insight.min.js` with test PID `102`.
- Does not trigger a conversion.
- Generates synthetic UUID values in the browser.
- Displays and persists only presence/match booleans, not identifier values.
- Deletes only `li_fat_id` and `li_giant` cookies across their valid host/domain and path variants on the test origin before tag injection.
- Refuses to load the Insight Tag if either stale test cookie remains after cleanup.
- Does not store request headers, cookies, HAR data, authorization data, or other visitor information.

The page itself sends a normal Insight Tag page-view request to LinkedIn when opened with all four synthetic test parameters.
