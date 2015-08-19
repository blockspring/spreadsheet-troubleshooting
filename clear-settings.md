# How to Clear Local Plugin Settings

1) Go to `%localappdata%\Microsoft_Corporation\FullTrustSandbox(Excel-*\Version`

2) Open the `user.config` file in Notepad and remove the plugin settings data. Specifically remove everything in between the Blockspring.ExcelAddIn.Services.Properties.Settings tags like so:

      <Blockspring.ExcelAddIn.Services.Properties.Settings>
        <!-- PLUGIN SETTINGS DATA IS HERE -->
      </Blockspring.ExcelAddIn.Services.Properties.Settings>
