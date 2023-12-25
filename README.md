# 802.1X-Term

IEEE 802.1X provides port-based authentication. Network devices have the following roles:

1. Supplicant: Endpoint 802.1X-compliant software service. It communicates with NAD authenticators to request network access.

2. Authenticator: Controls access to the network, based on client authentication status. The objective here is for endpoints to authenticate to the authentication server via some EAP. NAD authenticators act as an intermediary (proxy) between client and authentication server. They communicate with endpoint supplicants via 802.1X, to request identity information. Then they communicate with the authentication server via RADIUS to verify that information. They relay authentication server responses back to the client. The authenticator acts as a RADIUS client, encapsulating and de-encapsulating EAP frames. .

3. Authentication server: This role performs client authentication. The authentication server validates client identity and notifies NAD authenticators of client authorization status. Because the authenticator acts as the proxy, the authentication service is transparent to the client. Cisco ISE acts as the authentication server.
