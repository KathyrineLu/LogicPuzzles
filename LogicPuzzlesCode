import javax.swing.*; //import libraries
import java.awt.*;
import java.awt.event.*;
import java.applet.Applet;

public class logicPuzzle1 extends Applet implements ActionListener
{
    Panel p_card; //to hold all of the screen
    Panel card1, card2, card3, card4, card5, card6, card7, card8, card9, card10, card11, card70, card71, card72, card73, card74, card75, card80, card81, card82, card83, card84, card85; //declaring the cards/screens used
    CardLayout cdLayout = new CardLayout (); //Cardlayout to hold all cards/screens
    JComboBox choose; //declaring the Combo Box found in screen 3 (Easy Logic Puzzles screen)
    JComboBox choose1; //declaring the Combo Box found in screen 4 (Hard Logic Puzzles screen)

    JButton easygrid[] = new JButton [100]; //grid buttons in Busy Lovebirds puzzle (card6)
    JButton easygrid1[] = new JButton [100]; //grid buttons in Speed Dating puzzle (card7)
    JButton easygrid2[] = new JButton [100]; //grid buttons in Evil Exes puzzle (card8)
    JButton hardgrid[] = new JButton [144]; //grid buttons in Lots of Love puzzle (card9)
    JButton hardgrid1[] = new JButton [144]; //grid buttons in Island Weddings puzzle (card10)
    JButton hardgrid2[] = new JButton [144]; //grid buttons in Anniversary Cruises puzzle (card11)

    //variables used often in grid button functions (ex. resetting grids, changing button image, etc.)
    int i = 0;
    int j = 0;

    //arrays used in all puzzles to set values for each button (so that the image can be changed when clicked later on)
    int a[] [] = new int [10] [10];
    int a1[] [] = new int [10] [10];
    int a2[] [] = new int [10] [10];

    int b[] [] = new int [12] [12];
    int b1[] [] = new int [12] [12];
    int b2[] [] = new int [12] [12];


    public void init ()
    {
        p_card = new Panel ();
        p_card.setLayout (cdLayout);
        //everything below is to call the screens/cards used in the game
        main ();
        instructions ();
        easy ();
        hard ();
        busyLovebirds ();
        speedDating ();
        evilExes ();
        lotsOfLove ();
        islandWeddings ();
        anniversaryCruises ();
        busyLovebirdsDescription ();
        speedDatingDescription ();
        evilExesDescription ();
        lotsOfLoveDescription ();
        islandWeddingsDescription ();
        anniversaryCruisesDescription ();
        cluesBusyLovebirds ();
        cluesSpeedDating ();
        cluesEvilExes ();
        cluesLotsOfLove ();
        cluesIslandWeddings ();
        cluesAnniversaryCruises ();

        resize (900, 600); //resize the screen appropiately
    }


    public void main ()  //main screen

    {
        card1 = new Panel (new BorderLayout ());
        setBackground (new Color (236, 193, 217)); //set background colour for all screens
        add ("Center", p_card);

        Panel g = new Panel (); //panels to adjust screen layout
        Panel h = new Panel (new FlowLayout ());
        Panel i = new Panel (new BorderLayout ());
        Panel j = new Panel ();
        Panel k = new Panel ();
        Panel l = new Panel (new BorderLayout ());
        Panel m = new Panel (new BorderLayout ());

        JLabel title = new JLabel (createImageIcon ("Main Title.JPG"));

        JButton easy = new JButton ("Easy"); //go to easy puzzles
        easy.setFont (new Font ("Elephant", Font.PLAIN, 20));
        easy.setActionCommand ("3");
        easy.addActionListener (this);

        JButton hard = new JButton ("Hard"); //go to hard puzzles
        hard.setFont (new Font ("Elephant", Font.PLAIN, 20));
        hard.setActionCommand ("4");
        hard.addActionListener (this);

        JButton instructions = new JButton ("How to Play"); //go to instructions
        instructions.setFont (new Font ("Elephant", Font.PLAIN, 20));
        instructions.setActionCommand ("2");
        instructions.addActionListener (this);

        JButton quit = new JButton ("Exit"); //leave game
        quit.setFont (new Font ("Elephant", Font.PLAIN, 20));
        quit.setActionCommand ("ExitGame");
        quit.addActionListener (this);

        //adjusting layout
        g.add ("North", title);
        h.add (easy);
        h.add (hard);
        i.add ("North", g);
        i.add (h);
        j.add (instructions);
        k.add (quit);
        l.add ("North", j);
        l.add (k);
        m.add ("North", i);
        m.add (l);
        card1.add (m);

        p_card.add ("1", card1);
    }


    public void instructions ()  //instructions
    {
        card2 = new Panel (new BorderLayout ());

        Panel g = new Panel ();
        Panel h = new Panel ();
        Panel i = new Panel (new BorderLayout ());

        JLabel inst = new JLabel (createImageIcon ("Instructions.JPG")); //title (in an image)

        JButton menu = new JButton ("Menu"); //return to menu
        menu.setActionCommand ("1");
        menu.addActionListener (this);

        g.add (inst);
        h.add (menu);
        i.add ("North", g);
        i.add (h);
        card2.add (i);

        p_card.add ("2", card2);
    }


    public void easy ()  //easy puzzles selection screen
    {
        card3 = new Panel (new BorderLayout ());

        Panel g = new Panel ();
        Panel h = new Panel (new BorderLayout ());
        Panel i = new Panel (new BorderLayout ());
        Panel k = new Panel ();

        JLabel title = new JLabel (createImageIcon ("Easy Logic Puzzles Title.JPG")); //screen title
        JLabel border = new JLabel (createImageIcon ("Bottom Border.JPG")); //decoration

        JLabel select = new JLabel ("Select a puzzle: ");
        select.setFont (new Font ("Lucida Calligraphy", Font.PLAIN, 20));

        String[] puzzles = {"Busy Lovebirds", "Speed Dating", "Evil Exes"};
        choose = new JComboBox (puzzles); //combo box for player to choose a puzzle

        choose.setSelectedIndex (0); //set combo box default
        choose.setActionCommand ("easyCombo");
        choose.addActionListener (this);

        JButton menu = new JButton ("Back to Menu"); //return to menu
        menu.setActionCommand ("1");
        menu.addActionListener (this);

        g.add (select);
        g.add (choose);
        h.add ("North", border);
        k.add (menu);
        h.add (k);
        i.add ("North", g);
        i.add (h);
        card3.add ("North", title);
        card3.add ("Center", i);

        p_card.add ("3", card3);
    }


    public void hard ()  //hard puzzle selection screen
    {
        card4 = new Panel (new BorderLayout ());

        Panel g = new Panel ();
        Panel h = new Panel (new BorderLayout ());
        Panel i = new Panel (new BorderLayout ());
        Panel k = new Panel ();

        JLabel title = new JLabel (createImageIcon ("Hard Logic Puzzles Title.JPG"));
        JLabel border = new JLabel (createImageIcon ("Bottom Border.JPG")); //decoration

        JLabel select = new JLabel ("Select a puzzle: ");
        select.setFont (new Font ("Lucida Calligraphy", Font.PLAIN, 20));

        String[] puzzles = {"Lots of Love", "Island Weddings", "Anniversary Cruises"};
        choose1 = new JComboBox (puzzles); //combo box to choose a puzzle
        choose1.setSelectedIndex (0);
        choose1.setActionCommand ("hardCombo");
        choose1.addActionListener (this);


        JButton menu = new JButton ("Back to Menu"); //return to menu
        menu.setActionCommand ("1");
        menu.addActionListener (this);

        g.add (select);
        g.add (choose1);
        h.add ("North", border);
        k.add (menu);
        h.add (k);
        i.add ("North", g);
        i.add (h);
        card4.add ("North", title);
        card4.add ("Center", i);

        p_card.add ("4", card4);
    }


    //THE NEXT 6 METHODS ARE SCREENS SHOWING THE DESCRIPTIONS FOR EACH PUZZLE (IN ORDER: Busy Lovebirds, Speed Dating, Evil Exes, Lots of Love, Island Weddings, Anniversary Cruises)
    public void busyLovebirdsDescription ()
    {
        card70 = new Panel (new BorderLayout ());

        Panel g = new Panel ();
        Panel h = new Panel ();
        Panel i = new Panel (new BorderLayout ());

        JButton start = new JButton ("Start puzzle");
        start.setActionCommand ("6");
        start.addActionListener (this);


        JLabel desc = new JLabel (createImageIcon ("Busy Lovebirds Description.JPG"));

        JButton back = new JButton ("Back");
        back.setActionCommand ("3");
        back.addActionListener (this);

        h.add (start);
        h.add (back);
        i.add ("North", desc);
        i.add (h);
        card70.add (i);

        p_card.add ("70", card70);
    }


