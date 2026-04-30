# Instructions to restore VS Code on any device

## Reinstall all extensions in one shot

cat ~/vscode-backup/extensions.txt | xargs -L 1 code --install-extension

## Restore settings

cp ~/vscode-backup/settings.json ~/.config/Code/User/
cp "~/vscode-backup/keybindings.json" ~/.config/Code/User/
cp -r "~/vscode-backup/snippets" ~/.config/Code/User/
