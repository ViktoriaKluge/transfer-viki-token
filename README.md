# transfer-viki-token

Whitelist check: Before transferring VikiWhitelistToken, the page attempts to call addToWhitelist(recipient) on the contract. If the connected account is the contract owner, this ensures the recipient is whitelisted (or keeps it whitelisted if already); if the account is not the owner, this call reverts and is caught, after which the transfer is attempted regardless, succeeding only if the recipient was already whitelisted.