    public void speedDatingDescription ()
    {
        card71 = new Panel (new BorderLayout ());

        Panel g = new Panel ();
        Panel h = new Panel ();
        Panel i = new Panel (new BorderLayout ());

        JButton start = new JButton ("Start puzzle");
        start.setActionCommand ("7");
        start.addActionListener (this);


        JLabel desc = new JLabel (createImageIcon ("Speed Dating Description.JPG"));

        JButton back = new JButton ("Back");
        back.setActionCommand ("3");
        back.addActionListener (this);

        h.add (start);
        h.add (back);
        i.add ("North", desc);
        i.add (h);
        card71.add (i);

        p_card.add ("71", card71);
    }


    public void evilExesDescription ()
    {
        card72 = new Panel (new BorderLayout ());

        Panel g = new Panel ();
        Panel h = new Panel ();
        Panel i = new Panel (new BorderLayout ());

        JButton start = new JButton ("Start puzzle");
        start.setActionCommand ("8");
        start.addActionListener (this);


        JLabel desc = new JLabel (createImageIcon ("Evil Exes Description.JPG"));

        JButton back = new JButton ("Back");
        back.setActionCommand ("3");
        back.addActionListener (this);

        h.add (start);
        h.add (back);
        i.add ("North", desc);
        i.add (h);
        card72.add (i);

        p_card.add ("72", card72);
    }


    public void lotsOfLoveDescription ()
    {
        card73 = new Panel (new BorderLayout ());

        Panel g = new Panel ();
        Panel h = new Panel ();
        Panel i = new Panel (new BorderLayout ());

        JButton start = new JButton ("Start puzzle");
        start.setActionCommand ("9");
        start.addActionListener (this);


        JLabel desc = new JLabel (createImageIcon ("Lots of Love Description.JPG"));

        JButton back = new JButton ("Back");
        back.setActionCommand ("4");
        back.addActionListener (this);


        h.add (start);
        h.add (back);
        i.add ("North", desc);
        i.add (h);
        card73.add (i);

        p_card.add ("73", card73);
    }


    public void islandWeddingsDescription ()
    {
        card74 = new Panel (new BorderLayout ());

        Panel g = new Panel ();
        Panel h = new Panel ();
        Panel i = new Panel (new BorderLayout ());

        JButton start = new JButton ("Start puzzle");
        start.setActionCommand ("10");
        start.addActionListener (this);


        JLabel desc = new JLabel (createImageIcon ("Island Weddings Description.JPG"));

        JButton back = new JButton ("Back");
        back.setActionCommand ("4");
        back.addActionListener (this);

        h.add (start);
        h.add (back);
        i.add ("North", desc);
        i.add (h);
        card74.add (i);

        p_card.add ("74", card74);
    }


    public void anniversaryCruisesDescription ()
    {
        card75 = new Panel (new BorderLayout ());

        Panel g = new Panel ();
        Panel h = new Panel ();
        Panel i = new Panel (new BorderLayout ());

        JButton start = new JButton ("Start puzzle");
        start.setActionCommand ("11");
        start.addActionListener (this);


        JLabel desc = new JLabel (createImageIcon ("Anniversary Cruises Description.JPG"));

        JButton back = new JButton ("Back");
        back.setActionCommand ("4");
        back.addActionListener (this);

        h.add (start);
        h.add (back);
        i.add ("North", desc);
        i.add (h);
        card75.add (i);

        p_card.add ("75", card75);
    }


    //THE NEXT 6 METHODS ARE THE CLUE SCREEN FOR EACH PUZZLE (in same order as shown above for descriptions)
    public void cluesBusyLovebirds ()
    {
        card80 = new Panel ();

        JLabel title = new JLabel (createImageIcon ("Busy Lovebirds Clues.JPG"));

        Panel g = new Panel ();
        Panel h = new Panel ();
        Panel i = new Panel ();
        Panel j = new Panel ();
        Panel k = new Panel (new GridLayout (2, 2));
        Panel l = new Panel ();
        Panel m = new Panel (new GridLayout (4, 1));
        Panel n = new Panel ();

        JLabel blankspace = new JLabel ("");

        JCheckBox num1 = new JCheckBox ("1. ");
        JTextArea clue1 = new JTextArea ("James and Elizabeth didn't go to the restaurant on consecutive days.", 3, 20);
        clue1.setBackground (new Color (236, 193, 217));
        JCheckBox num2 = new JCheckBox ("2. ");
        JTextArea clue2 = new JTextArea ("Neither of their visits to the park was on the same day as their trips\nto either the restaurant or the cinema.", 3, 20);
        clue2.setBackground (new Color (236, 193, 217));
        JCheckBox num3 = new JCheckBox ("3. ");
        JTextArea clue3 = new JTextArea ("It wasn't on Friday that the couple spent the evening at the mall,\nalthough their evening visit to the mall was later in the week than\ntheir afternoon trip to the beach.", 2, 20);
        clue3.setBackground (new Color (236, 193, 217));
        JCheckBox num4 = new JCheckBox ("4. ");
        JTextArea clue4 = new JTextArea ("James and Elizabeth's evening outing to the swimming pool was the\nday after they'd spent the afternoon at the mall, but the day before\ntheir evening trip to the cinema (which wasn't on the same day as\ntheir afternoon restaurant visit).", 4, 20);
        clue4.setBackground (new Color (236, 193, 217));
        JButton back = new JButton ("Back");
        back.setActionCommand ("6");
        back.addActionListener (this);

        g.add (num1);
        g.add (clue1);
        h.add (num2);
        h.add (clue2);
        i.add (num3);
        i.add (clue3);
        j.add (num4);
        j.add (clue4);
        k.add (g);
        k.add (h);
        k.add (i);
        k.add (j);
        l.add (back);
        n.add (blankspace);
        m.add (title);
        m.add (k);
        m.add (n);
        m.add (l);

        card80.add (m);

        p_card.add ("80", card80);
    }


    public void cluesSpeedDating ()
    {
        card81 = new Panel ();

        JLabel title = new JLabel (createImageIcon ("Speed Dating Clues.JPG"));

        Panel g = new Panel ();
        Panel h = new Panel ();
        Panel i = new Panel ();
        Panel j = new Panel ();
        Panel k = new Panel (new GridLayout (2, 2));
        Panel l = new Panel ();
        Panel m = new Panel (new GridLayout (4, 1));
        Panel n = new Panel ();

        JLabel blankspace = new JLabel ("");

        JCheckBox num1 = new JCheckBox ("1. ");
        JTextArea clue1 = new JTextArea ("Isabella's date with Carlos Kato took place earlier  \nin the week than the date with the Argentinian man, but two\ndays after she met with Paul Porter.", 3, 20);
        clue1.setBackground (new Color (236, 193, 217));
        JCheckBox num2 = new JCheckBox ("2. ");
        JTextArea clue2 = new JTextArea ("The date with Ben Jones took place more than one day \nbefore she went on a date with Jim O'Neill.                ", 2, 20);
        clue2.setBackground (new Color (236, 193, 217));
        JCheckBox num3 = new JCheckBox ("3. ");
        JTextArea clue3 = new JTextArea ("Isabella went on a date with the man from Chili later\nin the week than the date with the man from Ecuador, but   \nthe day before she met Samuel Smith from Peru.", 3, 20);
        clue3.setBackground (new Color (236, 193, 217));
        JCheckBox num4 = new JCheckBox ("4. ");
        JTextArea clue4 = new JTextArea ("Neither Ben Jones nor Paul Porter came from Brazil.  ", 1, 20);
        clue4.setBackground (new Color (236, 193, 217));
        JButton back = new JButton ("Back");
        back.setActionCommand ("7");
        back.addActionListener (this);

        g.add (num1);
        g.add (clue1);
        h.add (num2);
        h.add (clue2);
        i.add (num3);
        i.add (clue3);
        j.add (num4);
        j.add (clue4);
        k.add (g);
        k.add (h);
        k.add (i);
        k.add (j);
        l.add (back);
        n.add (blankspace);
        m.add (title);
        m.add (k);
        m.add (n);
        m.add (l);

        card81.add (m);

        p_card.add ("81", card81);

    }


