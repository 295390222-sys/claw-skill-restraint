# Auto-Rollback - User Feedback Based

## Failure Detection Triggers
### User Feedback Based
- User reports: "failed", "doesn't work", "broken"
- User indicates test failures: "tests failed", "unit tests failing"
- User reports errors: "error", "exception", "crash"

### System Monitoring (if available)
- Build process failures
- Test suite failures
- Critical service unresponsiveness

## Rollback Protocol
1. **User Feedback Detection**
   - Scan conversation for failure indicators
   - Ask for confirmation if unclear
   - "Do you want me to rollback the changes?"

2. **Rollback Execution**
   - Restore from latest backup
   - Verify restoration success
   - Log rollback details

3. **Post-Rollback**
   - Inform user of rollback completion
   - Ask for further guidance
   - Pause further modifications until clarification

## Rollback Methods
- **File Restore**: Replace modified files with backups
- **Git Revert**: Use git revert if available
- **Database Rollback**: Rollback database transactions