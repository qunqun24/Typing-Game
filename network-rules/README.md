# Bilibili live chat rule

`bilibili-chat.srs` is a sing-box binary rule set matching only `chat.bilibili.com` and its subdomains. The JSON file is its reviewable source. These files contain no account or proxy credentials.

Raw download URL:

https://raw.githubusercontent.com/qunqun24/Typing-Game/bilibili-chat-rules/network-rules/bilibili-chat.srs

In the proxy client, assign this rule set to a proxy outbound and place it before broader rules that route these domains or their IPs directly. Keep the other required routing rule sets. Enabling custom rule sets in ZodAccess replaces part of its built-in routing; adding this file alone is not a complete replacement configuration.

After applying, reconnect and reopen the live room. Confirm that the chat connection uses the proxy outbound. This matching rule does not itself specify a proxy node.

Compiled with official sing-box 1.12.0 and verified by decompiling the result. SHA256:

`5f1da8d20fc57dc1a628f80c29d3ed16c7d2572cb037d0c097d67b78aba9c8b4`
