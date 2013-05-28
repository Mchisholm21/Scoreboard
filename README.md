Scoreboard
==========

Basic Scoreboard
 import java.awt.*;
import javax.swing.*;
import java.awt.event.*;

public class StartScreen extends JFrame
{

 JButton button1;
 
 public StartScreen()
 {
        setLayout(new GridLayout(1, 1));
       
        button1 = new JButton("Start Game");
        add(button1);
        
        PressStartGameButton e = new PressStartGameButton();
        button1.addActionListener(e);
    }
    
      public class PressStartGameButton implements ActionListener
{
   public void actionPerformed(ActionEvent e)
   {
   ScoreBoard grid = new ScoreBoard();
        grid.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        grid.setVisible(true);
        grid.pack();
        grid.setSize(300,500);
    
        setVisible(false);
           
   }
}
    
    
}



public class ScoreBoard extends JFrame
{
 JLabel label1, label2, label3, label4, label5, label6, label7, label8;
 JButton button1, button2;
 private int score1, score2, quarter, time, down, lastPlay;
 
 public ScoreBoard()
 {
        setLayout(new GridLayout(10, 1));
        
        label1 = new JLabel("Home Team" );
        add(label1);
        
        label2 = new JLabel("Score");
        add(label2);
        
        label3 = new JLabel("Away Team");
        add(label3);
        
        label4 = new JLabel("Score");
        add(label4);
        
        label5 = new JLabel("Quarter: ");
        add(label5);
     
        label6 = new JLabel("Time:  ");
        add(label6);
        
        label7 = new JLabel("Down:   ");
        add(label7);
        
        label8 = new JLabel("Last Play:    ");
        add(label8);
        
         button2 = new JButton("NEW GAME");
         add(button2);
         
        PressNewGameButton x = new PressNewGameButton();
        button2.addActionListener(x);
         
        button1 = new JButton("EXIT");
        add(button1);
       
  
        PressEndGameButton e = new PressEndGameButton();
        button1.addActionListener(e);
    }
   
  public class PressEndGameButton implements ActionListener
{
   public void actionPerformed(ActionEvent e)
   {
   
       System.exit(0);

   }
}
     public class PressNewGameButton implements ActionListener
{
   public void actionPerformed(ActionEvent x)
   {
     StartScreen start = new StartScreen();
        start.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        start.setVisible(true);
        start.pack();
        start.setTitle("FOOTBALL");
        start.setSize(300,300);
        
       setVisible(false);
 
    
   
   }
   
}
  

}
    
 

public class ScoreBoardCreator
{
    
    public static void main(String args[])
    {
        ScoreBoard grid = new ScoreBoard();
        grid.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        grid.setVisible(true);
        grid.pack();
        grid.setSize(300,500);
    }
}



public class StartScreenCreator
{
    
public static void main(String args[])
    {
        StartScreen start = new StartScreen();
        start.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        start.setVisible(true);
        start.pack();
        start.setTitle("FOOTBALL");
        start.setSize(300,300);
    }
}






