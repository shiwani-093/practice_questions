# practice_questions
//minimum bits flips to make a or b equal to c

class Solution {
public:
    int minFlips(int a, int b, int c) {
      int flips=0;
      while(a!=0 || b!=0 || c!=0)
      {
          if((c&1)==1)
          {
              if((a&1)==0 && (b&1)==0)
              {
                  flips++;
              }
             
          }
         // if(c&1==0)
         else
          {
              if((a&1)==1)
              flips++;
              if((b&1)==1)
              flips++;
            
          }
            a=a>>1;
            b=b>>1;
            c=c>>1;
      } 
      return flips; 
    }
};
