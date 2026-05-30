# Audit Logging - Enhanced

## Size Management
### Configuration
- **max_log_size_mb**: 10
- **auto_cleanup_on_overflow**: true
- **retention_days**: 30
- **compression**: true

### Log Structure
```
audit/
├── operations/
│   ├── {timestamp}-operation.json
│   ├── {timestamp}-risk-assessment.json
│   └── {timestamp}-rollback-plan.json
├── current/
│   └── latest-operation-link.lnk
├── archive/
│   ├── {date}/
│   └── compressed/
│       └── {date}.tar.gz
└── metadata/
    └── log-index.json
```

## Auto-Cleanup Trigger
When log size exceeds 10MB:
1. Compress oldest logs
2. Remove logs older than 30 days
3. Keep at least 100 recent operations
4. Create compressed archive
5. Update log index

## Audit Log Entry Template
```
AUDIT LOG ENTRY
==============
Timestamp: {timestamp}
Operation: {operation_type}
Triggered By: {rule_name}
User Request: {original_request}

Files Modified:
- File: {path}
  - Change Type: {add/modify/delete}
  - Lines Changed: {number}
  - Summary: {brief_description}
  - Before Hash: {hash}
  - After Hash: {hash}

Decision Rationale:
- Primary Rule: {rule_name}
- Secondary Rules: {list}
- Confidence Level: {high/medium/low}
- Blast Radius: {assessment}

Dependencies Affected:
- {dependency_1}: {impact}
- {dependency_2}: {impact}

Outcome: {success/failure/partial}
Error Details: {if applicable}
```