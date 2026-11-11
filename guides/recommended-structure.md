# Recommended Repository Structure

```text
project-name/
├── client/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   └── App.jsx
│   ├── .env.example
│   └── package.json
├── server/
│   ├── src/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── middleware/
│   │   └── app.js
│   ├── .env.example
│   └── package.json
├── AI-USE.md
├── README.md
└── .gitignore
```

This structure is a recommendation, not a mandatory architecture. Keep the project small and organize files by clear responsibility. Do not create additional layers unless they improve readability.
