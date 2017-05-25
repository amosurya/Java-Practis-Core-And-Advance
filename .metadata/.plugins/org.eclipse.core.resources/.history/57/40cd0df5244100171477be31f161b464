import java.io.FileOutputStream;
import java.io.ObjectOutputStream;
import java.io.Serializable;

import com.externalization.Box;

/*abstract class Abstracttest{
	
	private int i;
	public static void name() {
		System.out.println("-------");
	}
}
*/

class TestSerializable {
	
	 int i = 10;
	 String str = "Amossssl";
	 TestSerializable(){
		}
	TestSerializable(int i, String st){
		this.i = i;
		str = st; 
	}
}

class Studentinfo  implements Serializable {
	 /**
	 * 
	 */
	
	private static final long serialVersionUID = -1529378690148384997L;
	
	TestSerializable serializable = new TestSerializable(10 ,"aaa");
	String name;
	 int rid;
	 
	// TestSerializable testSerializable; // if u serialize Studentinfo class then u required to implement serializable interface of   
	 static String contact;             // TestSerializable class otherwise they will be throw java.io.NotSerializableException Exception 
	 Studentinfo(String n, int r, String c)
	 {
		// super(10,"aaa");
	  this.name = n;
	  this.rid = r;
	  this.contact = c;
	  //testSerializable = new TestSerializable(10,"AmolSurya");
	 }
	}
public class Test {

	public static void main(String[] args) {
		try{
		  
		  Studentinfo si = new Studentinfo("Abhi", 104, "110044");
		  FileOutputStream fos = new FileOutputStream("D:/student.txt");
		  ObjectOutputStream oos = new ObjectOutputStream(fos);
		  oos.writeObject(si);
		  oos.close();
		  fos.close();
		  System.out.println("-----------");
		  }
		  catch (Exception e)
		  { e. printStackTrace(); }

	}

}
