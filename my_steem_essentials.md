* #### Steem reputation score is calculated in the following way:
  ![](https://github.com/abhi3700/My_Learning-Steem/blob/master/Images/steem_reputation_score_calc.png)
  JAVA code:
  ```
  public  int calculateReputationScore(String rawScore){
        return (int)Math.floor(((Math.log10(Long.parseLong(rawScore)) - 9) * 9) + 25);
  }
  ```
  
