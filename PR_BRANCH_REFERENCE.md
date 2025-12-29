# Branch Reference

## Completed PRs

### PR #508 - Structured JSON Output (MERGED)
- Status: **MERGED** to upstream on Dec 12, 2025
- Feature: Added structured JSON output support for all providers

### PR #555 - Camera Entity Fix (MERGED)
- Status: **MERGED** to upstream v1.5.3-beta on Dec 12, 2025
- Feature: Fix TypeError when camera entity_picture is None or unavailable

## Archived Branches

### feature/min-frames-per-camera (ARCHIVED - Dec 29, 2025)
- **Feature**: Adds `min_frames_per_camera` parameter to `stream_analyzer` service
- **Purpose**: Guarantees minimum frame allocation per camera when using multiple cameras
- **Decision**: ARCHIVED - Not needed because:
  1. Original algorithm already includes first frame from each camera (guaranteed minimum)
  2. Remaining frames selected by best SSIM score across all cameras
  3. No observed imbalance problems in practice
  4. Adds ~100 lines of complexity for speculative benefit
- **Resurrection**: If camera imbalance becomes a real problem, this branch has a working implementation

### Old Phase Branches (STALE - Do not use)
- `feature/llm-vision-phase1` - Structured output (superseded by PR #508)
- `feature/llm-vision-phase2` - Old min_frames implementation (superseded by feature/min-frames-per-camera)
- `feature/llm-vision-combined` - Combined development branch
- `structured-output-*` branches - PR #508 work branches

## Current State
- `main` is synced with upstream/main
- All active development should branch from `main`
