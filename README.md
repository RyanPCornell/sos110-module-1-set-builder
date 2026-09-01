# Module 1 SET Builder

A drag-and-drop sandbox for the SOS 110 Module 1 group assignment: map a biome as
a **socio-ecological-technical system** and export it as a one-page PDF.

**Live:** https://ryanpcornell.github.io/sos110-module-1-set-builder/

This is the same tool that appears as slide 4 of the
[Module 1 assignment deck](https://ryanpcornell.github.io/sos110-module-1-group-assignment/),
published on its own so students can bookmark just the tool and work outside class.

## What it does
- **Pick a biome** from the nine the assignment offers; choosing one seeds editable
  *dominant vegetation*, *precipitation* and *temperature* fields.
- **Build the system** by dragging in social, ecological, trophic and technical
  pieces — or a blank **Custom…** piece. Double-click anything to rename it, so a
  desert's "Producers" can read "Saguaro & creosote".
- **Two kinds of arrow.** Run the food chain up from producers to apex predators
  with ⚡ *energy flows to* arrows; wire everything else with **+** *amplifies* and
  **−** *dampens*. Energy arrows are a chain, not feedback, so they are excluded
  from loop detection on purpose.
- **See what you built** — the tool finds the reinforcing and balancing feedback
  loops as you draw, and **⚡ Shock the system** shows whether a small change runs
  away, oscillates, or is absorbed.
- **Write it up** — a sustainability lens (challenge or opportunity, why it
  matters, potential solutions), an explanation of the diagram, and a field to
  credit which specific parts were AI-assisted.
- **Save as PDF** — opens the browser's own print dialog; choose "Save as PDF".
  That sheet is the Canvas submission.

Two worked examples ship with it: **Coral reef & fishing town** (a full food chain
wired into a fishing town, with a reinforcing price spiral racing a balancing
survey-and-quota loop), plus **Managed fishery** and **Fast fashion**.

## Under the hood
One HTML file, no build step, no dependencies, no backend — nothing is uploaded
and nothing is stored. The only external requests are Google Fonts.

Built from `_deck-builder/module1_set_builder.py` (shared with slide 4 of the
deck, so the two can never drift) via
`_deck-builder/module1_set_builder_standalone.py`:

    python3 module1_set_builder_standalone.py
