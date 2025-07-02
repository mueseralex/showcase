# Telegram Framework

## About

This is Telegram Framework centered around a bot that interacts with users via direct messages. The goal is to provide creators with a framework that handles payments, users, referrals, and private website sessions.

## Branch Info

*Documentation coming soon*

## Non-Paid Users Bot Interactions

```mermaid
graph LR
    %% Core flow with exact spacing
    User[user] -->|all users non-paid<br/>bot interactions| InitBot[initialize bot]
    InitBot --> Welcome[welcome<br/>message]
    Welcome --> Buttons[buttons]
    
    %% Payment and wallet check flow
    Buttons --> PayNow[pay now]
    PayNow --> WalletCheck[checks if a wallet<br/>is link]
    WalletCheck -->|yes| PayDash[payment<br/>dashboard]
    PayDash --> WebhookListen[webhook listens<br/>for payment]
    WebhookListen --> PayStatus[full payment]
    PayStatus --> PaidStatus[user is granted<br/>paid status]
    WebhookListen --> PartialStatus[partial or none]
    PartialStatus --> PayDash
    
    %% Wallet management
    WalletCheck -->|no| LinkWallet[link wallet]
    Buttons --> LinkWallet
    LinkWallet --> Add[add]
    LinkWallet --> Remove[remove]
    
    %% Referral system
    Buttons --> Referrals[referrals]
    Referrals --> ChangeWallet[change payout<br/>wallet]
    Referrals --> CreatorDash[creator<br/>dashboard]
    Referrals --> CreateRef[create referral<br/>link]
    
    %% Styling
    classDef default fill:#fff,stroke:#000,stroke-width:2px,color:#000
    classDef start fill:#fff,stroke:#000,stroke-width:2px,color:#000
    classDef success fill:#fff,stroke:#000,stroke-width:2px,color:#000
    
    class User,InitBot,Welcome,Buttons,PayNow,WalletCheck,PayDash,WebhookListen,PayStatus,PaidStatus,PartialStatus,LinkWallet,Add,Remove,Referrals,ChangeWallet,CreatorDash,CreateRef default
```

## Paid Users Bot Interactions

```mermaid
graph LR
    %% Core flow with exact spacing
    User[user] -->|paid user bot<br/>interactions| InitBot[initialize bot]
    InitBot --> Welcome[welcome<br/>message]
    Welcome --> Buttons[buttons]
    
    %% Website access flow
    Buttons --> WebAccess[website access]
    WebAccess --> CustomLink[custom link with<br/>unique token is<br/>generated]
    CustomLink --> Login[login to website]
    
    %% Referral system
    Buttons --> Referrals[referrals]
    Referrals --> ChangeWallet[change payout<br/>wallet]
    Referrals --> CreatorDash[creator<br/>dashboard]
    Referrals --> CreateRef[create referral<br/>link]
    
    %% Styling
    classDef default fill:#fff,stroke:#000,stroke-width:2px,color:#000
    classDef start fill:#fff,stroke:#000,stroke-width:2px,color:#000
    
    class User,InitBot,Welcome,Buttons,WebAccess,CustomLink,Login,Referrals,ChangeWallet,CreatorDash,CreateRef default
```

## Framework Implementation Examples

Below are video demonstrations of the framework in action. These are example implementations and are not included in the base framework.

### Quick Links
- [View Referral System Demo](#referral-program)
- [View Payment System Demo](#payment-processing)

## Referral Program

The referral system provides creators with powerful tools to manage and grow their community:

- **Custom Creator Links**: Unique referral links for tracking and attribution
- **Creator Dashboard**: Real-time analytics and performance metrics
- **Automated Payouts**: Seamless commission distribution system

<details>
<summary>View Referral System Demo</summary>

![Referral System Demo](https://github.com/user-attachments/assets/7bab3bb2-9af2-4bee-84ee-740576e2e01a)

</details>

## Payment Processing

Secure and efficient payment processing system featuring:

- **Solana Crypto Payments**: Fast and low-fee transactions
- **Secure Wallet Linking**: No signing required, maximum security
- **Automatic Payment Detection**: Real-time transaction monitoring
- **Comprehensive User Logging**: Complete payment history tracking

<details>
<summary>View Payment System Demo</summary>

![Payment System Demo](https://github.com/user-attachments/assets/f27e39b2-9649-412e-9a7d-f82eed312506)

</details>

## Documentation Quick Links

- [Full Documentation](#documentation)
- [Non-Paid User Flow](#non-paid-users-bot-interactions)
- [Paid User Flow](#paid-users-bot-interactions)

## Documentation

*Documentation coming soon*
