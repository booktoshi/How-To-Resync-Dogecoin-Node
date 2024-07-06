# Resync Your Dogecoin Node: Windows & Linux

Yo, what's good? Ready to get your Dogecoin node back in sync after updating your `dogecoin\.conf` file? Follow these steps whether you're rockin' Windows or Linux\.

## Windows Machine

1. **Stop the Dogecoin Node**:
   First things first, shut it down:
   ```sh
   dogecoin\-cli stop
   ```

2. **Locate the Data Directory**:
   Find your Dogecoin crib here:
   ```sh
   %APPDATA%\\Dogecoin\\
   ```
   Just hit `Win + R`, type `%APPDATA%\\Dogecoin\\`, and press Enter\.

3. **Delete the Blockchain Data**:
   Clear out the old blocks and chainstate, but don't touch that `wallet\.dat` if it's got your stacks\.
   ```sh
   del /S /Q %APPDATA%\\Dogecoin\\blocks
   del /S /Q %APPDATA%\\Dogecoin\\chainstate
   ```

4. **Start the Dogecoin Node**:
   Bring it back to life\.
   ```sh
   dogecoind \-daemon
   ```

5. **Monitor the Sync**:
   Check the status like a boss:
   ```sh
   dogecoin\-cli getblockchaininfo
   ```

## Linux Machine

1. **Stop the Dogecoin Node**:
   Shut it down, fam:
   ```sh
   dogecoin\-cli stop
   ```

2. **Locate the Data Directory**:
   Find your Dogecoin stash here:
   ```sh
   ~/.dogecoin/
   ```

3. **Delete the Blockchain Data**:
   Clean out the old stuff, but hands off that `wallet\.dat`:
   ```sh
   cd ~/.dogecoin/
   rm \-rf blocks chainstate
   ```

4. **Start the Dogecoin Node**:
   Fire it back up\.
   ```sh
   dogecoind \-daemon
   ```

5. **Monitor the Sync**:
   Keep an eye on it:
   ```sh
   dogecoin\-cli getblockchaininfo
   ```

And that's it\! You're back in the game with a fresh sync\.

---

Feel free to use this guide in your GitHub `readme\.md` file and keep it cool while you handle your Dogecoin biz\.

---