    public void cluesEvilExes ()
    {
        card82 = new Panel ();

        JLabel title = new JLabel (createImageIcon ("Evil Exes Clues.JPG"));

        Panel g = new Panel ();
        Panel h = new Panel ();
        Panel i = new Panel ();
        Panel j = new Panel ();
        Panel k = new Panel (new GridLayout (3, 2));
        Panel l = new Panel ();
        Panel m = new Panel (new GridLayout (4, 1));
        Panel n = new Panel ();
        Panel o = new Panel ();

        JLabel blankspace = new JLabel ("");

        JCheckBox num1 = new JCheckBox ("1. ");
        JTextArea clue1 = new JTextArea ("Raj's head is in the same picture as Mark's body.             ", 1, 20);
        clue1.setBackground (new Color (236, 193, 217));
        JCheckBox num2 = new JCheckBox ("2. ");
        JTextArea clue2 = new JTextArea ("Raj's body is in the same picture as Frederick's legs.        ", 1, 20);
        clue2.setBackground (new Color (236, 193, 217));
        JCheckBox num3 = new JCheckBox ("3. ");
        JTextArea clue3 = new JTextArea ("Raj's legs are in the same picture as Jimmy's head.           ", 1, 20);
        clue3.setBackground (new Color (236, 193, 217));
        JCheckBox num4 = new JCheckBox ("4. ");
        JTextArea clue4 = new JTextArea ("Feng's head is in the same picture as either Frederick's body.", 1, 20);
        clue4.setBackground (new Color (236, 193, 217));
        JCheckBox num5 = new JCheckBox ("5. ");
        JTextArea clue5 = new JTextArea ("Frederick's head is in a different picture from Feng's legs.  ", 1, 20);
        clue5.setBackground (new Color (236, 193, 217));

        JButton back = new JButton ("Back");
        back.setActionCommand ("8");
        back.addActionListener (this);

        g.add (num1);
        g.add (clue1);
        h.add (num2);
        h.add (clue2);
        i.add (num3);
        i.add (clue3);
        j.add (num4);
        j.add (clue4);
        o.add (num5);
        o.add (clue5);

        k.add (g);
        k.add (h);
        k.add (i);
        k.add (j);
        k.add (o);
        l.add (back);
        n.add (blankspace);
        m.add (title);
        m.add (k);
        m.add (n);
        m.add (l);

        card82.add (m);

        p_card.add ("82", card82);

    }


    public void cluesLotsOfLove ()
    {
        card83 = new Panel ();

        JLabel title = new JLabel (createImageIcon ("Lots of Love Clues.JPG"));

        Panel g = new Panel ();
        Panel h = new Panel ();
        Panel i = new Panel ();
        Panel j = new Panel ();
        Panel k = new Panel (new GridLayout (3, 2));
        Panel l = new Panel ();
        Panel m = new Panel (new GridLayout (4, 1));
        Panel n = new Panel ();
        Panel o = new Panel ();

        JLabel blankspace = new JLabel ("");

        JCheckBox num1 = new JCheckBox ("1. ");
        JTextArea clue1 = new JTextArea ("Keith's girlfriend is one year older than Fran,  \nwhose boyfriend isn't Arthur.", 1, 20);
        clue1.setBackground (new Color (236, 193, 217));
        JCheckBox num2 = new JCheckBox ("2. ");
        JTextArea clue2 = new JTextArea ("George's girlfriend received two fewer cards than\n were sent to the nineteen-year-old.", 1, 20);
        clue2.setBackground (new Color (236, 193, 217));
        JCheckBox num3 = new JCheckBox ("3. ");
        JTextArea clue3 = new JTextArea ("Debbie received two more cards than Claire, who  \n is one year older than Debbie.", 1, 20);
        clue3.setBackground (new Color (236, 193, 217));
        JCheckBox num4 = new JCheckBox ("4. ");
        JTextArea clue4 = new JTextArea ("Glenda is the youngest of the four women. She    \ndidn't receive the highest number of cards.", 1, 20);
        clue4.setBackground (new Color (236, 193, 217));
        JCheckBox num5 = new JCheckBox ("5. ");
        JTextArea clue5 = new JTextArea ("Johnnie sent fewer cards than Arthur.", 1, 20);
        clue5.setBackground (new Color (236, 193, 217));

        JButton back = new JButton ("Back");
        back.setActionCommand ("9");
        back.addActionListener (this);

        g.add (num1);
        g.add (clue1);
        h.add (num2);
        h.add (clue2);
        i.add (num3);
        i.add (clue3);
        j.add (num4);
        j.add (clue4);
        o.add (num5);
        o.add (clue5);

        k.add (g);
        k.add (h);
        k.add (i);
        k.add (j);
        k.add (o);
        l.add (back);
        n.add (blankspace);
        m.add (title);
        m.add (k);
        m.add (n);
        m.add (l);

        card83.add (m);

        p_card.add ("83", card83);
    }


    public void cluesIslandWeddings ()
    {
        card84 = new Panel ();

        JLabel title = new JLabel (createImageIcon ("Island Weddings Clues.JPG"));

        Panel g = new Panel ();
        Panel h = new Panel ();
        Panel i = new Panel ();
        Panel j = new Panel ();
        Panel k = new Panel (new GridLayout (2, 2));
        Panel l = new Panel ();
        Panel m = new Panel (new GridLayout (4, 1));
        Panel n = new Panel ();

        JLabel blankspace = new JLabel ("");

        JCheckBox num1 = new JCheckBox ("1. ");
        JTextArea clue1 = new JTextArea ("No bride or groom married in a month that starts with the same   \nletter as that of his or her name; and no bride married a groom\nwith a name that starts with the same letter as that of her own.", 3, 20);
        clue1.setBackground (new Color (236, 193, 217));
        JCheckBox num2 = new JCheckBox ("2. ");
        JTextArea clue2 = new JTextArea ("Julia and her husband married earlier in the year than the couple\nwhose wedding took place in Tenerife.", 2, 20);
        clue2.setBackground (new Color (236, 193, 217));
        JCheckBox num3 = new JCheckBox ("3. ");
        JTextArea clue3 = new JTextArea ("The wedding in Barbados took place three months before Danny's   \nmarriage, but later than the wedding on the island of Sardinia.", 2, 20);
        clue3.setBackground (new Color (236, 193, 217));
        JCheckBox num4 = new JCheckBox ("4. ");
        JTextArea clue4 = new JTextArea ("The bride who married in Majorca isn't Sarah.", 1, 20);
        clue4.setBackground (new Color (236, 193, 217));

        JButton back = new JButton ("Back");
        back.setActionCommand ("10");
        back.addActionListener (this);

        g.add (num1);
        g.add (clue1);
        h.add (num2);
        h.add (clue2);
        i.add (num3);
        i.add (clue3);
        j.add (num4);
        j.add (clue4);

        k.add (g);
        k.add (h);
        k.add (i);
        k.add (j);
        l.add (back);
        n.add (blankspace);
        m.add (title);
        m.add (k);
        m.add (n);
        m.add (l);

        card84.add (m);

        p_card.add ("84", card84);

    }


    public void cluesAnniversaryCruises ()
    {
        card85 = new Panel ();

        JLabel title = new JLabel (createImageIcon ("Anniversary Cruises Clues.JPG"));

        Panel g = new Panel ();
        Panel h = new Panel ();
        Panel i = new Panel ();
        Panel j = new Panel ();
        Panel k = new Panel (new GridLayout (3, 2));
        Panel l = new Panel ();
        Panel m = new Panel (new GridLayout (4, 1));
        Panel n = new Panel ();
        Panel o = new Panel ();
        Panel p = new Panel ();

        JLabel blankspace = new JLabel ("");

        JCheckBox num1 = new JCheckBox ("1. ");
        JTextArea clue1 = new JTextArea ("Denise and her husband have been married for longer than  \n 25 years, so they aren't celebrating their silver wedding\n anniversary.", 3, 20);
        clue1.setBackground (new Color (236, 193, 217));
        JCheckBox num2 = new JCheckBox ("2. ");
        JTextArea clue2 = new JTextArea ("Grace isn't married to Arthur; and Richard isn't married  \n to Camilla.", 2, 20);
        clue2.setBackground (new Color (236, 193, 217));
        JCheckBox num3 = new JCheckBox ("3. ");
        JTextArea clue3 = new JTextArea ("Felicity and her husband are enjoying their cruise aboard \n the Ocean Winner.", 2, 20);
        clue3.setBackground (new Color (236, 193, 217));
        JCheckBox num4 = new JCheckBox ("4. ");
        JTextArea clue4 = new JTextArea ("Richard is aboard the Sea Sprite, but not with Grace.", 1, 20);
        clue4.setBackground (new Color (236, 193, 217));
        JCheckBox num5 = new JCheckBox ("5. ");
        JTextArea clue5 = new JTextArea ("The couple celebrating their ruby wedding anniversary are \non the Ocean Breeze, cruising the Mediterranean, unlike  \nPaul and his wife.", 3, 20);
        clue5.setBackground (new Color (236, 193, 217));
        JCheckBox num6 = new JCheckBox ("6. ");
        JTextArea clue6 = new JTextArea ("Arthur and his wife (who isn't Felicity) are celebrating \ntheir diamond wedding anniversary.", 2, 20);
        clue6.setBackground (new Color (236, 193, 217));

        JButton back = new JButton ("Back");
        back.setActionCommand ("11");
        back.addActionListener (this);

        g.add (num1);
        g.add (clue1);
        h.add (num2);
        h.add (clue2);
        i.add (num3);
        i.add (clue3);
        j.add (num4);
        j.add (clue4);
        o.add (num5);
        o.add (clue5);
        p.add (num6);
        p.add (clue6);

        k.add (g);
        k.add (h);
        k.add (i);
        k.add (j);
        k.add (o);
        k.add (p);
        l.add (back);
        n.add (blankspace);
        m.add (title);
        m.add (k);
        m.add (n);
        m.add (l);

        card85.add (m);

        p_card.add ("85", card85);

    }


