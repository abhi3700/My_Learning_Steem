* #### Steem reputation score is calculated in the following way:
  ![](https://github.com/abhi3700/My_Learning-Steem/blob/master/Images/steem_reputation_score_calc.png)
  JAVA code:
  ```
  public  int calculateReputationScore(String rawScore){
        return (int)Math.floor(((Math.log10(Long.parseLong(rawScore)) - 9) * 9) + 25);
  }
  ```
  
* #### upvote worth calculation depends on - _`SP`_, _`Voting Power`_, _`Voting Weight`_.
  ```js
  // These values are blockchain parameters and can be seen on https://steemd.com
  const steem_per_vest = 488.307 / 1e6; // steem_per_mvests / 1E6
  const reward_balance = 699080;
  const recent_claims = 376642879570736617;
  const reward_per_rshare = reward_balance / recent_claims;
  const steem_price_sbd = 5.219; // feed_price.base / feed_price.quote

  function calculateVoteValue(
    steem_power = 10000,
    voting_power = 100,
    voting_weight = 100
  ) {
    const vests = steem_power / steem_per_vest;
    let multiplicator = voting_power * voting_weight;
    // some normalization of the vote multiplicator
    multiplicator = parseInt((multiplicator + 49) / 50);
    const reward =
      parseInt(vests * multiplicator * 100) * reward_per_rshare * steem_price_sbd;
    return reward;
  }
  ```
  
  [SOURCE](https://cmichel.io/how-does-steem-work/)
