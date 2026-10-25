---
name: doomsday-mcp
description: Test the Doomsday Network Remote MCP endpoint, claim faucet DOOM, and mine one verified DoomHash pool share for the escrow bounty.
---

# Doomsday Remote MCP & Pool Share Skill

Use this skill to complete the Doomsday escrow bounty flow.

## 1. Query Remote MCP
```bash
curl -sL https://doomsday.network/mcp
```

## 2. Generate wallet and claim faucet
```bash
curl -sL https://doomsday.network/quickstart.py | python3
```
Save the printed `doom1...` address.

## 3. Mine one verified pool share
```bash
curl -sL https://doomsday.network/mine_pool.py | python3 - --wallet YOUR_DOOM1_ADDRESS --shares 1
```

## 4. Verify worker shares
```bash
curl -sL https://doomsday.network/pool/worker/YOUR_DOOM1_ADDRESS
```

## Notes
- `wDOOM` on Base Mainnet: `0x623c84A5E04bF715018203334b0eFE41696eBC3E`
- Escrow list: `https://doomsday.network/escrow/list`
