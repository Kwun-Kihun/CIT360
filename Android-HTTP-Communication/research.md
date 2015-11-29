HTTP Connection

Most network-connected Android apps will use HTTP to send and receive data. Android includes two HTTP clients: HttpURLConnection and Apache HTTP Client. Both support HTTPS, streaming uploads and downloads, configurable timeouts, IPv6 and connection pooling.

Before the app attempts to connect to the network, it should check to see whether a network connection is available using getActiveNetworkInfo() and isConnected(). Remember, the device may be out of range of a network, or the user may have disabled both Wi-Fi and mobile data access. 