    public void busyLovebirds ()  //Busy Lovebirds puzzle screen
    {
        card6 = new Panel (new BorderLayout ());

        JButton grid[] = new JButton [100]; //declaring grid used in puzzle

        JLabel title = new JLabel ("Busy Lovebirds");
        title.setFont (new Font ("Edwardian Script ITC", Font.BOLD, 60));
        title.setForeground (new Color (158, 58, 131));

        JButton newPuzzle = new JButton ("Back");
        newPuzzle.setActionCommand ("3");
        newPuzzle.addActionListener (this);
        JButton reset = new JButton ("Reset");
        reset.setActionCommand ("reset");
        reset.addActionListener (this);
        JButton check = new JButton ("Check your answers");
        check.setActionCommand ("60");
        check.addActionListener (this);
        JButton clues = new JButton ("Clues");
        clues.setActionCommand ("80");
        clues.addActionListener (this);

        JLabel legend = new JLabel (createImageIcon ("Legend.jpg"));
        JLabel topgrid = new JLabel (createImageIcon ("EASY Busy Lovebirds Top.jpg"));
        JLabel leftgrid = new JLabel (createImageIcon ("EASY Busy Lovebirds Left.jpg")); //grid pictures

        Panel g = new Panel (new GridLayout (10, 10));
        Panel h = new Panel ();
        Panel j = new Panel ();
        Panel k = new Panel (new BorderLayout ());
        Panel l = new Panel ();
        Panel m = new Panel (new GridLayout (4, 1));

        Panel s = new Panel ();
        Panel t = new Panel ();
        Panel u = new Panel ();
        Panel v = new Panel ();
        Panel n = new Panel (new BorderLayout ());
        Panel o = new Panel ();
        Panel p = new Panel ();


        for (int i = 0 ; i < easygrid.length ; i++) //to change array value/button image when grid buttons are clicked
        {
            easygrid [i] = new JButton (createImageIcon ("Blank.jpg"));
            easygrid [i].setPreferredSize (new Dimension (23, 23));
            g.add (easygrid [i]);
            easygrid [i].setActionCommand ("click" + i);
            easygrid [i].addActionListener (this);
        }

        for (int i = 55 ; i < 60 ; i++) //make certain buttons invisible (they're unneeded)
            easygrid [i].setVisible (false);
        for (int i = 65 ; i < 70 ; i++)
            easygrid [i].setVisible (false);
        for (int i = 75 ; i < 80 ; i++)
            easygrid [i].setVisible (false);
        for (int i = 85 ; i < 90 ; i++)
            easygrid [i].setVisible (false);
        for (int i = 95 ; i < 100 ; i++)
            easygrid [i].setVisible (false);

        h.add (legend);
        h.add (topgrid);

        j.add (leftgrid);
        j.add (g);

        k.add ("North", h);
        k.add ("Center", j);


        l.add (title);

        m.add (clues);
        m.add (check);
        m.add (newPuzzle);
        m.add (reset);

        Panel middlepan = new Panel ();
        middlepan.add (k);
        middlepan.add (m);
        card6.add ("North", l);

        card6.add ("Center", middlepan);

        p_card.add ("6", card6);
    }




    public void speedDating ()  //Speed Dating puzzle
    {
        card7 = new Panel (new BorderLayout ());
        JButton grid1[] = new JButton [100]; //grid used in puzzle

        JLabel title = new JLabel ("Speed Dating");
        title.setFont (new Font ("Edwardian Script ITC", Font.BOLD, 60));
        title.setForeground (new Color (158, 58, 131));

        JButton newPuzzle = new JButton ("Back");
        newPuzzle.setActionCommand ("3");
        newPuzzle.addActionListener (this);
        JButton reset = new JButton ("Reset");
        reset.setActionCommand ("reseu");
        reset.addActionListener (this);
        JButton check = new JButton ("Check your answers");
        check.setActionCommand ("61");
        check.addActionListener (this);
        JButton clues = new JButton ("Clues");
        clues.setActionCommand ("81");
        clues.addActionListener (this);

        JLabel legend = new JLabel (createImageIcon ("Legend.jpg"));
        JLabel topgrid = new JLabel (createImageIcon ("EASY Speed Dating Top.jpg"));
        JLabel leftgrid = new JLabel (createImageIcon ("EASY Speed Dating Left.jpg"));

        Panel g = new Panel (new GridLayout (10, 10));
        Panel h = new Panel ();
        Panel j = new Panel ();
        Panel k = new Panel (new BorderLayout ());
        Panel l = new Panel ();
        Panel m = new Panel (new GridLayout (4, 1));
        Panel n = new Panel (new BorderLayout ());

        for (int i = 0 ; i < easygrid1.length ; i++) //to change array value/button image when grid buttons are clicked
        {
            easygrid1 [i] = new JButton (createImageIcon ("Blank.jpg"));
            easygrid1 [i].setPreferredSize (new Dimension (23, 23));
            g.add (easygrid1 [i]);
            easygrid1 [i].setActionCommand ("clicl" + i);
            easygrid1 [i].addActionListener (this);
        }
        for (int i = 55 ; i < 60 ; i++) //invisible buttons
            easygrid1 [i].setVisible (false);
        for (int i = 65 ; i < 70 ; i++)
            easygrid1 [i].setVisible (false);
        for (int i = 75 ; i < 80 ; i++)
            easygrid1 [i].setVisible (false);
        for (int i = 85 ; i < 90 ; i++)
            easygrid1 [i].setVisible (false);
        for (int i = 95 ; i < 100 ; i++)
            easygrid1 [i].setVisible (false);

        h.add (legend);
        h.add (topgrid);

        j.add (leftgrid);
        j.add (g);

        k.add ("North", h);
        k.add ("Center", j);

        l.add (title);

        m.add (clues);
        m.add (check);
        m.add (newPuzzle);
        m.add (reset);

        card7.add ("North", l);
        card7.add ("East", m);
        card7.add ("Center", k);

        Panel middlepan = new Panel ();
        middlepan.add (k);
        middlepan.add (m);
        card7.add ("North", l);

        card7.add ("Center", middlepan);

        p_card.add ("7", card7);
    }


    public void evilExes ()  //Evil Exes puzzle
    {
        card8 = new Panel (new BorderLayout ());
        JButton grid[] = new JButton [100]; //grid used in puzzle

        JButton newPuzzle = new JButton ("Back");
        newPuzzle.setActionCommand ("3");
        newPuzzle.addActionListener (this);

        JLabel title = new JLabel ("Evil Exes");
        title.setFont (new Font ("Chiller", Font.BOLD, 60));
        title.setForeground (new Color (158, 58, 131));

        JButton reset = new JButton ("Reset");
        reset.setActionCommand ("resev");
        reset.addActionListener (this);
        JButton check = new JButton ("Check your answers");
        check.setActionCommand ("62");
        check.addActionListener (this);
        JButton clues = new JButton ("Clues");
        clues.setActionCommand ("82");
        clues.addActionListener (this);

        JLabel legend = new JLabel (createImageIcon ("Legend.jpg"));
        JLabel topgrid = new JLabel (createImageIcon ("EASY Evil Exes Top.jpg"));
        JLabel leftgrid = new JLabel (createImageIcon ("EASY Evil Exes Left.jpg")); //grid labels

        Panel g = new Panel (new GridLayout (10, 10));
        Panel h = new Panel ();
        Panel j = new Panel ();
        Panel k = new Panel (new BorderLayout ());
        Panel l = new Panel ();
        Panel m = new Panel (new GridLayout (4, 1));
        Panel n = new Panel (new BorderLayout ());

        for (int i = 0 ; i < easygrid2.length ; i++) //to change array value/button image when grid buttons are clicked
        {
            easygrid2 [i] = new JButton (createImageIcon ("Blank.jpg"));
            easygrid2 [i].setPreferredSize (new Dimension (23, 23));
            g.add (easygrid2 [i]);
            easygrid2 [i].setActionCommand ("clicm" + i);
            easygrid2 [i].addActionListener (this);
        }
        for (int i = 55 ; i < 60 ; i++) //invisible buttons
            easygrid2 [i].setVisible (false);
        for (int i = 65 ; i < 70 ; i++)
            easygrid2 [i].setVisible (false);
        for (int i = 75 ; i < 80 ; i++)
            easygrid2 [i].setVisible (false);
        for (int i = 85 ; i < 90 ; i++)
            easygrid2 [i].setVisible (false);
        for (int i = 95 ; i < 100 ; i++)
            easygrid2 [i].setVisible (false);

        h.add (legend);
        h.add (topgrid);

        j.add (leftgrid);
        j.add (g);

        k.add ("North", h);
        k.add ("Center", j);

        l.add (title);

        m.add (clues);
        m.add (check);
        m.add (newPuzzle);
        m.add (reset);

        card8.add ("North", l);
        card8.add ("East", m);
        card8.add ("Center", k);

        Panel middlepan = new Panel ();
        middlepan.add (k);
        middlepan.add (m);
        card8.add ("North", l);
        card8.add ("Center", middlepan);

        p_card.add ("8", card8);
    }


