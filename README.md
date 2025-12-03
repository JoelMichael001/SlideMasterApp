SlideMaster Pro – Local Presentation Remote
A desktop + web remote tool to control PDF presentations over your local Wi-Fi network.
Only for Windows

________________________________________
Core Functionality
1. Multi-PDF Presentation Manager (Desktop)
   •	Load up to 3 PDF files into separate “slots” (File 1, File 2, File 3). 

   •	Each slot:
      o	Stores the PDF path, rendered slide images, current slide index, and optional slide titles.
      o	Is selectable via side buttons to quickly switch between presentations.
   •	Slot names are user-editable, so “File 1/2/3” can be renamed (e.g., “Session 1”, “Backup deck”). Names are saved and restored on next launch. 

   •	State (loaded PDFs, active slot, slide indices, titles, default image, theme, custom file names) is saved to a JSON file in a persistent data directory and automatically restored. 

2. Slide Preview & Fullscreen Presentation
   •	Desktop UI shows Previous / Current / Next slide previews side-by-side.
   •	Fullscreen presentation window on a selectable monitor:
      o	Choose which display to use for presenting.
      o	Shows the current slide scaled to screen.
      o	Supports keyboard navigation: arrow keys for next/previous, Esc to exit. 
   •	Live presentation timer (mm:ss or hh:mm:ss) runs during active presentation and is shown in the main window footer (and mirrored to the web remote). 

3. Blank & Default Screen Modes
   •	Blank Page: instantly switch the presentation output to a black screen without closing the presentation.
   •	Default Image:
      o	Load a PNG/JPG as a “title screen” or standby slide.
      o	Toggle it in fullscreen instead of a slide.
      o	Default image persisted across runs. 

4. Slide Titles Editor
   •	Per-PDF slide titles can be edited in a dedicated dialog.
   •	Titles are:
      o	Stored with the slot,
      o	Used as labels in the web remote slide grid to quickly identify slides by name instead of number. 

5. Local Web Remote (Phone / Tablet Control)
   •	Starts a local Flask server (default port 5000) that exposes a web remote UI. 
   •	Desktop shows the remote URL and a QR code so a phone can connect easily over the same Wi-Fi. 
   •	Web remote features:
      o	Main controls: Present, Blank, Default, Close, Prev, Next.
      o	File selection buttons for File 1/2/3, showing which file is loaded and active.
      o	Slide grid: tap any slide to instantly jump to that page.
      o	A small timer pill showing the live presentation time.
   •	All commands are sent to the desktop via an in-memory bridge (web_bridge callbacks), and the desktop periodically polls for remote actions. 

6. Theming & Custom Chrome
   •	Custom frameless window with:
      o	Custom title bar (logo + title text + custom minimize/close buttons).
   •	Built-in themes:
      o	Dark, Light, AMOLED Black
   •	Theme choice is persisted between sessions

