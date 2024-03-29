# MetaMorphic Contract
A metamorphic contract can potentially cause confusion or security risks. Since the contract's bytecode changes upon each deployment, it can be challenging for users to verify its functionality or security. Malicious actors could abuse this property to deploy contracts with malicious intent or to evade detection by security tools.
## Create2 Function:
The create2 function is an internal function of the Metamorph contract. It takes four parameters: value (ether value to send with the creation), salt (a random number to ensure deterministic deployment), bytecode (the bytecode of the contract to deploy), and created (the address of the newly created contract). This function deploys a contract using the create2 opcode, which allows for deterministic deployment based on a salt value.
- By using create2 with a salt value, the contracts ContractX and ContractY can be deployed with different bytecode but at the same address if the salt value remains the same. This enables the contract to change its bytecode upon each deployment while maintaining the same address, making it "metamorphic."

## Potential Risks:
- Metamorphic contracts can introduce uncertainty and trust issues. Users interacting with such contracts may find it difficult to audit or predict their behavior accurately. Additionally, since the bytecode changes with each deployment, it might bypass certain security checks or analyses, posing risks to the Ethereum network and its users.
