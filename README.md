# Kanban Task Board — README

## Overview

This project is a lightweight, single-page Kanban board. You can add tasks, choose their status (To Do, Doing, Done), and see them immediately on the board. Tasks are saved in your browser’s local storage, so they’re still there when you refresh the page or come back later. The design matches the provided Figma and adapts cleanly from desktop down to small phones.

## What you can do

- Open the “Add New Task” modal to create a task with a title, description, and status.
- See the task appear instantly in the correct column, with column counts updating automatically.
- Revisit the page and find your tasks preserved.
- Use the interface comfortably on both large screens and very small phones.

## How it works (behind the scenes, in simple terms)

- The app saves your tasks to the browser’s local storage under a single key.
- When the page loads, it checks for saved tasks. If present, it loads them; if not, it starts with the provided sample tasks.
- Tasks keep a simple shape: an id, title, description, and one of three statuses.
- Rendering groups tasks into their matching column and updates the counts shown in each column header.
- The modal handles both creating and editing tasks while keeping the visual style consistent with the design.

## Design and responsiveness

- Desktop modal size and spacing include the follow: soft border, subtle shadow, and a centered “Create Task” button in a pill shape.
- On phones, the header title is replaced by the Kanban icon, and the “Add New Task” button becomes a compact circular “+”.
- The modal becomes fluid on small screens so text doesn’t spill, and user can scroll if needed.
- Typography uses Plus Jakarta Sans, with strong emphasis for key actions and labels.

## Accessibility and UX details

- Keyboard focus moves into the modal when it opens, so you can type immediately.
- Validation avoids harsh outlines. If a required field is empty, a small, readable red-accent tip appears above that field.
- Buttons maintain clear contrast and visible focus styles.

## Project layout at a glance

- A single HTML page defines the structure and the modal.
- A CSS file contains design tokens (colors, spacing), layout rules, modal styling, and responsive behavior.
- A JavaScript file handles storage, rendering, and modal interactions.
- A small seed file provides initial tasks the first time you run the app.

## Getting started

1. Download or clone the project files to your machine.
2. Open the project with any simple local web server (for example, a lightweight HTTP server or a “Live Server” extension in your editor).
3. Visit the local address it provides in your browser. The board will load with the seed tasks, and you can start adding your own.

Have fun 🚀
