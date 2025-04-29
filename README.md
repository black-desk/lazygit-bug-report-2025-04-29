# Lazygit Bug Reproduction

## Issue Description

This repository is used to
reproduce a bug in Lazygit related to
the custom patch application feature.

## Steps to Reproduce

1. Clone this repository:

   ```bash
   git clone https://github.com/black-desk/lazygit-bug-report-2025-04-29
   cd lazygit-bug-report-2025-04-29
   ```

2. Build a custom patch
   from changes to the `test.md` file in `HEAD^`.

3. Move the patch to a new commit.

**Expected Result:**
The patch should be applied successfully.

**Actual Result:**
Git fails to apply the patch.

## Issue Verification

Here's a simple example
to verify the issue in another way:

```bash
# Create a patch with zero context lines
git format-patch HEAD^ -U0

# Try to apply the patch in reverse
git apply --reverse *.patch
```

This will clearly demonstrate the patch application failure.
