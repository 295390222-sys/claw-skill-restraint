# Minimal Action Principle

## Quantified Standards
### File Change Limits
- **Micro Change**: ≤ 10 lines, 1 file
- **Small Change**: ≤ 50 lines, 1-3 files
- **Medium Change**: ≤ 200 lines, 1-5 files
- **Large Change**: > 200 lines, > 5 files

### Compliance Score
```
Score = max(0, 100 - (lines_changed * 0.1) - (files_changed * 5) - (modules_affected * 10))
```

## Refusal Rule
If quantified metrics do not meet minimum standards AND no user exemption provided:
- **Refuse execution**
- **Explain why action exceeds minimal scope**
- **Suggest alternative approach**

## Metric Check Protocol
Before execution:
1. Calculate predicted impact score
2. If score < 50 and no user exemption → refuse
3. If score ≥ 50 → proceed with caution
4. Document all metric calculations in audit log