# JXL Compression Guide

[🏠 Document Top](../index.md) | [⚖️ Terms of Service](./terms.md) | [🔒 Privacy Policy](./privacy.md)

---

VSA can store VRChat photos in reversible JPEG XL (JXL) format. It preserves image quality and metadata while reducing storage use, and selected photos can be restored to PNG.

## Automatic Archive

Open “JXL Compression” from the sidebar to configure automatic archiving.

- Choose an age threshold of 1, 2, 3, 4, 6, or 12 months.
- While VSA is running, it checks for eligible older PNG files once per day.
- Archives are stored in `VSA-Archive` under the current photo output folder. Changing the photo output folder also updates the archive destination.
- Photos organized by month are moved to reversible JXL storage with their metadata preserved.
- Opening an archived photo creates a temporary PNG for viewing without changing the archive itself.

The schedule time, file-count trigger, monitor interval, snooze, and VRChat-state pause settings from older versions are no longer available.

## Archive Manager

Use the folder tree and status tabs to review archived photos.

- **Archived**: Photos currently stored as JXL.
- **Restored**: Photos restored to PNG. They can be compressed again when needed.
- **Problems**: Photos whose restore, verification, or source-file cleanup failed. Review the cause and retry the available action.

If restoration or verification fails, VSA keeps the last verified source file. Do not manually delete it until the problem is resolved.

## Manual Compression

You can compress a folder of PNG files as one batch.

1. Open the “Manual Compression” tab.
2. Select the input and output folders.
3. Click “Start Compression.”
4. Follow the processed count, total count, and current file in the progress display.

Manual compression uses batch processing. The background processing mode from older versions is no longer available.

## Extracting JXL Files

1. Open the “Extract JXL” section.
2. Select a JXL file or folder.
3. Select the output folder.
4. Click “Start Extraction.”

The restored PNG retains the original metadata.

## Troubleshooting

### Automatic archiving is not progressing

1. Confirm automatic archiving is enabled and eligible photos are older than the selected threshold.
2. Confirm VSA can read and write the photo output folder and `VSA-Archive`, and check free disk space.
3. Open the archive manager’s Problems tab and retry the action shown there.

### Manual compression is not progressing

- Confirm the input folder contains PNG files.
- Check read permission for the input and write permission for the output.
- If the issue continues, restart VSA and retry.
