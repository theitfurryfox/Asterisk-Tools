# This is for ROOT SSSH access.

## Dark Mode

```bash
nano /var/www/html/admin/assets/js/dark.js
```

Then 
```bash
(function() {
    // Load DarkReader script dynamically
    const script = document.createElement('script');
    script.src = 'https://unpkg.com/darkreader/darkreader.js';
    script.onload = () => {
        // Enable DarkReader with default settings
        DarkReader.enable({
            brightness: 100,
            contrast: 90,
            sepia: 10,
        });
    };
    document.head.appendChild(script);
})();
```

then
```bash
mysql
```

Then
```
UPDATE asterisk.freepbx_settings SET value = 'assets/js/dark.js' WHERE keyword = 'BRAND_ALT_JS'; quit;
```
And Enjoy Darkmode
