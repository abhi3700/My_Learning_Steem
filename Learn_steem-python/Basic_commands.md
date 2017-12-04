## Introduction
This is all about practising the basic commands of **"Steem-Python"**. 


## Basic commands
Import the Steem function from steem library. After importing, we can use the function to access further commands (variables) inside that function.
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
#### Public Profile Settings
This shows the meta-data about the user.
![](https://github.com/abhi3700/My_Learning-Steem/blob/master/Learn_steem-python/Images/public_profile_settings.png)
```python
>>> s.get_account('abhi3700')['json_metadata']
'{"profile":{"name":"Abhijit Roy","about":"A Software Developer, Traveller, Crypto Trader, Blockchain enthusiast","location":"Chandigarh, India","profile_image":"https://firebasestorage.googleapis.com/v0/b/bitinfocoinfree.appspot.com/o/14068548_1125160424216001_2627046384272844500_o.jpg?alt=media&token=8bb1b1f9-36f5-4b9a-8220-4134f01f8542","website":"https://play.google.com/store/apps/details?id=in.topux.bitinfocoin","cover_image":"https://www.ethereum.org/images/assets/1900/Ethereum-homestead-background-4.jpg"}}'
```

#### Proxy
It is null in this case as no proxy server used.
```
>>> s.get_account('abhi3700')['proxy']
''
```
#### Last owner update
It comes from the UNIX command i.e. January 1st 1970. Also birthdays are written in timestamps (time from this date till date).
```
>>> s.get_account('abhi3700')['last_owner_update']
'1970-01-01T00:00:00'
```

#### Last account update
It mainly is when the account settings (public profile) was last updated.
```python
>>> s.get_account('abhi3700')['last_account_update']
'2017-11-26T17:57:18'
```

#### Account creation time
The date, time when the account was created.
```python
>>> s.get_account('abhi3700')['created']
'2017-04-02T08:00:57'
```

#### Recovery account
If your account gets hacked, it can be recovered before any data is manipulated.
```python
>>> s.get_account('abhi3700')['recovery_account']
'steem'
>>> s.get_account('abhi3700')['last_account_recovery']
'1970-01-01T00:00:00'
```






