//viacheslav borodin 
// 15464068 


import java.awt.Graphics;
import javax.swing.JFrame;
import java.awt.BorderLayout;
import javax.swing.JPanel;
import java.awt.Image;
import javax.swing.ImageIcon;
import java.awt.Dimension;
import javax.swing.JLabel;


import static javax.swing.JFrame.EXIT_ON_CLOSE;

	public class TheSimpsons {
		
	public static void main(String[] args){
		
		ImageIcon image = new ImageIcon("C:/Users/Slava Borodin/Documents/COMP20050/Assignment1/monopoly.jpg");
		JLabel imageLabel = new JLabel(image);
	    // new frame created called frame
		JFrame frame = new JFrame();
		
		// size of frame width by height 
	    frame.setSize(1366, 768);
	    // title
		frame.setTitle("Monopoly");
		//shows the frame
		frame.setVisible(true);
		frame.add(imageLabel);
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		
		frame.add(imageLabel,BorderLayout.WEST);
		
		// gets the rectangle boxes from rect class to display in frame 
	
		
		
		
		//frame.getContentPane().add(panel);
	
	}
	
	}
	class ImagePanel extends JPanel{
		private Image img;
		
		public ImagePanel(String img){
			
			this(new ImageIcon(img).getImage());
			
			
			
		}
		public ImagePanel(Image img){
			this.img = img;
			Dimension size = new Dimension(img.getWidth(null), img.getHeight(null));
			setPreferredSize(size);
			setMinimumSize(size);
			setMaximumSize(size);
			setSize(size);
			setLayout(null);
			
		}
		
		public void paint(Graphics g) {
			
			g.drawImage(img, 0, 0, 	null);
				
			}
	
	}
	
