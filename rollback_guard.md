# Rollback Guard - Enhanced

## Backup Management
### Storage Locations
- **Primary**: ./backups/{timestamp}/{operation_name}/
- **Secondary**: ./restraint_backups/{operation_hash}/
- **Archive**: ./archive/backups/{date}/

### Backup Structure
```
backup/
├── {timestamp}/
│   ├── original_files/
│   ├── metadata.json
│   └── rollback_script.sh
├── current/
│   └── latest_operation/
└── archive/
    └── {date}/
```

## Auto-Cleanup Rules
- **Immediate Cleanup**: After successful rollback
- **7-Day Retention**: For successful operations
- **30-Day Retention**: For failed operations
- **90-Day Archive**: For audit purposes
- **Size Limit**: Max 100MB total backup storage

## Cleanup Protocol
1. Check backup age and size
2. Remove backups older than retention period
3. Compress large backup directories
4. Log cleanup actions
5. Ensure at least one recent backup remains