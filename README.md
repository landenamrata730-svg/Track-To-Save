# Track2Save

Track2Save is a multi-role ambulance booking and live tracking web application built with HTML, CSS, JavaScript, Firebase Authentication, Firestore, and Leaflet with OpenStreetMap.

## Included screens

- Home page
- Login and registration
- Patient dashboard
- Driver dashboard
- Hospital dashboard
- Admin dashboard
- Book ambulance
- Live tracking
- Emergency tracking ID lookup
- Profile
- Forgot password

## Live Firebase setup

Firebase is already wired in `assets/js/firebase-config.js` with your project:

- Project ID: `track-to-save`
- Auth domain: `track-to-save.firebaseapp.com`

Enable these services in Firebase Console:

- Authentication with Email/Password
- Cloud Firestore

Recommended Firestore collections:

- `users`
- `emergencies`

## Running locally

1. Start a static server from the project folder.
2. Open `index.html`.
3. Register your role-based accounts from the login page or seed Firebase using `firebase-seed-data.txt`.

Examples:

- `python3 -m http.server 8000`
- `npx serve .`
- VS Code Live Server

## Notes

- Authentication, users, and emergency trips are stored in Firebase.
- Driver position updates aim for high-accuracy GPS and fall back to simulation only if device location is unavailable.
- Booking uses GPS-first pickup capture, and the patient can refine the pickup pin directly on the map.
- Route drawing prefers live road geometry from OSRM and falls back to simulated routing if the route service is unavailable.
- Family members can track trips through `live-tracking.html?trackingId=12345`.

## Suggested next step

- Add Firestore security rules for role-based access.
