# secure-evoting
Proof of concept for Codefundo++ 2019 (Secure e-voting using Blockchain)
# The Problem
Currently, voters have to be present at the voting booth physically to be able to exercise their right to vote. Using a secure, online voting system we can eliminate the need for presenting oneself at the location, and instead do it from the comfort of one's home. 
# How Blockchain is Involved
- Improving logistics of voting  
  *Since all the election data is linked and timestamped, everyone can count the votes for themselves and verify it with others on the blockchain almost instantaneously eliminating the lengthy process of vote counting and recounting. 
- Preventing corruption and misrepresentation of voters  
  *Traditional voting systems are prone to being tampered with and can easily be manipulated to misrepresent the votes. By linking the votes to a blockchain everyone will have access to them. Everyone will have exactly one vote that is immutable and tamper proof.
- Real-time data collection and sharing  
  *Does away with the need to have a central agency to validate the votes.
# The Block and Chain
The block chain will be viewed in two levels  i.e two types of nodes: constituency and national  
  
We use a system of public-private key pairs to encrypt-decrypt the data for the votes. The key pairs are generated at the constituency level. Each constituency will have a different public key which is used to encrypt the votes given by voters registered to that constituency.  
Since the constituencies have different keys, different blocks will have their data encrypted differently depending on their constituency.  
Consequently, it would be almost impossible for anyone trying to illegally gain access to all the votes to do so without conquering the entire network, due to this encryption mechanism.  
The below diagram will put the above description succinctly.  
![alt text](structure.png?raw=true "Network Structure")
## The Voting Process
During the voting period, the voter will be asked to login to his/her account using the issued Voter ID and an MFA system. After a successful login, the voter will be directed to the ballot page where he/she will be asked to enter the candidate choice. Note here, that a voter will be shown candidates standing for elections only in the constituency he/she is registered to vote in, thus making sure that the vote is cast in the same constituency.  
After this, the vote will be encrypted using the public key.  

After the voting deadline the constituency nodes publish their private keys so data can be decrypted by the blockchain network. The votes can be counted once the data has propagated the network.




