# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.4.1] - 2026-04-10

### Added

- Global `showTimestamp` configuration on `GooeyToaster` to enable/disable timestamps for all toasts by default
- Per-toast `showTimestamp` override still available to prioritize specific notifications

## [0.4.0] - 2026-03-29

### Added

- Close button with configurable position (`top-left` / `top-right`) via `closeButton` prop on `GooeyToaster`
- Close button inherits toast border/fill styling; uses shadow when no border is set
- Close button visible on hover, touch, and keyboard focus with scale animation
- Dark mode support for close button with light glow shadow
- Optional `showTimestamp` prop to show/hide timestamp on individual toasts (default `true`)
- Backward-compatible export aliases for v0.2.x users (`GoeyToaster`, `goeyToast`, etc.)

### Fixed

- ESM export broken in v0.3.0 — rebuilt exports to reference correct renamed variables
- Center toast positioning on mobile viewports (≤600px)
- Toast header stretching full width due to `display: flex` regression — restored `inline-flex`
- Swipe-to-dismiss now works for compact (no-description) toasts — `toastId` always passed
- Close button position correctly mirrors for right-side and center toast positions

## [0.1.0] - 2026-02

### Added

- Organic blob morph animation (pill to blob and back)
- Five toast types: default, success, error, warning, info
- Description body with string or ReactNode support
- Timestamp display on toast UI with optional `showTimestamp` toggle

- Action button with optional success label morph-back
- Promise toasts with loading to success/error transitions
- Configurable timing: expand delay, morph duration, collapse, display
- Position support: top-left, top-right, bottom-left, bottom-right
- Right-side positions auto-mirror the blob horizontally
- Pre-dismiss collapse animation (blob shrinks to pill before exit)
- Custom fill color, border color, and border width
- CSS class overrides via classNames prop
- Built on Sonner and Framer Motion
