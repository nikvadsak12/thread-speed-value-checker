package javasa;



	class hiii implements Runnable{	
	     public void run() {
	    	 for(int i=1;i<=5;i++) {
	    		 System.out.println("hii");
	    		 try {
					Thread.sleep(1000);
				} catch (InterruptedException e) {
					// TODO Auto-generated catch block
					e.printStackTrace();
				}
	    	 }
	     }
	     

	}
	class hello implements Runnable{	
	     public void run() {
	    	 for(int i=1;i<=5;i++) {
	    		 System.out.println("hello");
	    		 try {
					Thread.sleep(1000);
				} catch (InterruptedException e) {
					e.printStackTrace();
				}
	    	 }
	     }
	     
	}
class Person{
		
	 public static void main(String[] args)  {
		Runnable ne=new hiii();
		Runnable me=new hello();
		Thread t1=new Thread(ne);
	    Thread t2=new Thread(me);
	    t1.start();
	    try {
			Thread.sleep(100);
		} catch (InterruptedException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
	    t2.start();
	    
	}
	}

