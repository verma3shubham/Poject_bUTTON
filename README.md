# Poject_bUTTON
import java.awt.Button;
import java.awt.FlowLayout;
import java.awt.Frame;
import java.awt.Label;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
class MyFrame extends Frame implements ActionListener
{
    int count;
    Button b;
    Label l;
    public MyFrame()
    {
        super("Button Demo");
        setLayout(new FlowLayout());
        b=new Button("COUNTING BUTTON");
        l=new Label("  "+count);
        b.addActionListener(this);

        add(l);
        add(b);
    }
    public void actionPerformed(ActionEvent e)
    {
        count++;
        l.setText("  "+count);
    }
}
class FirstButton
{
    public static void main(String[] args)
    {
        MyFrame f=new MyFrame();
        f.setSize(300,300);
        f.setVisible(true);
    }
}
