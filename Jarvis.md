# JARVIS --- Tony Stark's Personal AI Assistant

## Objective

Tony Stark has a lot on his plate.

Between designing new technology, managing meetings, keeping track of
important tasks, communicating with his team, and maintaining a growing
collection of research documents, Tony needs something that can keep
everything organised without slowing him down.

That's where **JARVIS** comes in.

Your mission is to build a **web-based personal AI assistant inspired by
JARVIS from the Avengers**, capable of understanding Tony's requests and
performing useful actions through a single, polished interface.

The application should not feel like a collection of unrelated features.
Each capability should build on the previous one, gradually turning a
simple assistant into a useful personal command centre.

The overall experience should follow a **Doomsday-themed Stark
interface** --- futuristic, intelligent, and inspired by Tony Stark's
technology.

------------------------------------------------------------------------

# Task 1: Booting Up JARVIS

### Core Interface & Assistant Setup --- 35 points

Before JARVIS can assist Tony, it needs a proper interface.

Build the main JARVIS command centre where Tony can interact with the
assistant.

### Subtask 1.1 --- Stark Command Centre (15 pts)

Create the main dashboard with a clear JARVIS-inspired interface.

The interface should include:

-   A JARVIS-style assistant/chat area.
-   A clear input field for Tony to enter commands.
-   A section showing the assistant's responses.
-   A split-screen view containing a **Live Integration Preview Pane** on one half (e.g., displaying the active Google Calendar, Google Drive file explorer, or Reminders list so Tony can verify actions live without navigating away).
-   A visible status indicator showing that JARVIS is online.
-   A futuristic Stark/Doomsday-inspired visual design.
-   Responsive layout suitable for both desktop and mobile.

The interface should feel like a **personal command centre**, rather
than a generic chatbot page.

### Subtask 1.2 --- Understanding Tony's Commands & Command Queuing (20 pts)

JARVIS should be able to recognise different categories of requests, handle input processing intelligently, and route them to the appropriate functionality.

For example:

-   "Schedule a meeting with Bruce tomorrow at 5 PM."
-   "Remind me to check the reactor at 8 PM."
-   "Upload this document to my Drive."
-   "Send a message to the team."
-   "What do I have scheduled for tomorrow?"

**Command Execution & Queuing**:
JARVIS must support sequential execution management when receiving back-to-back or rapid commands. The application should either:
-   Queue subsequent commands while an existing operation is executing, OR
-   Allow the user/Tony to choose whether new input interrupts and cancels the current running command or simply gets appended to the execution queue.

The exact wording does not need to be fixed. JARVIS should provide a
sensible response and guide the user when required information is
missing.

------------------------------------------------------------------------

# Task 2: Tony's Schedule

### Calendar & Reminder Management --- 40 points

Tony is constantly moving between meetings, experiments, and missions.

JARVIS must make sure he doesn't forget what matters.

### Subtask 2.1 --- Stark Calendar Integration (20 pts)

Connect JARVIS with **Google Calendar**.

Tony should be able to create and manage events through the assistant.

The application should support requests such as:

-   Creating a calendar event.
-   Setting the event title, date and time.
-   Adding a description when provided.
-   Viewing upcoming events in the side-by-side Calendar Preview Pane.
-   Handling missing or ambiguous information by asking Tony for
    clarification.

For example:

> "JARVIS, schedule a meeting with Bruce Banner tomorrow at 4 PM."

JARVIS should translate the request into an appropriate Google Calendar
event and immediately reflect it in the Live Preview Pane.

### Subtask 2.2 --- Don't Let Tony Forget (20 pts)

Add a reminder system that allows Tony to create and manage personal
reminders.

Examples:

-   "Remind me to check the Mark 50 at 7 PM."
-   "Remind me tomorrow morning about the reactor test."
-   "What reminders do I have today?"

The interface should clearly distinguish **calendar events** from
**personal reminders**, displaying active reminders within the command center's preview panel.

------------------------------------------------------------------------

# Task 3: The Stark Archive

### Google Drive & Document Management --- 45 points

Tony's work generates a huge amount of information --- designs, research
papers, reports, schematics, notes, and other documents.

JARVIS needs to keep the Stark Archive organised.

### Subtask 3.1 --- Upload to the Stark Archive (25 pts)

Integrate **Google Drive** with JARVIS.

Tony should be able to upload a user-provided document directly to his
Google Drive through the application.

For example:

> "JARVIS, upload this research report to my Drive."

The application should:

