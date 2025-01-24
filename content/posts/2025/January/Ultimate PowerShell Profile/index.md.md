---
title: Ultimate Powershell Profile
date: 2025-01-24T22:12:09+05:30
lastmod: 2025-01-24T22:12:09+05:30
author: its-ashu-otf
cover: /img/2025/powershell-cover.png
images:
   - /img/2025/powershell-cover.png
categories:
  - windows
tags:
  - powershell-profile
  - powershell
  - windows
  - pwsh
---

# PowerShell Profile: Linux Terminal Experience on Windows

PowerShell is already powerful on its own, but with a few tweaks and enhancements, you can transform it into a Linux-like terminal experience—right on your Windows machine. This blog walks you through setting up a custom PowerShell profile that comes preloaded with quality-of-life improvements, aliases, and shortcuts to supercharge your terminal experience.

---

## ⚡ One-Line Install

Getting started is quick and easy. Open an **elevated PowerShell window** (run PowerShell as Administrator) and execute the following command:

```powershell
irm "https://github.com/its-ashu-otf/powershell-profile/raw/main/setup.ps1" | iex
```

This script sets up a PowerShell profile that not only mimics a Linux terminal but also introduces productivity-enhancing features.

---

## 🔧 Fixing the Missing Font Issue

After running the script, you'll notice that some icons or glyphs might not render correctly. That’s because your current font doesn’t support Nerd Fonts. Here are two simple options to resolve this:

### Option 1: Manual Installation

1. After running the script, you’ll find a downloaded file named `cove.zip` in the folder where you executed the setup.
2. Extract the `cove.zip` file.
3. Locate the patched **Caskadia Mono Nerd Font Family** files.
4. Install these fonts by right-clicking on each file and selecting "Install for all users."

### Option 2: Automated Installation with Oh-My-Posh

The PowerShell profile comes preloaded with **Oh-My-Posh**, a powerful prompt theme engine. You can use it to install a Nerd Font effortlessly:

1. Run the following command:
    
    ```powershell
    oh-my-posh font install
    ```
    
2. You’ll see a list of available Nerd Fonts like this:
    
    ```
    PS> oh-my-posh font install
    
       Select font
    
     > 0xProto
       3270
       Agave
       AnonymousPro
       Arimo
       AurulentSansMono
       BigBlueTerminal
       BitstreamVeraSansMono
    
       •••••••
       ↑/k up • ↓/j down • q quit • ? more
    ```
    
3. Use the arrow keys to navigate, select your desired font, and press **Enter** to install it.
    

---

## 🎨 Customizing Your PowerShell Profile

One key feature of this setup is that the main profile file, `Microsoft.PowerShell_profile.ps1`, is protected. Any changes you make to this file will be overwritten by future updates from the repository. Instead, follow these steps to create your own custom profile:

1. After installation, run the following command:
    
    ```powershell
    Edit-Profile
    ```
    
2. This will create a new profile file named `profile.ps1` for your current user.
    
3. Open the file in your preferred text editor (e.g., VS Code, Notepad++).
    
4. Add any custom aliases, functions, or shortcuts here. For example:
    
    ```powershell
    # Example Alias
    Set-Alias ll Get-ChildItem
    
    # Example Function
    function cdls {
        param (
            [string]$Path
        )
        Set-Location $Path
        Get-ChildItem
    }
    ```
    
5. Save the file and reload your PowerShell session to apply the changes.
    

---

## 🚀 Enjoy the Enhanced PowerShell Experience

Once your profile is installed and customized, you’ll enjoy:

- A Linux-like terminal environment.
- Beautifully themed prompts with **Oh-My-Posh**.
- Useful aliases and shortcuts.
- Support for icons and glyphs with Nerd Fonts.
- Linux Like Aliases
- Zoxide Integration
- History Implementation
- Automated Updated Profile Configuration
- & many more....
PowerShell doesn’t have to be boring—with this setup, it’s modern, efficient, and a joy to use. Try it out today and see the difference!

---

### Resources

- [PowerShell Profile GitHub Repository](https://github.com/its-ashu-otf/powershell-profile)
- [Oh-My-Posh Documentation](https://ohmyposh.dev/)
- [Nerd Fonts](https://www.nerdfonts.com/)