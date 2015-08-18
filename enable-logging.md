# Report an Excel bug (and logging instructions)

If you've found an bug with our Excel plugin, let us know! We'd love to fix it asap.

Here's the trick - a lot can go wrong. Could be a problem with a specific update in Excel, Windows, a network firewall, or something completely unique. That's why it'd be very helpful to know exactly where the plugin code failed on your machine.

To pinpoint the failure, we'd love for you to temporarily turn on the plugin logging, re-do the steps you did to produce the error, and send us the results. Here's how to do that:

  1) Navigate to following path:  `%appdata%\BlockSpring\Blockspring for Excel\`
  
  2) Open the file “BlockSpring.ExcelAddIn.xll.config” (if you have x86 version of Excel) or “BlockSpring.ExcelAddIn64.xll.config” (if you have x64 version of Excel) with any text editor (ie Notepad)
  
  3) Find the following string:
  
      <!--section name="log4net" type="log4net.Config.Log4NetConfigurationSectionHandler, log4net" /-->
  
  and replace it with the following string:
  
      <section name="log4net" type="log4net.Config.Log4NetConfigurationSectionHandler, log4net" />
  
  4) Find the following string:
  
      <!--log4net debug="false">
    
        <appender name="FileAppender" type="log4net.Appender.FileAppender">
    
          <file value="log-file.txt" />
    
          <appendToFile value="true" />
    
          <layout type="log4net.Layout.PatternLayout">
    
            <conversionPattern value="%date [%thread] %-5level %logger - %message%newline" />
    
          </layout>
    
        </appender>
    
     
    
        <root>
    
          <level value="ALL" />
    
          <appender-ref ref="FileAppender" />
    
        </root>
    
      </log4net-->
  
  
  and replace it with the following string:
  
  
      <log4net debug="false">
  
        <appender name="FileAppender" type="log4net.Appender.FileAppender">
    
          <file value="log-file.txt" />
    
          <appendToFile value="true" />
    
          <layout type="log4net.Layout.PatternLayout">
    
            <conversionPattern value="%date [%thread] %-5level %logger - %message%newline" />
    
          </layout>
    
        </appender>
    
     
    
        <root>
    
          <level value="ALL" />
    
          <appender-ref ref="FileAppender" />
    
        </root>
  
      </log4net>
   
  
  5) Save and close the file
  
  6) Re-open Excel and try to reproduce the error.
  
  7) Once you run into the error, navigate to `%appdata%\BlockSpring\Blockspring for Excel\`, find **log.txt** file and send to support@blockspring.com.