    public void lotsOfLove ()  //Lots of Love puzzle
    {
        card9 = new Panel (new BorderLayout ());
        JButton grid[] = new JButton [144];

        JButton newPuzzle = new JButton ("Back");
        newPuzzle.setActionCommand ("4");
        newPuzzle.addActionListener (this);

        JLabel title = new JLabel ("Lots of Love");
        title.setFont (new Font ("Brush Script MT", Font.BOLD, 60));
        title.setForeground (new Color (158, 58, 131));

        JButton reset = new JButton ("Reset");
        reset.setActionCommand ("resew");
        reset.addActionListener (this);
        JButton check = new JButton ("Check your answers");
        check.setActionCommand ("63");
        check.addActionListener (this);
        JButton clues = new JButton ("Clues");
        clues.setActionCommand ("83");
        clues.addActionListener (this);

        JLabel legend = new JLabel (createImageIcon ("Legend.jpg"));
        JLabel topgrid = new JLabel (createImageIcon ("HARD Lots of Love Top.jpg"));
        JLabel leftgrid = new JLabel (createImageIcon ("HARD Lots of Love Left.jpg")); //grid labels

        Panel g = new Panel (new GridLayout (12, 12));
        Panel h = new Panel ();
        Panel j = new Panel ();
        Panel k = new Panel (new BorderLayout ());
        Panel l = new Panel ();
        Panel m = new Panel (new GridLayout (4, 1));
        Panel n = new Panel (new BorderLayout ());

        for (int i = 0 ; i < hardgrid.length ; i++)
        {
            hardgrid [i] = new JButton (createImageIcon ("Blank.jpg")); //to change array value/button image when grid buttons are clicked
            hardgrid [i].setPreferredSize (new Dimension (27, 27));
            g.add (hardgrid [i]);
            hardgrid [i].setActionCommand ("clicn" + i);
            hardgrid [i].addActionListener (this);
        }
        for (int i = 56 ; i < 60 ; i++)
            hardgrid [i].setVisible (false); //invisble buttons
        for (int i = 68 ; i < 72 ; i++)
            hardgrid [i].setVisible (false);
        for (int i = 80 ; i < 84 ; i++)
            hardgrid [i].setVisible (false);
        for (int i = 92 ; i < 96 ; i++)
            hardgrid [i].setVisible (false);
        for (int i = 100 ; i < 108 ; i++)
            hardgrid [i].setVisible (false);
        for (int i = 112 ; i < 120 ; i++)
            hardgrid [i].setVisible (false);
        for (int i = 124 ; i < 132 ; i++)
            hardgrid [i].setVisible (false);
        for (int i = 136 ; i < 144 ; i++)
            hardgrid [i].setVisible (false);

        h.add (legend);
        h.add (topgrid);

        j.add (leftgrid);
        j.add (g);

        k.add ("North", h);
        k.add ("Center", j);

        l.add (title);

        m.add (clues);
        m.add (check);
        m.add (newPuzzle);
        m.add (reset);

        card9.add ("North", l);
        card9.add ("South", m);
        card9.add ("Center", k);

        Panel middlepan = new Panel ();
        middlepan.add (k);
        middlepan.add (m);
        card9.add ("North", l);
        card9.add ("Center", middlepan);


        p_card.add ("9", card9);
    }


    public void islandWeddings ()  //Island Weddings puzzle
    {
        card10 = new Panel (new BorderLayout ());
        JButton grid[] = new JButton [144]; //grid used in puzzle

        JButton newPuzzle = new JButton ("Back");
        newPuzzle.setActionCommand ("4");
        newPuzzle.addActionListener (this);

        JLabel title = new JLabel ("Island Weddings");
      title.setFont (new Font ("Informal Roman", Font.BOLD, 60));
        title.setForeground (new Color (158, 58, 131));

        JButton reset = new JButton ("Reset");
        reset.setActionCommand ("resey");
        reset.addActionListener (this);
        JButton check = new JButton ("Check your answers");
        check.setActionCommand ("64");
        check.addActionListener (this);
        JButton clues = new JButton ("Clues");
        clues.setActionCommand ("84");
        clues.addActionListener (this);

        JLabel legend = new JLabel (createImageIcon ("Legend.jpg"));
        JLabel topgrid = new JLabel (createImageIcon ("HARD Island Weddings Top.jpg"));
        JLabel leftgrid = new JLabel (createImageIcon ("HARD Island Weddings Left.jpg"));

        Panel g = new Panel (new GridLayout (12, 12));
        Panel h = new Panel ();
        Panel j = new Panel ();
        Panel k = new Panel (new BorderLayout ());
        Panel l = new Panel ();
        Panel m = new Panel (new GridLayout (4, 1));
        Panel n = new Panel (new BorderLayout ());

        for (int i = 0 ; i < hardgrid1.length ; i++) //to change array value/button image when grid buttons are clicked
        {
            hardgrid1 [i] = new JButton (createImageIcon ("Blank.jpg"));
            hardgrid1 [i].setPreferredSize (new Dimension (27, 27));
            g.add (hardgrid1 [i]);
            hardgrid1 [i].setActionCommand ("clico" + i);
            hardgrid1 [i].addActionListener (this);
        }
        for (int i = 56 ; i < 60 ; i++) //invisible buttons
            hardgrid1 [i].setVisible (false);
        for (int i = 68 ; i < 72 ; i++)
            hardgrid1 [i].setVisible (false);
        for (int i = 80 ; i < 84 ; i++)
            hardgrid1 [i].setVisible (false);
        for (int i = 92 ; i < 96 ; i++)
            hardgrid1 [i].setVisible (false);
        for (int i = 100 ; i < 108 ; i++)
            hardgrid1 [i].setVisible (false);
        for (int i = 112 ; i < 120 ; i++)
            hardgrid1 [i].setVisible (false);
        for (int i = 124 ; i < 132 ; i++)
            hardgrid1 [i].setVisible (false);
        for (int i = 136 ; i < 144 ; i++)
            hardgrid1 [i].setVisible (false);

        h.add (legend);
        h.add (topgrid);

        j.add (leftgrid);
        j.add (g);

        k.add ("North", h);
        k.add ("Center", j);

        l.add (title);

        m.add (clues);
        m.add (check);
        m.add (newPuzzle);
        m.add (reset);

        card10.add ("North", l);
        card10.add ("South", m);
        card10.add ("Center", k);

        Panel middlepan = new Panel ();
        middlepan.add (k);
        middlepan.add (m);
        card10.add ("North", l);
        card10.add ("Center", middlepan);

        p_card.add ("10", card10);
    }


    public void anniversaryCruises ()  //Anniversary Cruises puzzle
    {
        card11 = new Panel (new BorderLayout ());
        JButton grid[] = new JButton [144]; //grid used in puzzle

        JButton newPuzzle = new JButton ("Back");
        newPuzzle.setActionCommand ("4");
        newPuzzle.addActionListener (this);

        JLabel title = new JLabel ("Anniversary Cruises");
      title.setFont (new Font ("Edwardian Script ITC", Font.PLAIN, 60));
        title.setForeground (new Color (158, 58, 131));

        JButton reset = new JButton ("Reset");
        reset.setActionCommand ("resez");
        reset.addActionListener (this);
        JButton check = new JButton ("Check your answers");
        check.setActionCommand ("65");
        check.addActionListener (this);
        JButton clues = new JButton ("Clues");
        clues.setActionCommand ("85");
        clues.addActionListener (this);

        JLabel legend = new JLabel (createImageIcon ("Legend.jpg"));
        JLabel topgrid = new JLabel (createImageIcon ("HARD Lots of Love Top.jpg"));
        JLabel leftgrid = new JLabel (createImageIcon ("HARD Lots of Love Left.jpg")); //grid labels

        Panel g = new Panel (new GridLayout (12, 12));
        Panel h = new Panel ();
        Panel j = new Panel ();
        Panel k = new Panel (new BorderLayout ());
        Panel l = new Panel ();
        Panel m = new Panel (new GridLayout (4, 1));
        Panel n = new Panel (new BorderLayout ());

        for (int i = 0 ; i < hardgrid2.length ; i++) //to change array value/button image when grid buttons are clicked
        {
            hardgrid2 [i] = new JButton (createImageIcon ("Blank.jpg"));
            hardgrid2 [i].setPreferredSize (new Dimension (27, 27));
            g.add (hardgrid2 [i]);
            hardgrid2 [i].setActionCommand ("clicp" + i);
            hardgrid2 [i].addActionListener (this);
        }

        for (int i = 56 ; i < 60 ; i++) //invisible buttons
            hardgrid2 [i].setVisible (false);
        for (int i = 68 ; i < 72 ; i++)
            hardgrid2 [i].setVisible (false);
        for (int i = 80 ; i < 84 ; i++)
            hardgrid2 [i].setVisible (false);
        for (int i = 92 ; i < 96 ; i++)
            hardgrid2 [i].setVisible (false);
        for (int i = 100 ; i < 108 ; i++)
            hardgrid2 [i].setVisible (false);
        for (int i = 112 ; i < 120 ; i++)
            hardgrid2 [i].setVisible (false);
        for (int i = 124 ; i < 132 ; i++)
            hardgrid2 [i].setVisible (false);
        for (int i = 136 ; i < 144 ; i++)
            hardgrid2 [i].setVisible (false);

        h.add (legend);
        h.add (topgrid);

        j.add (leftgrid);
        j.add (g);

        k.add ("North", h);
        k.add ("Center", j);

        l.add (title);

        m.add (clues);
        m.add (check);
        m.add (newPuzzle);
        m.add (reset);

        card11.add ("North", l);
        card11.add ("South", m);
        card11.add ("Center", k);

        Panel middlepan = new Panel ();
        middlepan.add (k);
        middlepan.add (m);
        card11.add ("North", l);
        card11.add ("Center", middlepan);

        p_card.add ("11", card11);
    }


