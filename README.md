# MyFirstRepo

package src;

public class StringMatching {
	
	public static void main(String[] args) {
		
		String pat="aab";
		String text="aaaaaaaaaaaaaab";
		StringMatching s = new StringMatching();
		s.matchPattern(pat,text);
		
	}
	
	public void matchPattern(String pat, String text) {
		
		int t=text.length();
		int p=pat.length();
		boolean found=false;
		
		for(int i=0;i<= t-p ; i++) {
			
			if(text.charAt(i) == pat.charAt(0)){
				if(text.substring(i,p+i).equalsIgnoreCase(pat)) {
					found=true;
					System.out.println("found");
					break;
				}
				
			}
			
		}
		if(!found)
			System.out.println("not found");
			
		
	}

}
