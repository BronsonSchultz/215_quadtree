# 215_quadtree
A qaud tree data structure implementation in the MIPS architecture assembly language

This data structure consists of nodes in a tree structure, each node can have at most 4 children. Each node contains a value pair x,y  
As data is entered into the tree, the program builds it in such a way that follows the ruling of the cartesian plane.  

    If the tree is empty, the pair will be inserted in the root 
    If the (new x > parent x) && (new y >= parent y) then the parent will recieve a North East child
    If the (new x >= parent x) && (new y < parent y) then the parent will recieve a South East child    
    If the (new x <= parent x) && (new y > parent y) then the parent will recieve a North West child   
    If the (new x < parent x) && (new y <= parent y) then the parent will recieve a South West child    

To add new nodes, the program performs a search through the tree until it fids the correct place for an insert. The creation of nodes is performed through a linked list. Each node in the linked list is allocated 6 words of memory, the first 2 words store the x and y values respectively and the last 4 words store the references to the nodes potential children.

The program also includes a recursive procedure to delete the entire tree. This procedure works bottom up so it could be called an any node in the tree to delete a subtree.

Running this program is not as easy as others, MIPS assembly language is a bit deprecated and not used by consumer CPUs. However, there are free simulators avaiable for download online that simulate a MIPS based machine. I used qtSpim to write and run this so I would suggest looking into that one!
