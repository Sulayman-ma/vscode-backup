# Instructions to restore VS Code on any device

## Reinstall all extensions in one shot

**Linux/macOS**
```bash
cat ~/vscode-backup/extensions.txt | xargs -L 1 code --install-extension
```

**Windows (PowerShell)** — run from inside the `vscode-backup` directory
```powershell
Get-Content extensions.txt | ForEach-Object { code --install-extension $_ }
```

## Restore settings

**Linux/macOS**
```bash
cp ~/vscode-backup/settings.json ~/.config/Code/User/
cp ~/vscode-backup/keybindings.json ~/.config/Code/User/
cp -r ~/vscode-backup/snippets ~/.config/Code/User/
```

**Windows (PowerShell)** — run from inside the `vscode-backup` directory
```powershell
Copy-Item settings.json $env:APPDATA\Code\User\
Copy-Item keybindings.json $env:APPDATA\Code\User\
Copy-Item -Recurse snippets $env:APPDATA\Code\User\
```
