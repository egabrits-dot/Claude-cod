# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

A single-page Russian-language todo app (`index.html`). No build step, no dependencies — open directly in a browser.

## Structure

- `index.html` — all markup, styles (inline `<style>`), and logic (inline `<script>`) in one file
- `css/` — empty folder, reserved for extracted styles if the project grows

## Architecture notes

State is ephemeral (DOM only, no localStorage). Tasks are created and removed via direct DOM manipulation in `addTask()` and the per-item delete handler. `updateEmpty()` toggles the empty-state message based on `list.children.length`.
