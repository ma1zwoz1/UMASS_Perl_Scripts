#!/usr/bin/perl
# Perl Assignment - Hash of Hashes
# Zachary Wozich 4-30-2018

# Amazon Books a Hash of Hashes

# I have created the following array:

@books = ("A Higher Loyalty", "Fascism: A Warning", "Killers of the Flower Moon", "I'll Be Gone in the Dark" , "Fire and Fury");

# and the following Hash of Hashes:

%myTitles = ( "A Higher Loyalty" => { copyRight => 2018,
                                    author => "J.Comey",
                                    publisher => "Flatiron",
                                    isdn => 1250192455,
                                    price => 17.99
                                  },
              "Fascism: A Warning" => { copyRight => 2018,
                                    author => "M.Albright-B.Woodward",
                                    publisher => "Harper",
                                    isdn => 62802186,
                                    price => 16.79
                                  },
              "Killers of the Flower Moon" => {copyRight => 2018,
                                    author => "D.Grann",
                                    publisher => "Doubleday",
                                    isdn => 307742482,
                                    price => 10.17
                                  },
                    "I'll Be Gone in the Dark" => { copyRight => 2018,
                                    author => "M.McNamara",
                                    publisher => "Harper",
                                    isdn => 62319787,
                                    price => 17.05
                                  },
                       "Fire and Fury" => { copyRight => 2018,
                                    author => "M.Wolff",
                                    publisher => "Holt",
                                    isdn => 1250158060,
                                    price => 16.05
                                  },

);

# To print out sorted Title information in the Hash of Hashes (ascending order):

print ("\n\nMy Title - sorted by Title Name ascending:\n\n");

printf("%-18s \t%-6s \t%-10s \t%-18s \t%-10s \t%-25s\n", "Title", "Copy Right", "Author", "Publisher", "ISDN", "Price");

@sortedKeys = sort (@books);

for $bookName (@sortedKeys) {
    $copyRight = $myTitles{$bookName}{'copyRight'};
    $author = $myTitles{$bookName}{'author'};
    $publisher = $myTitles{$bookName}{'publisher'};
    $isdn = $myTitles{$bookName}{'isdn'};
    $price = $myTitles{$bookName}{'price'};

    printf("%-18s \t%-6i \t%-10s \t%-18s \t%-10s \t%-25s \n", $bookName, $copyRight, $author, $publisher, $isdn, $price);
    print "\n";
}

# To print out sorted Title information in the Hash of Hashes (descending order):

print ("\n\My Title - sorted by Title Name decending:\n\n");

printf("%-18s \t%-6s \t%-10s \t%-18s \t%-10s \t%-25s\n", "Title", "Copy Right", "Author", "Publisher", "ISDN", "Price");

@reverseKeys = reverse (@sortedKeys);

for $bookName (@reverseKeys) {
    $copyRight = $myTitles{$bookName}{'copyRight'};
    $author = $myTitles{$bookName}{'author'};
    $publisher = $myTitles{$bookName}{'publisher'};
    $isdn = $myTitles{$bookName}{'isdn'};
    $price = $myTitles{$bookName}{'price'};

    
    printf("%-18s \t%-6i \t%-10s \t%-18s \t%-10s \t%-25s\n", $bookName, $copyRight, $author, $publisher, $isdn, $price);
    print "\n";
}

print "\n\nHTML Page containing information on my Books:\n\n";

print "<html>\n";
print "<head>\n";
print "<title>My Books</title>";
print "</head>\n";
print "<body>\n";
print "<H1>Book Titles</H1>\n";
print "<table border=1>\n";
print "<tr><th>Title</th><th>Copy Right</th><th>Author</th><th>Publisher</th><th>ISDN</th><th>Price/th></tr>\n";

for $bookName (sort keys %myTitles ) {
    $copyRight = $myTitles{$bookName}{'copyRight'};
    $author = $myTitles{$bookName}{'author'};
    $publisher = $myTitles{$bookName}{'publisher'};
    $isdn = $myTitles{$bookName}{'isdn'};
    $price = $myTitles{$bookName}{'price'};

    print "<tr><td>$bookName</td><td>$copyRight</td><td>$author</td><td>$publisher</td><td>$isdn</td><td>$price</td></tr>\n";
}
print "</table>\n";
print "</body>\n";
print "</html>\n";

print "\n\nXML file containing information on my Books - by Book Name ascending:\n\n"; 

print "<?xml version=\"1.0\"?>\n"; 
print "<teams>\n"; 

for $bookName (sort keys %myTitles ) { 

    print " <team>\n";

    $copyRight = $myTitles{$bookName}{'copyRight'}; 
    $author = $myTitles{$bookName}{'author'}; 
    $publisher = $myTitles{$bookName}{'publisher'}; 
    $isdn = $myTitles{$bookName}{'isdn'};
    $price = $myTitles{$bookName}{'price'}; 

    print " \n"; 

    print " <bookName>$bookName</bookName>\n"; 
    print " <copyRight>$copyRight</copyRight>\n";  
    print " <author>$author</author>\n";
    print " <publisher>$publisher</publisher>\n";
    print " <isdn>$isdn</isdn>\n";
    print " <price>$price</price>\n";

    print " </team>\n"; 
} 
print "</teams>\n";
