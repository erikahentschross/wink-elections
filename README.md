# Wink Election Widget

Download this repository and put it in a static directory accessible by your website (AWS S3 or through FTP access).

Navigate to this location to access the widget.

## Navigate and generate URLS
https://example.com/path/to/widget/#/2024/august will allow users to view both Local and Primary election instances.
Adding "local" or "primary" to the end of the URL will show only election events of those instances: 

Local: 
https://bannisterlake.com/dl/web-widgets/elections/us/local/#/2024/august/local

Primaries: 
https://bannisterlake.com/dl/web-widgets/elections/us/local/#/2024/august/primaries

## Use on website
Use generated URLs as the src of an iframe within your website. 

```<iframe id="gnca-iframe-1" height=300 width=300 src="https:/example.com/path/to/widget/#/2024/august/primaries"></iframe>```

## Making use of iframe resizing postMessage
These widgets use a postMessage to send the height of the widget to the parent window. Use this height to dynamically change the height of the iframe in order to avoid iframe scrolling. This height will adjust whenever a new election filter is selected.

The data object on the message event will look like this: 
```
{
  height: ###,
  action: "setHeight",
  target: "gnca-iframe-1",
  type: "gnca-iframe"
}
```

If you would like any of these variables changed contact repository owner.
If you would like to use this feature, the html will need updating to include parent domain as an authorized domain.  

