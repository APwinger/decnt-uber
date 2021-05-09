# decnt-uber
I have been imagining some kind of bounty platform to allow people who want a ride somewhere to connect with and create trustless contracts with drivers. 


Riders post a "bounty" to the blockchain. This bounty is how much the rider is willing to pay for a ride (held in escrow when bounty posted). It contains information like their address, destination and time they need to arrive by.

Frontends parse the posted bounties for drivers in the area. Once a driver finds a bounty they want, they accept it (maybe this somehow decodes something to get a more precise area) and head to the pickup spot.

Once they pick the person up, they scan QR code at pickup. This ensures both parties are being honest and any disputes can be solved face to face. There could be another scan again at dropoff. At this point the bounty is transfered automatically by the smart contract. The QR codes successfully being scanned could upload GPS data to the blockchain for saftey if its worth the fees.

As an additional saftey step, drivers should be required to lock up a certain amount of money as collateral. As in, in order to interact with the smart contract as driver, a minimum balance from that account must be controlled by the smart contract.

There could be a sort of reputation system that could penalize them if the person who paid their bounty is upset. For example if the pickup or dropoff QR code is not scanned in time after a driver accepts a contract.

DAO governance could be used to hold "hearings" for drivers who are reported to have misbehaved to use data on chain, as well as testimony from driver and rider to determine if any of the drivers collateral should be liquidated.

Riders could potentially reject or filter out drivers without much money locked because they could be less trustworthy.

Additionally, there could be a way to let third parties offer certifications for verified drivers that are viewable on chain. Ie, driver X pays business Y to give him a signed certificate. Business Y checks his background info etc. Y can then publish a list of trusted accounts. Riders who are wary of drivers (particularly women traveling alone) could filter and only accept drivers who have this extra layer of verification.

This all depends on low fees, but I think its an interesting idea. Especially because it scales so well. If there are a low number of drivers, you can just set the timeframe for weeks in advance. If there are many drivers, you can ask for a lower price and give less notice.



I'm not sure the GPS needs to verify anything. I was thinking that the frontend could generate different QR codes for each leg of the journey. For example, at pickup, driver scans riders QR code and lets them in and drives the rider to their desired spot. A new code is generated from the rider and the driver scans it. Each QR code scan should probably be uploaded to the blockchain.



After the first pickup scan, the rider cannot withdraw the bounty. This means they have effectively spent the money. The final scan completes the transaction and allows the payment to go to the driver. This way, the rider retains the power to withhold the funds if they are not delivered to their destination but cannot get the money back. This incentivizes the rider to act positively and confirm the transaction for the driver.



Optionally, GPS information could be encoded somehow and uploaded to the blockchain for safety. Either at set intervals throughout the journey or when QR code scans are completed. I'm not a huge fan of the GPS data on the blockchain for much more than auditing but I haven't really looked into it. For example, if someone goes missing, the blockchain could tell us what scans were completed and where.



Different frontends could provide GPS tracking of drivers the typical uber way where you can see them on their way to you. I think constantly uploading essentially junk data to the blockchain would get expensive. The frontends should implement as much of this off the blockchain as possible. The blockchain should just be used to hold the funds in escrow and transfer them as conditions are met.



Selling bounties to uber or taxi stations is fucking BRILLIANT. I'm quite curious as to what the rates would settle to. If you ignore the transaction fees (which are a lower level problem that could be solved with using an l2 eth solution, a different chain, or if eth improves) would they be lower than uber or a taxi? There isn't a lot of overhead besides gas fees and potentially a fee to a DAO fund.
