# TCP-IPC-connection

Step 1: (Initially)

	On PC 1 TCP client is running
	On PC 2 TCP Server is running + When any demand comes from TCP client then IPC Client runs here
	On PC 3 IPC Server is running
Step 2:
	1.Now TCP Client connects to TCP sever via sockets 
	2.TCP client send file name to TCP server.
	3.Now TCP server check its directory for existence of file 
	4.If file exists in the server directory then TCP server sends file to TCP Client.

Step 3: If File does not exist on TCP Server PC then 
	
	1.TCP Server run IPC Client via pipes.
	2.Now IPC client connect to IPC Server via socket and send the file name.
	3.IPC server send the file to IPC Client then TCP server send file to TCP client.
	4.Connection closed between TCP Server and TCP Client