-   Allow the user to select a document from their device.
-   Provide the option to **choose an existing folder or create a new folder** in Google Drive (defaulting to `My Drive`).
-   Upload the selected file directly to the specified destination in Google Drive.
-   Upon successful authentication/action, display a **Live Drive Preview Pane** on the side showing the current files and folder structure in Drive.
-   Clearly indicate upload progress/status.
-   Handle upload failures gracefully.
-   Confirm when the document has been successfully uploaded.

The document should actually reach the authenticated user's Google Drive
rather than simply being stored locally.

### Subtask 3.2 --- Finding the Right File (20 pts)

Allow JARVIS to help Tony locate documents in his Drive.

For example:

> "JARVIS, find the reactor design report."

The assistant should be able to search the user's Drive and present
relevant files in the interface / preview pane with useful information such as:

-   File name.
-   File type.
-   Folder location.
-   Last modified time.
-   A way to open the file.

------------------------------------------------------------------------

# Task 4: Stark Communications

### Telegram & External Actions --- 35 points

Tony also needs JARVIS to communicate with the people around him.

### Subtask 4.1 --- Send a Message (20 pts)

Integrate **Telegram** so that Tony can send messages through JARVIS.

For example:

> "JARVIS, send Bruce a message saying the experiment is postponed."

The application should:

-   Identify the intended recipient.
-   Generate the message from Tony's request.
-   Ask for clarification if the recipient or message is unclear.
-   Send the message through Telegram.
-   Clearly indicate whether the message was successfully sent.

### Subtask 4.2 --- Communication History (15 pts)

Provide a simple way for Tony to view recent communication activity
handled by JARVIS.

Display useful information such as:

-   Recipient.
-   Message summary.
-   Time sent.
-   Delivery/action status.

The interface should make it clear which actions were performed by
JARVIS.

------------------------------------------------------------------------

# Task 5: The Doomsday Protocol

### Bringing JARVIS Together --- 45 points

Tony has now given JARVIS access to his calendar, reminders, documents,
and communication tools.

But a true personal assistant should make these capabilities work
together.

The final stage is to turn the individual features into **one coherent
JARVIS experience**.

### Subtask 5.1 --- Unified Command Flow & Queuing (20 pts)

A single user request may require multiple actions, or multiple requests may be issued in quick succession.

JARVIS should be capable of:
1.  Handling multi-step requests in sequence (e.g., "JARVIS, schedule the Stark team meeting for tomorrow at 6 PM, remind me 30 minutes before it, and send Bruce a Telegram message about it.").
2.  Managing input command queues or interrupt behavior when new instructions are submitted while previous tasks are executing.
3.  Reporting results clearly and updating the preview panel dynamically as each phase completes.

### Subtask 5.2 --- Action Confirmation & Error Handling (15 pts)

JARVIS should not silently fail.

Provide clear feedback when:

-   An integration is unavailable.
-   Authentication has expired.
-   A required field or folder location is missing.
-   A calendar event cannot be created.
-   A file upload fails.
-   A message cannot be sent.

For potentially consequential actions, JARVIS should provide an
appropriate confirmation step before executing them.

### Subtask 5.3 --- The Stark Interface (10 pts)

Polish the application into a cohesive **JARVIS × Doomsday** experience.

Consider:

-   Futuristic HUD-style components with dynamic dual-pane/preview layouts.
-   Stark-inspired typography and visual hierarchy.
-   Subtle animations and queue processing visual feedback.
-   Assistant status indicators.
-   Action history.
-   Clear loading and success/error states.
-   A consistent visual language across every feature.

The final application should feel like **Tony Stark is actually
interacting with JARVIS**, not like several APIs stitched together.

------------------------------------------------------------------------

# Final Mission

By the end of the task, Tony should be able to interact with JARVIS from
one web application and use it to:

-   Manage his Google Calendar with live preview confirmation.
-   Create and manage reminders.
-   Upload documents directly to chosen or newly created Google Drive folders.
-   Preview Google Drive contents directly in a side pane post-authentication.
-   Search and access files from Drive.
-   Send messages through Telegram.
-   Queue or interrupt command execution seamlessly.
-   View actions performed by JARVIS.
-   Combine multiple actions into a single request.

The goal is to build a **functional personal AI assistant**, not just a
chatbot UI.

## Theme

The entire application should be designed around the **JARVIS / Tony
Stark / Doomsday** setting.

You are free to interpret the visual style creatively, but the theme
should be visible in both the interface and the way the application
presents its functionality.

## Suggested Technologies

You may use any appropriate technologies and libraries.

Possible choices include:

-   React / Next.js
-   Node.js / Express
-   Python / FastAPI
-   Google Calendar API
-   Google Drive API
-   Telegram Bot API
-   Any suitable AI/LLM API

The technology stack is not fixed. What matters is the quality,
functionality, integration, and overall experience of the final
application.