# 🐧 Penguin Fishing Club v1.2

A Web3-enabled fishing game built with RPG Maker MZ, featuring blockchain integration, wallet connectivity, and interactive minigames.

## 🌟 Features

### 🎣 Enhanced Fishing System
- **Interactive Minigame**: Skill-based timing system instead of simple clicking
- **Multiple Fish Types**: Mackerel, Anchovy, Salmon, Trout, and rare Treasure
- **Difficulty Levels**: Easy, Normal, and Hard with different catch rates
- **Visual Feedback**: Progress bars, moving targets, and score system

### 💰 Web3 Integration
- **Abstract Global Wallet (AGW)**: Connect via Privy SDK
- **Blockchain Coinflip**: Real ETH stakes with smart contract integration
- **Wallet Save System**: Progress saved per wallet address
- **MetaMask Support**: Traditional Web3 wallet connectivity

### 🎮 Game Features
- **Customizable Skins**: Multiple character appearances and clothing options
- **Event System**: Community challenges and tournaments
- **Leaderboard**: Firebase-powered global rankings
- **Audio System**: Background music and sound effects with mute controls

## 🚀 Quick Start

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- MetaMask browser extension (for Web3 features)
- Internet connection (for blockchain features)

### Installation
1. Clone this repository
2. Open `index.html` in your web browser
3. Accept the EULA to start playing
4. Connect your wallet for full Web3 features

### Web3 Setup
1. Install MetaMask browser extension
2. Add Abstract Chain (Chain ID: 2741) to your wallet
3. Get some test ETH for coinflip games
4. Connect your wallet in-game

## 🎯 How to Play

### Basic Fishing
1. Approach water areas in the game
2. Press Enter or click on fishing spots
3. Time your clicks when the fish is in the yellow target zone
4. Better timing = higher score = better rewards

### Coinflip Minigame
1. Find coinflip events in the game (look for "YEAYEAYEA" text)
2. Connect your wallet if not already connected
3. Choose your bet amount (0.0001, 0.01, 0.1 ETH or custom)
4. Select Green (Heads) or Brown (Tails)
5. Wait for blockchain confirmation
6. Win 2x your stake if you guess correctly!

### Skin Customization
1. Click the skin button (👕) in the bottom right
2. Choose from available hats and clothing
3. Mix and match different combinations
4. Changes are saved automatically

## 🔧 Technical Details

### Smart Contracts
- **Coinflip Contract**: `0xcb300ef13a41E27a29674278b4C4D68A506aFf8D`
- **Network**: Abstract Chain (Chain ID: 2741)
- **Type**: Test-only coinflip using on-chain pseudo-randomness

### Technologies Used
- **RPG Maker MZ**: Game engine
- **JavaScript**: Core game logic
- **Ethers.js**: Web3 library for blockchain interaction
- **Firebase**: Real-time database for leaderboards
- **Privy SDK**: Abstract Global Wallet integration

### File Structure
```
├── js/plugins/           # Game plugins
│   ├── WalletConnect.js  # AGW wallet integration
│   ├── WalletSaveSystem.js # Wallet-based save system
│   ├── CoinflipMinigame.js # Blockchain coinflip
│   └── FishingMinigame.js # Enhanced fishing system
├── data/                 # Game data files
├── img/                  # Game assets
├── audio/                # Sound effects and music
├── index.html            # Main entry point
├── game.html             # Game interface
└── coinflip-test.html    # Testing page
```

## 🛠️ Development

### Testing
- Use `coinflip-test.html` to test Web3 functionality
- Check browser console for detailed logs
- Test with small amounts first

### Adding Features
1. Create new plugins in `js/plugins/`
2. Add plugin references to `js/plugins.js`
3. Test thoroughly before deployment

### Debugging
- Enable browser developer tools
- Check console for error messages
- Verify wallet connection status
- Test network connectivity

## 🔒 Security Notes

⚠️ **Important**: The coinflip contract uses on-chain pseudo-randomness and is marked as "TEST ONLY". 

**Not suitable for production use** where real money is at stake.

### Randomness Source
The contract derives randomness from:
- `block.timestamp`
- `block.prevrandao` (PoS difficulty)
- `msg.sender` (player address)
- `address(this).balance` (contract balance)

## 📱 Browser Compatibility

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

## 🐛 Troubleshooting

### Common Issues

1. **Wallet Not Connecting**
   - Ensure MetaMask is installed and unlocked
   - Check if you're on the correct network (Abstract Chain)
   - Try refreshing the page

2. **Coinflip Not Working**
   - Verify you have sufficient ETH for gas fees
   - Check contract balance (needs 2x your bet amount)
   - Ensure you're on Abstract Chain

3. **Fishing Minigame Issues**
   - Make sure the plugin is enabled
   - Check browser console for errors
   - Try refreshing the game

4. **Save Data Not Loading**
   - Ensure wallet is connected
   - Check localStorage for saved data
   - Try disconnecting and reconnecting wallet

## 📄 License

This project is licensed under the MIT License. See the LICENSE file for details.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📞 Support

For technical support or questions:
1. Check the browser console for error messages
2. Verify all prerequisites are met
3. Test with the provided test page
4. Create an issue on GitHub

## 🎉 Acknowledgments

- RPG Maker MZ community
- Abstract Global Wallet team
- Privy SDK developers
- Firebase team
- All beta testers and contributors

---

**Enjoy fishing in the Penguin Fishing Club! 🐧🎣**
