# Tor.net
Add config in project
1) Add referent in "Tor Lib.zip" to project .Net
2) Unzip file "tor-win32-0.3.3.7.zip" and copy to Folder Tor in project
3) Add config tor file web.config/app.config 
<appSettings>
    <add key="ControlPassword" value="123456789" />
    <add key="ControlPort" value="9051" />
    <add key="SocketPort" value="9050" />
    <add key="TorPath" value="Tor" />
    <add key="Profile" value="" />
    <add key="License" value="" />
  </appSettings>
  - Profile and License: Please contact me to get the key;
  -ControlPort, SocketPort: port not used
  4) Function Library:
  public static string HTTPGetAPI(string uri, Client client = null, Dictionary<string, string> queryParams = null, int port = -1);
  public static string HTTPGetAPI(Uri uri, Client client = null, Dictionary<string, string> queryParams = null, int port = -1);
  public static string HTTPPostAPI(string url, Client client = null, Dictionary<string, string> para = null, int port = -1);
  public static string HTTPPostAPI(Uri url, Client client = null, Dictionary<string, string> para = null, int port = -1);

  5) Demo code:
    Tor.Clients.Client tor= Tor.Clients.Client.Instance(); // Khởi tạo Tor client
    string content = Tor.Clients.Client.HTTPGetAPI("https://www.torproject.org/download/download.html.en",tor); 

  
