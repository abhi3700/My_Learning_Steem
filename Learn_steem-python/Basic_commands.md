## Introduction
This is all about practising the basic commands of **"Steem-Python"**. 


## Basic commands
```python
>>> from steem import Steem
>>> s = Steem()
```
#### All keys
Using all keys, we can query.
```python
>>> s.get_account('abhi3700').keys()
```
![](https://github.com/abhi3700/My_Learning-Steem/blob/master/Learn_steem-python/Images/all_keys.png)

#### Id
This represents the 'user id' of the steem account holder. This is assigned whenever the user joins for 1st time and it remains permanent for the 'username'
```python
>>> s.get_account('abhi3700')['id']
143518
```
#### Name
```python
>>> s.get_account('abhi3700')['name']
'abhi3700'
```
#### Owner, Active, Posting, Memo Keys
Here, all the keys required to access account's different features.
![](https://github.com/abhi3700/My_Learning-Steem/blob/master/Learn_steem-python/Images/posting_active_owner_memo_keys.png)

##### Owner
```python
>>> s.get_account('abhi3700')['owner']
{'weight_threshold': 1, 'account_auths': [], 'key_auths': [['STM6ihsdp1csAV4PP3L9iR32BDTs2YMMuKKFucf4cPFGsMo4JNBdA', 1]]}
```

##### Active 
```python
>>> s.get_account('abhi3700')['active']
{'weight_threshold': 1, 'account_auths': [], 'key_auths': [['STM7pC2cAQKJyvx4bTVymHmsEsv7MdpLHavfGwsH9xdmvzwUbUfJ9', 1]]}
```

##### Posting
```python
>>> s.get_account('abhi3700')['posting']
{'weight_threshold': 1, 'account_auths': [['utopian.app', 1]], 'key_auths': [['STM7qcX28MAA5KD8bDiJ9NpQjmKx6gPmr51d8LrMV8SFxKTBi8WzS', 1]]}
```
##### Memo
```python
>>> s.get_account('abhi3700')['memo_key']
'STM67gGcjV8Fg3xMtDvWuzYZoxWs6amHethQPihUuCcnv3EMTeb3J'
```