    public void actionPerformed (ActionEvent e)
    {
        if (e.getActionCommand ().equals ("1")) //menu/main screen
            cdLayout.show (p_card, "1");
        else if (e.getActionCommand ().equals ("2")) //instructions
            cdLayout.show (p_card, "2");
        else if (e.getActionCommand ().equals ("3")) //easy puzzles
            cdLayout.show (p_card, "3");
        else if (e.getActionCommand ().equals ("4")) //hard puzzles
            cdLayout.show (p_card, "4");
        else if (e.getActionCommand ().equals ("easyCombo"))
        { //To draw the name that is in the easyCombo combo box
            JComboBox cb = (JComboBox) e.getSource ();
            String choose = (String) cb.getSelectedItem ();
            if (choose == "Busy Lovebirds") //go to Busy Lovebirds puzzle description screen
                cdLayout.show (p_card, "70");
            else if (choose == "Speed Dating") //go to Speed Dating puzzle description screen
                cdLayout.show (p_card, "71");
            else if (choose == "Evil Exes") //go to Evil Exes puzzle description screen
                cdLayout.show (p_card, "72");
        }
        else if (e.getActionCommand ().equals ("hardCombo"))
        { //To draw the name that is in the hardCombo combo box
            JComboBox cb = (JComboBox) e.getSource ();
            String choose1 = (String) cb.getSelectedItem ();
            if (choose1 == "Lots of Love") //go to Lots of Love puzzle description screen
                cdLayout.show (p_card, "73");
            else if (choose1 == "Island Weddings") //go to Island Weddings puzzle description screen
                cdLayout.show (p_card, "74");
            else if (choose1 == "Anniversary Cruises") //go to Anniversary Cruises puzzle description screen
                cdLayout.show (p_card, "75");
        }
        else if (e.getActionCommand ().equals ("6")) //Busy Lovebirds Puzzle Screen
            cdLayout.show (p_card, "6");
        else if (e.getActionCommand ().equals ("7")) //Speed Dating Puzzle Screen
            cdLayout.show (p_card, "7");
        else if (e.getActionCommand ().equals ("8")) //Evil Exes Puzzle Screen
            cdLayout.show (p_card, "8");
        else if (e.getActionCommand ().equals ("9")) //Lots of Love Puzzle Screen
            cdLayout.show (p_card, "9");
        else if (e.getActionCommand ().equals ("10")) //Island Weddings Puzzle Screen
            cdLayout.show (p_card, "10");
        else if (e.getActionCommand ().equals ("11")) //Anniversary Cruises Puzzle Screen
            cdLayout.show (p_card, "11");
        else if (e.getActionCommand ().equals ("70")) //Busy Lovebirds puzzle description screen
            cdLayout.show (p_card, "70");
        else if (e.getActionCommand ().equals ("71")) //Speed Dating puzzle description screen
            cdLayout.show (p_card, "71");
        else if (e.getActionCommand ().equals ("72")) //Evil Exes puzzle description screen
            cdLayout.show (p_card, "72");
        else if (e.getActionCommand ().equals ("73")) //Lots of Love puzzle description screen
            cdLayout.show (p_card, "73");
        else if (e.getActionCommand ().equals ("74")) //Island Weddings puzzle description screen
            cdLayout.show (p_card, "74");
        else if (e.getActionCommand ().equals ("75")) //Anniversary Cruises puzzle description screen
            cdLayout.show (p_card, "75");
        else if (e.getActionCommand ().equals ("60")) //check answers for Busy Lovebirds puzzle
            busyLovebirdsAnswers ();
        else if (e.getActionCommand ().equals ("61")) //check answers for Speed Dating puzzle
            speedDatingAnswers ();
        else if (e.getActionCommand ().equals ("62")) //check answers for Evil Exes puzzle
            evilExesAnswers ();
        else if (e.getActionCommand ().equals ("63")) //check answers for Lots of Love puzzle
            lotsOfLoveAnswers ();
        else if (e.getActionCommand ().equals ("64")) //check answers for Island Weddings puzzle
            islandWeddingsAnswers ();
        else if (e.getActionCommand ().equals ("65")) //check answers for Anniversary Cruises puzzle
            anniversaryCruisesAnswers ();
        else if (e.getActionCommand ().equals ("80")) //clues for Busy Lovebirds puzzle
            cdLayout.show (p_card, "80");
        else if (e.getActionCommand ().equals ("81")) //clues for Speed Dating puzzle
            cdLayout.show (p_card, "81");
        else if (e.getActionCommand ().equals ("82")) //clues for Evil Exes puzzle
            cdLayout.show (p_card, "82");
        else if (e.getActionCommand ().equals ("83")) //clues for Lots of Love puzzle
            cdLayout.show (p_card, "83");
        else if (e.getActionCommand ().equals ("84")) //clues for Island Weddings puzzle
            cdLayout.show (p_card, "84");
        else if (e.getActionCommand ().equals ("85")) //clues for Anniversary puzzle
            cdLayout.show (p_card, "85");
        else if (e.getActionCommand ().equals ("reset")) //reset Busy Lovebirds
        {
            int i = 0;
            for (int j = 0 ; j < 10 ; j++)
            {
                for (int k = 0 ; k < 10 ; k++)
                {
                    a [j] [k] = 0; //set all array values back to 0 (which will show blank image)
                    easygrid [i].setIcon (createImageIcon ("Blank.JPG")); //set each button back to blank image
                    i++;
                }
            }
        }

        else if (e.getActionCommand ().equals ("reseu")) //reset Speed Dating
        {
            int i = 0;
            for (int j = 0 ; j < 10 ; j++)
            {
                for (int k = 0 ; k < 10 ; k++)
                {
                    a1 [j] [k] = 0; //set all array values back to 0 (which will show blank image)
                    easygrid1 [i].setIcon (createImageIcon ("Blank.JPG")); //set each button back to blank image
                    i++;
                }
            }
        }

        else if (e.getActionCommand ().equals ("resev")) //reset Evil Exes
        {
            int i = 0;
            for (int j = 0 ; j < 12 ; j++)
            {
                for (int k = 0 ; k < 12 ; k++)
                {
                    a2 [j] [k] = 0; //set all array values back to 0 (which will show blank image)
                    easygrid2 [i].setIcon (createImageIcon ("Blank.JPG")); //set each button back to blank image
                    i++;
                }
            }
        }

        else if (e.getActionCommand ().equals ("resew")) //reset Lots of Love
        {
            int i = 0;
            for (int j = 0 ; j < 12 ; j++)
            {
                for (int k = 0 ; k < 12 ; k++)
                {
                    b [j] [k] = 0; //set all array values back to 0 (which will show blank image)
                    hardgrid [i].setIcon (createImageIcon ("Blank.JPG")); //set each button back to blank image
                    i++;
                }
            }
        }

        else if (e.getActionCommand ().equals ("resey")) //reset Island Weddings
        {
            int i = 0;
            for (int j = 0 ; j < 12 ; j++)
            {
                for (int k = 0 ; k < 12 ; k++)
                {
                    b1 [j] [k] = 0; //set all array values back to 0 (which will show blank image)
                    hardgrid1 [i].setIcon (createImageIcon ("Blank.JPG")); //set each button back to blank image
                    i++;
                }
            }
        }

        else if (e.getActionCommand ().equals ("resez")) //reset Anniversary Cruises
        {
            int i = 0;
            for (int j = 0 ; j < 12 ; j++)
            {
                for (int k = 0 ; k < 12 ; k++)
                {
                    b2 [j] [k] = 0; //set all array values back to 0 (which will show blank image)
                    hardgrid2 [i].setIcon (createImageIcon ("Blank.JPG")); //set each button back to blank image
                    i++;
                }
            }
        }


        else if (e.getActionCommand ().substring (0, 5).equals ("click")) //to set grid array values when puzzle grid buttons are clicked
        {
            int pos = Integer.parseInt (e.getActionCommand ().substring (5, e.getActionCommand ().length ()));

            int j = pos / 10;
            int k = pos % 10;

            if (a [j] [k] == 0)
                a [j] [k] = 1; //if image is blank, change to an 'X'
            else if (a [j] [k] == 1)
                a [j] [k] = 2; //if image is an 'X', change to an 'O'
            else if (a [j] [k] == 2)
                a [j] [k] = 0; //if image is an 'O', change to blank image

            draw ();
        }
        else if (e.getActionCommand ().substring (0, 5).equals ("clicl")) //to set grid array values when puzzle grid buttons are clicked
        {
            int pos = Integer.parseInt (e.getActionCommand ().substring (5, e.getActionCommand ().length ()));

            int j = pos / 10;
            int k = pos % 10;

            if (a1 [j] [k] == 0) //if image is blank, change to an 'X'
                a1 [j] [k] = 1;
            else if (a1 [j] [k] == 1) //if image is an 'X', change to an 'O'
                a1 [j] [k] = 2;
            else if (a1 [j] [k] == 2) //if image is an 'O', change to blank image
                a1 [j] [k] = 0;

            draw1 ();
        }

        else if (e.getActionCommand ().substring (0, 5).equals ("clicm")) //to set grid array values when puzzle grid buttons are clicked
        {
            int pos = Integer.parseInt (e.getActionCommand ().substring (5, e.getActionCommand ().length ()));

            int j = pos / 10;
            int k = pos % 10;

            if (a2 [j] [k] == 0) //if image is blank, change to an 'X'
                a2 [j] [k] = 1;
            else if (a2 [j] [k] == 1) //if image is an 'X', change to an 'O'
                a2 [j] [k] = 2;
            else if (a2 [j] [k] == 2) //if image is an 'O', change to blank image
                a2 [j] [k] = 0;

            draw2 ();
        }

        else if (e.getActionCommand ().substring (0, 5).equals ("clicn")) //to set grid array values when puzzle grid buttons are clicked
        {
            int pos = Integer.parseInt (e.getActionCommand ().substring (5, e.getActionCommand ().length ()));

            int j = pos / 12;
            int k = pos % 12;

            if (b [j] [k] == 0) //if image is blank, change to an 'X'
                b [j] [k] = 1;
            else if (b [j] [k] == 1) //if image is an 'X', change to an 'O'
                b [j] [k] = 2;
            else if (b [j] [k] == 2) //if image is an 'O', change to blank image
                b [j] [k] = 0;

            draw3 ();
        }
        else if (e.getActionCommand ().substring (0, 5).equals ("clico")) //to set grid array values when puzzle grid buttons are clicked
        {
            int pos = Integer.parseInt (e.getActionCommand ().substring (5, e.getActionCommand ().length ()));

            int j = pos / 12;
            int k = pos % 12;

            if (b1 [j] [k] == 0) //if image is blank, change to an 'X'
                b1 [j] [k] = 1;
            else if (b1 [j] [k] == 1) //if image is an 'X', change to an 'O'
                b1 [j] [k] = 2;
            else if (b1 [j] [k] == 2) //if image is an 'O', change to blank image
                b [j] [k] = 0;

            draw4 ();
        }

        else if (e.getActionCommand ().substring (0, 5).equals ("clicp")) //to set grid array values when puzzle grid buttons are clicked
        {
            int pos = Integer.parseInt (e.getActionCommand ().substring (5, e.getActionCommand ().length ()));

            int j = pos / 12;
            int k = pos % 12;

            if (b2 [j] [k] == 0) //if image is blank, change to an 'X'
                b2 [j] [k] = 1;
            else if (b2 [j] [k] == 1) //if image is an 'X', change to an 'O'
                b2 [j] [k] = 2;
            else if (b2 [j] [k] == 2) //if image is an 'O', change to blank image
                b2 [j] [k] = 0;

            draw5 ();
        }

        else if (e.getActionCommand ().equals ("ExitGame")) //exit game
            System.exit (0);
    }





