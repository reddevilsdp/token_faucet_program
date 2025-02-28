# 🏛️ Blind Auction

A **first-price sealed-bid auction** (or **blind auction**) implemented in **Leo**.

## 📌 Summary

A **blind auction** is a type of auction where participants submit bids without knowing the bids of others. The highest bid wins the auction.

### **Roles in the Auction**
- **Bidder**: A participant placing a bid.
- **Auctioneer**: The entity managing the auction process.

### **Auction Assumptions**
- The **auctioneer is honest** and resolves all bids in the order received, without tampering.
- There is **no limit** on the number of bids.
- The auctioneer knows all bidders, but bidders do **not** necessarily know each other.
- Bidders cannot learn the value of other bids.

## 📜 Auction Flow

1️⃣ **Bidding Stage**: Bidders submit their bids by invoking the `place_bid` function.
2️⃣ **Resolution Stage**: The auctioneer resolves bids in order using the `resolve` function. The highest bid wins.
3️⃣ **Finishing Stage**: The auctioneer finalizes the auction with the `finish` function, allowing the winner to claim the item.

## 🔍 Key Language Features
- **`record` declarations**
- **`assert_eq` for validation**
- **Record ownership enforcement**

## 🚀 Running the Program

Leo provides a **command-line interface** for compiling and running programs.

### **🔧 Configuring Accounts**
The `.env` file contains a **private key**, used to sign transactions and verify ownership of records.
- When running the program as different participants, update the `PRIVATE_KEY` in `.env` accordingly.
- See `./run.sh` for an example of running the program as different roles.

### **🛠️ Generating Accounts**
You can generate a new account using the [Aleo SDK](https://github.com/ProvableHQ/leo/tree/mainnet) or via [provable.tools](https://provable.tools).

### **📝 Running the Auction via CLI**
```bash
leo run <function_name> <input_1> <input_2> ...
```
See `./run.sh` for an example of running the program.

---

### 📢 Need Help?
Check out the official **Leo documentation** or reach out to the community for support!

