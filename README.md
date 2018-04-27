# Networking_Client

import java.io.DataOutputStream;
import java.net.Socket;

public class Networking {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		try {
			Socket s = new Socket("192.168.100.71", 10000);
			DataOutputStream dout = new DataOutputStream(s.getOutputStream());
			dout.writeUTF("Happy Friday");
			dout.flush();
			dout.close();
			s.close();
		} catch (Exception e) {
			System.out.println(e);
		}

	}
}
