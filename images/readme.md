# DisketteBox images

This folder contains screenshots, diagnostic captures, and photographs used by the DisketteBox documentation.

**Images here are evidence, not decoration.** Each one should answer at least one practical question:

- What does the application do?
- What hardware was tested?
- How was the device connected?
- What result did the test produce?
- What does a successful or failed operation look like?

## Current image

### `usb-floppy-track-read-1440k.png`

XX

Standalone SPTI validation against an SMSC-based Samsung `USB FDC`.

The capture records:

- 1.44 MB geometry detected through `READ CAPACITY(10)`
- 1,474,560 bytes read in 64,766 ms
- 160 track reads attempted
- 160 track reads successful
- No sector fallback
- All 2,880 sectors read cleanly on the first attempt
- The generated raw image path

This is the first documented proof that the track-batched reader is functioning on real hardware.

## Suggested image set

These filenames are recommendations so the root README and future documentation can remain stable.

| Filename | What it should show |
| --- | --- |
| `diskettebox-main-window.png` | Main application window with a real multi-disk set selected |
| `diskettebox-set-catalog.png` | Set metadata, disk order, labels, and verification fields |
| `diskettebox-mounted-image-explorer.png` | A raw image mounted through the VHD path and opened in Explorer |
| `sfd-321u-usb-fdc-setup.jpg` | Samsung/SMSC USB floppy drive, cable, disk, and host connection |
| `dell-multibay-usb-fdd-side-port.jpg` | Dell MultiBay FDD and the external USB port that permits standalone use |
| `usb-floppy-track-read-1440k.png` | Successful 1.44 MB track-batched read |
| `usb-floppy-fallback-report.png` | A weak or deliberately damaged disk exercising sector fallback |
| `usb-floppy-write-verify-pass.png` | Disposable disk completing write and full readback verification |
| `usb-floppy-transport-abort.png` | A disconnect or fatal transport failure being aborted safely |
| `diskettebox-vhd-lifecycle.png` | Image wrapped, attached read-only, assigned a drive letter, and detached |

## Capture guidelines

### Screenshots

- Use PNG.
- Capture the complete result needed to understand the operation.
- Keep command lines, device identifiers, geometry, elapsed time, and final status visible.
- Crop unrelated desktop space, but do not crop away evidence.
- Remove personal paths, usernames, serial numbers, or unrelated devices when they do not add technical value.
- Do not resize text until it becomes difficult to read.
- Prefer one decisive screenshot over several nearly identical captures.

### Hardware photographs

- Use JPG for ordinary device photos and PNG only when lossless detail is important.
- Photograph the complete device before close-ups.
- Include the connector, cable, adapter, and drive label when they establish compatibility.
- Add a close-up of unusual features, such as the Dell MultiBay side USB port.
- Use a plain background and enough light to read labels without flash glare.
- Show temporary wiring honestly; do not stage a cleaner configuration that was not used for the test.

## Naming

Use lowercase descriptive filenames with hyphens:

```text
device-or-feature-result.ext
```

Examples:

```text
sfd-321u-usb-fdc-setup.jpg
dell-multibay-usb-fdd-side-port.jpg
usb-floppy-track-read-1440k.png
diskettebox-mounted-image-explorer.png
```

Avoid names such as:

```text
Screenshot 2026-07-20.png
IMG_4821.jpg
final-final-2.png
```

## Documentation rule

A screenshot should not merely claim that something works. Its caption should explain what the reader can verify in the image.

A hardware photograph should not merely prove that a device exists. Its caption should identify the relevant controller, connector, modification, or test arrangement.

When an image represents an early or hardware-specific result, say so directly.
