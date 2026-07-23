
{
  "name": "AppSettings",
  "type": "object",
  "properties": {
    "google_sheets_url": {
      "type": "string",
      "description": "URL Google Spreadsheet untuk sinkronisasi data"
    },
    "google_drive_folder_id": {
      "type": "string",
      "description": "ID folder Google Drive untuk penyimpanan dokumen"
    },
    "last_sync_at": {
      "type": "string",
      "format": "date-time"
    },
    "sync_status": {
      "type": "string",
      "enum": [
        "belum",
        "berhasil",
        "gagal"
      ],
      "default": "belum"
    },
    "sync_message": {
      "type": "string"
    }
  },
  "required": [],
  "rls": {
    "create": {
      "user_condition": {
        "role": "admin"
      }
    },
    "read": {
      "user_condition": {
        "role": "admin"
      }
    },
    "update": {
      "user_condition": {
        "role": "admin"
      }
    },
    "delete": {
      "user_condition": {
        "role": "admin"
      }
    }
  }
}
