### **The OSI Model (Networking)**

**What is the OSI Model?**  
The OSI (Open Systems Interconnection) model is a framework to understand how data flows across a network. It breaks down communication into  **7 layers**, each with a specific job. Think of it like a factory assembly line: each layer adds/removes a "wrapper" to prepare data for delivery.

----------

#### **The 7 Layers Explained (Top to Bottom)**

1.  **Layer 7: Application Layer**
    
    -   **What it does**: Directly interacts with user applications (e.g., web browsers, email clients).
        
    -   **Example**: When you type  `https://aws.amazon.com`, your browser (application layer) sends a request.
        
    -   **Protocols**: HTTP, HTTPS, DNS.
        
2.  **Layer 6: Presentation Layer**
    
    -   **What it does**: Translates data into a format the application layer understands (e.g., encryption, compression).
        
    -   **Example**: SSL/TLS encryption for secure HTTPS connections.
        
3.  **Layer 5: Session Layer**
    
    -   **What it does**: Manages connections between devices (start, maintain, end sessions).
        
    -   **Example**: A Zoom call setup: it ensures your call stays connected until you hang up.
        
4.  **Layer 4: Transport Layer**
    
    -   **What it does**: Ensures data arrives reliably and in order.
        
    -   **Key protocols**:
        
        -   **TCP**  (Transmission Control Protocol): Reliable but slower (used for emails, web pages).
            
        -   **UDP**  (User Datagram Protocol): Fast but unreliable (used for video streaming).
            
5.  **Layer 3: Network Layer**
    
    -   **What it does**: Routes data between networks using IP addresses.
        
    -   **Example**: A router directing traffic between your home network and AWS.
        
    -   **Protocol**: IP (Internet Protocol).
        
6.  **Layer 2: Data Link Layer**
    
    -   **What it does**: Transfers data between devices on the  **same network**  using MAC addresses.
        
    -   **Example**: Your home Wi-Fi router sending data to your laptop.
        
7.  **Layer 1: Physical Layer**
    
    -   **What it does**: Deals with physical hardware (cables, switches, radio waves).
        
    -   **Example**: Ethernet cables or fiber optics transmitting raw electrical/light signals.
        

----------

#### **Why Should You Care?**

-   **Troubleshooting**: If a website isn’t loading, you can isolate the issue:
    
    -   Layer 7: Is the URL correct?
        
    -   Layer 3: Is the IP address reachable?
        
-   **Cloud Relevance**: AWS services map to these layers. For example:
    
    -   **Application Load Balancer (ALB)**: Operates at Layer 7 (HTTP/HTTPS).
        
    -   **Network Load Balancer (NLB)**: Operates at Layer 4 (TCP/UDP).
        

----------

#### **Interview Question Prep**

**Q: What layer does a router operate at?**  
**A**: Layer 3 (Network Layer) – it uses IP addresses to route traffic between networks.

**Q: Why is TCP used for web browsing but UDP for video streaming?**  
**A**: TCP ensures no data is lost (critical for web pages), while UDP prioritizes speed (acceptable for video even if some frames drop).

----------

#### **How This Relates to Your Projects**

In your AWS cloud resume project:

-   **Application Layer (7)**: React frontend served via S3/CloudFront.
    
-   **Transport Layer (4)**: API Gateway uses HTTPS (TCP).
    
-   **Network Layer (3)**: VPCs and subnets manage IP routing.
    

----------