    public void draw ()  //to change images in Busy Lovebirds puzzle grid buttons when clicked
    {
        int i = 0;
        for (int j = 0 ; j < 10 ; j++)
        {
            for (int k = 0 ; k < 10 ; k++)
            {
                if (a [j] [k] == 0)
                    easygrid [i].setIcon (createImageIcon ("Blank.JPG"));
                else if (a [j] [k] == 1)
                    easygrid [i].setIcon (createImageIcon ("X.jpg"));
                else if (a [j] [k] == 2)
                    easygrid [i].setIcon (createImageIcon ("O.jpg"));
                i++;
            }
        }
    }


    public void draw1 ()  //to change images in Speed Dating puzzle grid buttons when clicked
    {
        int i = 0;
        for (int j = 0 ; j < 10 ; j++)
        {
            for (int k = 0 ; k < 10 ; k++)
            {
                if (a1 [j] [k] == 0)
                    easygrid1 [i].setIcon (createImageIcon ("Blank.JPG"));
                else if (a1 [j] [k] == 1)
                    easygrid1 [i].setIcon (createImageIcon ("X.jpg"));
                else if (a1 [j] [k] == 2)
                    easygrid1 [i].setIcon (createImageIcon ("O.jpg"));
                i++;
            }
        }
    }


    public void draw2 ()  //to change images in Evil Exes puzzle grid buttons when clicked
    {
        int i = 0;
        for (int j = 0 ; j < 10 ; j++)
        {
            for (int k = 0 ; k < 10 ; k++)
            {
                if (a2 [j] [k] == 0)
                    easygrid2 [i].setIcon (createImageIcon ("Blank.JPG"));
                else if (a2 [j] [k] == 1)
                    easygrid2 [i].setIcon (createImageIcon ("X.jpg"));
                else if (a2 [j] [k] == 2)
                    easygrid2 [i].setIcon (createImageIcon ("O.jpg"));
                i++;
            }
        }
    }


    public void draw3 ()  //to change images in Lots of Love puzzle grid buttons when clicked
    {
        int i = 0;
        for (int j = 0 ; j < 12 ; j++)
        {
            for (int k = 0 ; k < 12 ; k++)
            {
                if (b [j] [k] == 0)
                    hardgrid [i].setIcon (createImageIcon ("Blank.JPG"));
                else if (b [j] [k] == 1)
                    hardgrid [i].setIcon (createImageIcon ("X.jpg"));
                else if (b [j] [k] == 2)
                    hardgrid [i].setIcon (createImageIcon ("O.jpg"));
                i++;
            }
        }
    }


    public void draw4 ()  //to change images in Island Weddings puzzle grid buttons when clicked
    {
        int i = 0;
        for (int j = 0 ; j < 12 ; j++)
        {
            for (int k = 0 ; k < 12 ; k++)
            {
                if (b1 [j] [k] == 0)
                    hardgrid1 [i].setIcon (createImageIcon ("Blank.JPG"));
                else if (b1 [j] [k] == 1)
                    hardgrid1 [i].setIcon (createImageIcon ("X.jpg"));
                else if (b1 [j] [k] == 2)
                    hardgrid1 [i].setIcon (createImageIcon ("O.jpg"));
                i++;
            }
        }
    }



    public void draw5 ()  //to change images in Anniversary Cruises puzzle grid buttons when clicked
    {
        int i = 0;
        for (int j = 0 ; j < 12 ; j++)
        {
            for (int k = 0 ; k < 12 ; k++)
            {
                if (b2 [j] [k] == 0)
                    hardgrid2 [i].setIcon (createImageIcon ("Blank.JPG"));
                else if (b2 [j] [k] == 1)
                    hardgrid2 [i].setIcon (createImageIcon ("X.jpg"));
                else if (b2 [j] [k] == 2)
                    hardgrid2 [i].setIcon (createImageIcon ("O.jpg"));
                i++;
            }
        }
    }


    public void busyLovebirdsAnswers ()  //check Busy Lovebirds answers
    {
        if ((a [0] [2] == 2) && (a [0] [8] == 2) && (a [1] [1] == 2) && (a [1] [9] == 2) && (a [2] [4] == 2) && (a [2] [5] == 2) && (a [3] [3] == 2) && (a [3] [7] == 2) && (a [4] [0] == 2) && (a [4] [6] == 2) && (a [5] [4] == 2) && (a [6] [0] == 2) && (a [7] [3] == 2) && (a [8] [2] == 2) && (a [9] [1] == 2))
        {
            int x = 0;
            for (int j = 0 ; j < 10 ; j++)
            {
                for (int k = 0 ; k < 10 ; k++)
                {
                    if (a [j] [k] == 2) //check if all of the array elements have a value of 2 (which would mean that the player set an 'O' in that element/button
                        x++;
                }
            }
            if (x == 15) //if all elements have a value of 2 and there are exactly 15, give congratulations message
                JOptionPane.showMessageDialog (null, "You have finished this puzzle successfully!\nNow try another!", "Success", JOptionPane.INFORMATION_MESSAGE);
            else //if there are more than 15, then tell player they made a mistake
                JOptionPane.showMessageDialog (null, "You have made a mistake. Please check again.", "Failed", JOptionPane.INFORMATION_MESSAGE);
        }
        else //mistake message
        {
            JOptionPane.showMessageDialog (null, "You have made a mistake. Please check again.", "Failed", JOptionPane.INFORMATION_MESSAGE);
        }
    }


