# How to Clear Local Plugin Settings

1) Go to `%localappdata%\Microsoft_Corporation\FullTrustSandbox(Excel-*\Version`

2) Open the `user.config` file and remove the plugin settings data. It will be surrounded by the Blockspring.ExcelAddIn.Services.Properties.Settings tags like so:

      <Blockspring.ExcelAddIn.Services.Properties.Settings>
        <!-- PLUGIN SETTINGS DATA IS HERE -->
      </Blockspring.ExcelAddIn.Services.Properties.Settings>
