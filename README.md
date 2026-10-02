# Certifyd AR Registry

This repository is the public Certifyd AR registry.

Records stored here are signed by authorized Certifyd AR creator devices. GitHub is used only as public storage and transport for those signed records.

Consumers must independently verify registry records against the creator's Certifyd Core node before trusting or displaying them. Registry contents alone are not proof of creator identity.

Record files use this path convention:

```text
records/<creator-handle>/<provider>/<account>.json
```

Example:

```text
records/beatify-group/spotify/1pKR6nU0QhMlbouug8OPtD.json
```

The registry index uses this shape:

```json
{
  "version": 1,
  "updatedAt": "ISO-8601 timestamp or null",
  "records": {
    "<creator-profile-url>": {
      "<provider>": {
        "<account>": {
          "recordUrl": "records/<creator>/<provider>/<account>.json"
        }
      }
    }
  }
}
```
