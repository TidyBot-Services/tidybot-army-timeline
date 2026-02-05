# Activity Log Entries

Add your log entries to `entries.json`. The timeline will automatically load and display them.

## Entry Format

```json
{
  "timestamp": "2024-10-24 09:00",
  "type": "feature",
  "title": "Feature Name",
  "description": "Brief description of what was done.",
  "files": ["path/to/file.ts", "another/file.ts"]
}
```

## Fields

| Field | Required | Description |
|-------|----------|-------------|
| `timestamp` | Yes | Date and time in `YYYY-MM-DD HH:MM` format |
| `type` | Yes | One of: `setup`, `feature`, `fix`, `refactor`, `test`, `docs`, `deploy` |
| `title` | Yes | Short title for the entry |
| `description` | Yes | Brief description of what was accomplished |
| `files` | Yes | Array of file paths that were changed |

## Entry Types

- **setup** - Initial setup, configuration, environment
- **feature** - New functionality added
- **fix** - Bug fixes
- **refactor** - Code improvements without changing functionality
- **test** - Adding or updating tests
- **docs** - Documentation updates
- **deploy** - Deployment related activities

## Example

```json
[
  {
    "timestamp": "2024-10-24 09:00",
    "type": "setup",
    "title": "Repository Initialized",
    "description": "Created initial project structure.",
    "files": ["package.json", ".gitignore"]
  },
  {
    "timestamp": "2024-10-24 14:30",
    "type": "feature",
    "title": "User Authentication",
    "description": "Implemented JWT-based authentication system.",
    "files": ["src/auth/jwt.ts", "src/middleware/auth.ts"]
  }
]
```

## Notes

- Entries are displayed in the order they appear in the JSON file
- The timeline defaults to showing the last (newest) entry
- IDs are automatically generated based on array position
