## Setting up a Proof of Authority network and sending transactions using
MyCryto wallet ##

1.  Start to create a text file to keep some information noted and handy
    for reference. [HW18 Notes.txt](HW18%20Notes.txt). Probably this is
    the most important matter for the project to be success.

2.  Nest enter into MyCrypto , selected few addresses and their private
    keys as shown in the test note file in paragraphs 1,2 &3.

3.  Decide on chin ID. (Para 4)

4.  Decide on a password (para5). If you plan to use a new password for
    each node, you can skip that here and decide each time when asked
    for. In that case, follow the text file to find out where to keep
    the changing passwords.

5.  Now you can save and leave open the text file and start git bash and
    change the directory to "Go Eth directory".

6.  Inside the folder of where the Go Eth has been installed, start the
    puppet using gitbash -- "./puppeath"

7.  Once the puppeth started, select the following options in sequence
    (see the screensaves):

    a.  [PNGs\\Puppeth Screen1.png](PNGs/Puppeth%20Screen1.png)

    b.  [PNGs\\Puppeth Screen2.png](PNGs/Puppeth%20Screen2.png)

    c.  [PNGs\\Puppeth Screen3.png](PNGs/Puppeth%20Screen3.png)

8.  Use text file data when asked for addresses (Paras 1-3). Please use
    minimum two addresses, without the first two digits (0x). Use the
    same addresses to have them prefunded. Pressing enter after the
    addresses will take to the next line and at the end, next question
    too

9.  Last page of Screen3 is showing the exported files and failed files.
    We need only network \_ named file (hw18.json)

10. Now you can create node files and directories. Each node requires
    one time to use of "./geth"

    a.  ./geth \--datadir node1 account new

    b.  ./geth \--datadir node2 account new

    c.  ./geth \--datadir node3 account new

11. Copy down the information given out by geth during the step 10 to
    the text tile. These are the paras 6, 7, & 8. Here separate
    passwords can be used.

12. Initialize the notes with these command lines. [PNGs\\Puppeth
    Screen4.png](PNGs/Puppeth%20Screen4.png)

    a.  ./geth \--datadir node1 init hw18.json

    b.  ./geth \--datadir node2 init hw18.json

    c.  ./geth \--datadir node3 init hw18.json

13. Start the node1 -[PNGs\\node1 after
    transaction.png](PNGs/node1%20after%20transaction.png)

    a.  ./geth \--datadir node1 \--unlock
        0x22e55178FFF7faDA10AC7c324191BA3dabEc3329 \--rpc
        \--allow-insecure-unlock --ipcdisable

14. Start the node2 -[PNGs\\node2 after
    transaction.png](PNGs/node2%20after%20transaction.png)

    a.  ./geth \--unlock 0x211a55aAd5e459E5Fb65715020593C77A6D199d4
        \--datadir node2 \--port 30304 \--bootnodes
        \"enode://817f66c033c854b1b6aa5aa23d307974f0b2d90890e02163ea6cb86351e4c32b2b7db210e8a2a22dd27f1a246b61121755a1b5680476a80886e5e968abf5ea0f\@127.0.0.1:30303\"
        \--ipcdisable \--allow-insecure-unlock -rpcport 8546

15. Start the node 3 [PNGs\\node3 after
    transaction.png](PNGs/node3%20after%20transaction.png)

    a.  ./geth \--unlock 0x7620bD8473360783fAc0363601eE72298Fab082a
        \--datadir node3 \--port 30305 \--bootnodes
        \"enode://817f66c033c854b1b6aa5aa23d307974f0b2d90890e02163ea6cb86351e4c32b2b7db210e8a2a22dd27f1a246b61121755a1b5680476a80886e5e968abf5ea0f\@127.0.0.1:30303\"
        \--ipcdisable \--allow-insecure-unlock -rpcport 8547
        --nodiscover

16. At this point go to MyCrypto and setup a new currency called HW18
    and selected to it to use.[PNGs\\MyCrpto connected to
    network.png](PNGs/MyCrpto%20connected%20to%20network.png)

17. Go Keystore File button, browse for "/node1/keystore" directory and
    select private key file.

18. Select an address to send coin. Enter an amount to send. Selected
    the currency. [PNGs\\Mycrypto before
    send.png](PNGs/Mycrypto%20before%20send.png) or [PNGs\\transaction
    inter-addresses.png](PNGs/transaction%20inter-addresses.png)
    or[PNGs\\fourth transaction.png](PNGs/fourth%20transaction.png)

19. Send the transaction.[PNGs\\Sent out.png](PNGs/Sent%20out.png) and
    [PNGs\\pending transaction.png](PNGs/pending%20transaction.png)

20. Check for transaction completions. [PNGs\\pending fouth
    transaction.png](PNGs/pending%20fouth%20transaction.png)