    public void speedDatingAnswers ()  //check answers for Speed Dating
    {
        if ((a1 [0] [3] == 2) && (a1 [0] [5] == 2) && (a1 [1] [1] == 2) && (a1 [1] [8] == 2) && (a1 [2] [0] == 2) && (a1 [2] [9] == 2) && (a1 [3] [2] == 2) && (a1 [3] [6] == 2) && (a1 [4] [4] == 2) && (a1 [4] [7] == 2) && (a1 [5] [3] == 2) && (a1 [6] [2] == 2) && (a1 [7] [4] == 2) && (a1 [8] [1] == 2) && (a1 [9] [0] == 2))
        {
            int x = 0;
            for (int j = 0 ; j < 10 ; j++) //refer to comments in busyLovebirdsAnswers method
            {
                for (int k = 0 ; k < 10 ; k++)
                {
                    if (a1 [j] [k] == 2)
                        x++;
                }
            }
            if (x == 15)
                JOptionPane.showMessageDialog (null, "You have finished this puzzle successfully!\nNow try another!", "Success", JOptionPane.INFORMATION_MESSAGE);
            else
                JOptionPane.showMessageDialog (null, "You have made a mistake. Please check again.", "Failed", JOptionPane.INFORMATION_MESSAGE);
        }
        else
        {
            JOptionPane.showMessageDialog (null, "You have made a mistake. Please check again.", "Failed", JOptionPane.INFORMATION_MESSAGE);
        }
    }


    public void evilExesAnswers ()  //check answer for Evil Exes
    {
        if ((a2 [0] [1] == 2) && (a2 [0] [7] == 2) && (a2 [1] [4] == 2) && (a2 [1] [5] == 2) && (a2 [2] [3] == 2) && (a2 [2] [6] == 2) && (a2 [3] [2] == 2) && (a2 [3] [9] == 2) && (a2 [4] [0] == 2) && (a2 [4] [8] == 2) && (a2 [5] [4] == 2) && (a2 [6] [3] == 2) && (a2 [7] [1] == 2) && (a2 [8] [0] == 2) && (a2 [9] [2] == 2))
        {
            int x = 0;
            for (int j = 0 ; j < 10 ; j++) //refer to comments in busyLovebirdsAnswers method
            {
                for (int k = 0 ; k < 10 ; k++)
                {
                    if (a2 [j] [k] == 2)
                        x++;
                }
            }
            if (x == 15)
                JOptionPane.showMessageDialog (null, "You have finished this puzzle successfully!\nNow try another!", "Success", JOptionPane.INFORMATION_MESSAGE);
            else
                JOptionPane.showMessageDialog (null, "You have made a mistake. Please check again.", "Failed", JOptionPane.INFORMATION_MESSAGE);
        }
        else
        {
            JOptionPane.showMessageDialog (null, "You have made a mistake. Please check again.", "Failed", JOptionPane.INFORMATION_MESSAGE);
        }
    }


    public void lotsOfLoveAnswers ()  //check answers in Lots of Love
    {
        if ((b [0] [3] == 2) && (b [0] [4] == 2) && (b [0] [9] == 2) && (b [1] [0] == 2) && (b [1] [7] == 2) && (b [1] [10] == 2) && (b [2] [2] == 2) && (b [2] [5] == 2) && (b [2] [8] == 2) && (b [3] [1] == 2) && (b [3] [6] == 2) && (b [3] [11] == 2) && (b [4] [2] == 2) && (b [4] [5] == 2) && (b [5] [3] == 2) && (b [5] [4] == 2) && (b [6] [0] == 2) && (b [6] [7] == 2) && (b [7] [1] == 2) && (b [7] [6] == 2) && (b [8] [3] == 2) && (b [9] [2] == 2) && (b [10] [1] == 2) && (b [11] [0] == 2))
        {
            int x = 0;
            for (int j = 0 ; j < 12 ; j++)
            {
                for (int k = 0 ; k < 12 ; k++)
                {
                    if (b [j] [k] == 2) //check if all of the array elements have a value of 2 (which would mean that the player set an 'O' in that element/button
                        x++;
                }
            }
            if (x == 24) //if all elements have a value of 2 and there are exactly 24, give congratulations message
                JOptionPane.showMessageDialog (null, "You have finished this puzzle successfully!\nNow try another!", "Success", JOptionPane.INFORMATION_MESSAGE);
            else //if there are more than 15, then tell player they made a mistake
                JOptionPane.showMessageDialog (null, "You have made a mistake. Please check again.", "Failed", JOptionPane.INFORMATION_MESSAGE);
        }
        else //mistake message
        {
            JOptionPane.showMessageDialog (null, "You have made a mistake. Please check again.", "Failed", JOptionPane.INFORMATION_MESSAGE);
        }
    }


    public void islandWeddingsAnswers ()  //check answers for Island Weddings
    {
        if ((b1 [0] [3] == 2) && (b1 [0] [4] == 2) && (b1 [0] [9] == 2) && (b1 [1] [0] == 2) && (b1 [1] [6] == 2) && (b1 [1] [8] == 2) && (b1 [2] [1] == 2) && (b1 [2] [5] == 2) && (b1 [2] [10] == 2) && (b1 [3] [2] == 2) && (b1 [3] [7] == 2) && (b1 [3] [11] == 2) && (b1 [4] [0] == 2) && (b1 [4] [6] == 2) && (b1 [5] [3] == 2) && (b1 [5] [4] == 2) && (b1 [6] [1] == 2) && (b1 [6] [5] == 2) && (b1 [7] [2] == 2) && (b1 [7] [7] == 2) && (b1 [8] [3] == 2) && (b1 [9] [1] == 2) && (b1 [10] [0] == 2) && (b1 [11] [2] == 2))
        {
            int x = 0;
            for (int j = 0 ; j < 12 ; j++) //refer to above
            {
                for (int k = 0 ; k < 12 ; k++)
                {
                    if (b1 [j] [k] == 2)
                        x++;
                }
            }
            if (x == 24)
                JOptionPane.showMessageDialog (null, "You have finished this puzzle successfully!\nNow try another!", "Success", JOptionPane.INFORMATION_MESSAGE);
            else
                JOptionPane.showMessageDialog (null, "You have made a mistake. Please check again.", "Failed", JOptionPane.INFORMATION_MESSAGE);
        }
        else
        {
            JOptionPane.showMessageDialog (null, "You have made a mistake. Please check again.", "Failed", JOptionPane.INFORMATION_MESSAGE);
        }
    }


    public void anniversaryCruisesAnswers ()  //check answer for Anniversary Cruises
    {
        if ((b2 [0] [0] == 2) && (b2 [0] [4] == 2) && (b2 [0] [10] == 2) && (b2 [1] [2] == 2) && (b2 [1] [7] == 2) && (b2 [1] [9] == 2) && (b2 [2] [1] == 2) && (b2 [2] [5] == 2) && (b2 [2] [11] == 2) && (b2 [3] [3] == 2) && (b2 [3] [6] == 2) && (b2 [3] [8] == 2) && (b2 [4] [3] == 2) && (b2 [4] [6] == 2) && (b2 [5] [2] == 2) && (b2 [5] [7] == 2) && (b2 [6] [0] == 2) && (b2 [6] [4] == 2) && (b2 [7] [1] == 2) && (b2 [7] [5] == 2) && (b2 [8] [0] == 2) && (b2 [9] [1] == 2) && (b2 [10] [3] == 2) && (b2 [11] [2] == 2))
        {
            int x = 0;
            for (int j = 0 ; j < 12 ; j++) //refer to above
            {
                for (int k = 0 ; k < 12 ; k++)
                {
                    if (b2 [j] [k] == 2)
                        x++;
                }
            }
            if (x == 24)
                JOptionPane.showMessageDialog (null, "You have finished this puzzle successfully!\nNow try another!", "Success", JOptionPane.INFORMATION_MESSAGE);
            else
                JOptionPane.showMessageDialog (null, "You have made a mistake. Please check again.", "Failed", JOptionPane.INFORMATION_MESSAGE);
        }
        else
        {
            JOptionPane.showMessageDialog (null, "You have made a mistake. Please check again.", "Failed", JOptionPane.INFORMATION_MESSAGE);
        }
    }


    protected static ImageIcon createImageIcon (String path)  //method used to retrieve images used in game
    {
        java.net.URL imgURL = logicPuzzle1.class.getResource (path);
        if (imgURL != null)
            return new ImageIcon (imgURL);
        else
        {
            System.err.println ("Couldn't find file: " + path);
            return null;
        }
    }
}
