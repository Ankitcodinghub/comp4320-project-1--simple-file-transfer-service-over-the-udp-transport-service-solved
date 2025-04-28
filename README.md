# comp4320-project-1--simple-file-transfer-service-over-the-udp-transport-service-solved
**TO GET THIS SOLUTION VISIT:** [COMP4320 Project 1- Simple File Transfer Service over the UDP Transport Service Solved](https://www.ankitcodinghub.com/product/comp4320-computer-sciences-and-software-engineering-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;117722&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;COMP4320 Project 1- Simple File Transfer Service over the UDP Transport Service Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (3 votes)    </div>
    </div>
&nbsp;

Objective

Overview

In this project you will implement simple FTP client and server programs that must be written in C or C++ and execute correctly either in your own computer(s) or in the COE tux Linux computers. You will also implement segmentation and re-assembly function, an error detection function and a gremlin function (that can corrupt packets and lose packets with specified probabilities). The overview of these software components is shown in Figure 1 below.

PUT TestFile

Figure 1. Overview of the Software Components

The file is an ASCII file and must be at least 20 Kbytes in size. The file is sent in 128byte packets (including the header) until the end of the file is reached. The last packet will be padded with NULL character if the remaining data of the file is less than 128 bytes. At the end of the file, it transmits 1 byte (NULL character) that indicates the end of the file. It will then close the file.

Add cout or printf statements in the client program to print the sequence numbers and data to indicate that client is sending the packets and also receiving packets from the server, i.e. print each packet sequence number and data (say, only the first 48 bytes of data) that it sends and receives.

The FTP server program will respond to the client FTP requests. On receiving the PUT request, the server will receive data of the file in 128-byte packets, i.e. the server will receive each 128-byte packet in a loop and writes them into a local file system sequentially. Each packet is processed by the error detection function that will detect possibility of error based on the checksum. If there are errors in the packet, just print the error message and the packet sequence number. You do not need to handle errors or lost packets in this project. The packet is then processed by the segmentation and re-assembly function that re-assembles all the segments of the file from the packets received into the original file. When it receives a 1-byte message with a NULL character, then it knows that the last packet has been received and it closes the file. The server then constructs FTP response messages by putting the status on the header lines. The header line will be of the following form:

PUT successfully completed

This FTP server response packet is not processed by the segmentation and re-assembly, error detection or the Gremlin function.

Add cout or printf statements in the server program to print the sequence numbers and data to indicate that the server is receiving packets and sending the packets, i.e. print each packet sequence number and data (say, only the first 48 bytes of data) that it receives and sends.

Gremlin Function

Your program must allow the probabilities of damaged and lost packets to be input as arguments when the program is executed. These parameters for packet damage and lost probabilities are passed to your Gremlin function. You will implement a gremlin function to simulate three possible scenarios in the transmission line: (1) transmission error that cause packet corruption, (2) packet loss, and (3) correct delivery. Before the client process sends each packet through the UDP socket, it first pass the packet to a gremlin function which will randomly determine, depending on the damage probability, whether to change (corrupt) some of the bits or pass the packet as it is to the server receiving function. It will also decide whether some packets will be dropped based on the loss probability. The gremlin function uses a random-number generator to determine whether to damage a packet, drop (lose) a packet or pass the packet as it is to the receiving function. For example, a packet’s loss probability of 0.2 would mean that two out of ten packets will be dropped.

If it decides to damage a packet, it will decide on how many and which byte to change. The probability that a given packet will be damaged, P(d), is entered as an argument at runtime. If the probability of damaging a packet is .3, then three out of every ten packets will be damaged. If the packet is to be damaged, the probability of changing one byte is .7, the probability of changing two bytes is .2, and the probability of changing 3 bytes is .1. Every byte in the packet is equally likely to be damaged. The packet is then passed from the gremlin function to be sent through the UDP socket.

Error Detection Function

The sending process, e.g. the FTP client, will compute the checksum for the packet that is to be sent. The checksum is calculated by simply summing all the bytes in the packet. The checksum is then inserted into the checksum header field of the packet.

The receiving process, e.g. the FTP server, will then use the same algorithm for computing the checksum that the sending process used. It will calculate the checksum by summing all the bytes in the received packet. It then compares the computed checksum with the checksum received in the packet. If the two checksums match, then it assumes that there is no error, otherwise there is at least an error in the packet.

When the receiving process detects an error in a packet, it will print out a message indicating the packet’s sequence number and that there is an error in the packet.

In this project, the receiver need not handle errors in packets; instead, it just prints out a message indicating that the packet has an error and prints the packet sequence number. The sender does not need to handle the packet error either.

Testing

In both environments that you use for your execution environment, capture the execution trace of the programs. In Linux, use the script command to capture the trace of the execution of your FTP client and FTP server programs. The execution traces must contain information when packets are sent or received, when packets are corrupted, and when packets are lost. Sequence numbers and other relevant information on the packets must be printed.

Print the content of the input file read by the client program and the output file received by the server program.

Submission
