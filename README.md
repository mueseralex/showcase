# Telegram Framework

## About

The Framework is still being uploaded. This is Telegram Framework centered around a bot that interacts with users via direct messages. The goal is to provide creators with a framework that handles payments, users, referrals, and private website sessions.

## Branch Info

### Repository Structure

- [📄 README.md](README.md) - Main documentation and framework overview
- [📦 Framework/](Framework/) - Core package for creators to implement the bot framework
- [📝 Installation.md](Installation.md) - Step-by-step installation guide
- [🎬 Sample.md](Sample.md) - Example implementations and demos

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

## Documentation

*Documentation coming soon*
