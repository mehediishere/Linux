# Port

![port scan](port-scan.jpg)

In computer networking, a port is a communication endpoint. At the software level, within an operating system, a port is a logical construct that identifies a specific process or a type of network service.

To put it simply, A port is a virtual location where networking communication starts and ends.

There are two kinds of network ports on each computer
* TCP ( Transmission Control Protocol )
* UDP ( User Datagram Protocol )

A port scanner sends a TCP or UDP network packet and asks the port about their current status.

* **Open, Accepted:** The computer responds and asks if there is anything it can do for you.
* **Closed, Not Listening:** The computer responds that “This port is currently in use and unavailable at this time.”
* **Filtered, Dropped, Blocked:** The computer doesn’t even bother to respond.

|Port|Description|
|:---|:---|
|20| File Transfer Protocol (FTP) data channel.
|21| File Transfer Protocol (FTP) control channel. The commands port.
|22| Secure Shell (SSH). Remote management protocol OS.
|23| Telnet, or terminal network, for protocol implementation text interface across a network.
|25| Simple Mail Transfer Protocol (SMTP).
|37| Time protocol.
|43| WHOIS. Protocol for obtaining registration of ownership details for IP addresses and domain names.
|53| Domain Name System (DNS).
|67| Dynamic Host Configuration Protocol (DHCP). Dynamic IP.
|69| Trivial File Transfer Protocol (TFTP).
|79| Finger protocol.
|80| Hypertext Transfer Protocol (HTTP).
|88| Kerberos.
|109| Post Office Protocol v2 (POP2). Protocol for receiving emails, version two.
|110| Post Office Protocol v3 (POP3). Protocol for receiving emails, version three.
|115| Secure File Transfer Protocol (SFTP). Protocol for secure transmission of data.
|118| SQL Services.
|123| Network Time Protocol (NTP)
|143| Internet Message Access Protocol (IMAP). Protocol at the application level, for accessing emails.
|161| Simple Network Management Protocol (SNMP). Protocol for device management.
|162| Simple Network Management Protocol (SNMP) Trap.
|179| Border Gateway Protocol (BGP).
|194| Internet Relay Chat (IRC).
|389| Lightweight Directory Access Protocol (LDAP). Application layer protocol.
|443| Hypertext Transfer Protocol Secure (HTTPS). HTTP protocol, with support for encryption.
|464| Kerberos reset password.
|465| Simple Mail Transfer Protocol over SSL (SMTPS).
|514| Syslog.
|515| Line Printer Daemon (LPD). Protocol for remote printing.
|530| Remote Procedure Call (RPC).
|543| Kerberos login.
|544| Real Time Stream Control Protocol (RTSP).
|547| DHCPv6 server.
|993| Internet Message Access Protocol over SSL (IMAPS). IMAP protocol with support for SSL encryption.
|995| Post Office Protocol 3 over SSL (POP3S). POP3 protocol with support for SSL encryption.
|1080| SOCKet Secure (SOCKS). Protocol for receiving secure and anonymous access.
|3128| Proxy. Port often used for proxies.
|3306| MySQL, for MySQL database.
|3389| Remote Desktop Protocol (RDP), for Windows.
|5432| Postgres Database (PostgreSQL).
|5900| Virtual Network Computing (VNC). For desktop remote access.
|5938| TeamViewer, for the remote-control system, to facilitate data computer and data exchange.
|8080| HTTP/Web. An alternate HTTP protocol port.