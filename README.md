
# macOS-style Traffice Light Buttons for GNOME

This repository provides **macOS window control buttons** (close, minimize, maximize) as **standalone CSS** for both **GTK 3.0 / GTK 4.0** and **Firefox (applied on a GNOME theme)**. 

---

## 📁 Directory Structure

```
.
├── gtk-3.0/
│   ├── gtk.css
│   └── windows-assets/
│       └── ... (button images)

├── gtk-4.0/
│   ├── gtk.css
│   └── windows-assets/
│       └── ... (button images)

└── chrome/
    ├── firefox-gnome-theme/
    ├── userChrome.css
    ├── userContent.css
    └── whitesur-titlebuttons/
        └── windows-assets/
            └── ... (button images)
```

---

## GTK Installation

### GTK 3.0

```bash
mkdir -p ~/.config/gtk-3.0
cp -r gtk-3.0/* ~/.config/gtk-3.0/
```

### GTK 4.0

```bash
mkdir -p ~/.config/gtk-4.0
cp -r gtk-4.0/* ~/.config/gtk-4.0/
```

### Both GTK 3.0 & 4.0

```bash
# GTK 3.0
mkdir -p ~/.config/gtk-3.0
cp -r gtk-3.0/* ~/.config/gtk-3.0/

# GTK 4.0
mkdir -p ~/.config/gtk-4.0
cp -r gtk-4.0/* ~/.config/gtk-4.0/
```

---

## Appending to Existing gtk.css

If you already have a GTK theme and just want to add the buttons:

```bash
# GTK 3.0
cat gtk-3.0/gtk.css >> ~/.config/gtk-3.0/gtk.css
cp -r gtk-3.0/windows-assets ~/.config/gtk-3.0/

# GTK 4.0
cat gtk-4.0/gtk.css >> ~/.config/gtk-4.0/gtk.css
cp -r gtk-4.0/windows-assets ~/.config/gtk-4.0/
```

---

## Firefox Integration

The `chrome/` directory contains files for modifying the **Firefox GNOME Theme** with macOS style window control buttons.


### Instructions

1. **Install the [Add Water](https://github.com/rafaelmardojai/firefox-gnome-theme#installation) extension** (required for GNOME theme integration).

2. Go to `about:profiles` in Firefox.

3. Under the profile currently **in use**, click **“Open Directory”** (this opens your Firefox profile’s root folder).

4. In that folder, **replace** the existing `chrome` directory with the `chrome` folder from this repository:

   ```bash
   # Example
   cp -r chrome ~/.mozilla/firefox/<your-profile>/
```

5. Restart Firefox to apply the changes.


---

## Theme Switching

### Light Theme

Light buttons are used by default.

### Dark Theme

Dark buttons are automatically applied when the `.dark` class is present (GTK themes and Firefox GNOME theme handle this automatically).

---

## License

Extracted from **WhiteSur GTK Theme** by **Vince Liuice** and **Firefox GNOME theme** by **Rafael Mardojai**
Licensed under **GPL-3.0+**

---

## Source

Original projects: 
[https://github.com/vinceliuice/WhiteSur-gtk-theme](https://github.com/vinceliuice/WhiteSur-gtk-theme)
[https://github.com/rafaelmardojai/firefox-gnome-theme](https://github.com/rafaelmardojai/firefox-gnome-theme)

