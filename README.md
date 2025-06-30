<p align="center">
  <img src="banner.png" alt="EdgeRemover banner" width="800">
</p>

<p align="center"><b>A PowerShell script that correctly uninstalls or reinstalls Microsoft Edge on Windows 10 & 11.</b></p>

---

## 🎉 Features

- Remove Edge with its own uninstaller, meaning there aren't leftovers, alongside no breakage as nothing is hardcoded
- Multiple fallback methods for uninstallation
- Can remove Edge installed with a `.msi`
- Ability to reinstall Edge and WebView2
- Implementable in scripts with parameters

## ⬇️ Usage

You can use the commands below in `Command Prompt` to launch the script.

```powershell
@powershell -NoProfile -ExecutionPolicy Bypass -Command "& ([ScriptBlock]::Create((irm https://cdn.jsdelivr.net/gh/iammelvink/EdgeRemover@main/get.ps1)))"
```

Uninstall Edge, remove Edge's user-data, and install Edge WebView. **`Recommended*`**

  ```powershell
  @powershell -NoProfile -ExecutionPolicy Bypass -Command "& ([ScriptBlock]::Create((irm https://cdn.jsdelivr.net/gh/iammelvink/EdgeRemover@main/get.ps1))) -UninstallEdge -RemoveEdgeData -InstallWebView -NonInteractive"
  ```

<p align="center">
  <img src="showcase.png" alt="Image of the EdgeRemover UI" width="800">
</p>

### 📜 Implementation in Scripts

Download the script and run `Get-Help .\RemoveEdge.ps1` in `PowerShell` to see its options. You can either use the downloaded file directly with these arguments or put them into the snippet below:

```powershell
iex "&{$(irm https://cdn.jsdelivr.net/gh/iammelvink/EdgeRemover@main/get.ps1)} [ARGUMENTS HERE]"
```

<details>
  <summary>Example</summary>

  This would uninstall Edge, remove Edge's user-data, and install Edge WebView:

  ```powershell
  iex "&{$(irm https://cdn.jsdelivr.net/gh/iammelvink/EdgeRemover@main/get.ps1)} -UninstallEdge -RemoveEdgeData -InstallWebView"
  ```

</details>

## 🫧 Clearing Edge Blocks

You can use the command below in `PowerShell` to clear all EdgeUpdate policies, including those that block the reinstallation and update of Edge or WebView.

```powershell
iex "&{$(irm https://cdn.jsdelivr.net/gh/iammelvink/EdgeRemover@main/get.ps1)} -ClearUpdateBlocks"
```

## ❓ Troubleshooting

If Edge won't uninstall, try:

1. Repairing Edge
2. Making sure that Windows is up to date
3. Making sure that Edge is up to date

## ✅ Additional Credits

- [Xyueta](https://github.com/Xyueta) - minor bug fixes
- [ave9858](https://gist.github.com/ave9858/c3451d9f452389ac7607c99d45edecc6) - inspired this script
- [h3r0](https://github.com/melo936) - notified me about the 'windir' method in the script

### Credit to

[@he3als](https://github.com/he3als/EdgeRemover)

## More Stuff

Check out some other stuff on
[Melvin K](https://github.com/iammelvink 'Melvin K GitHub page')
