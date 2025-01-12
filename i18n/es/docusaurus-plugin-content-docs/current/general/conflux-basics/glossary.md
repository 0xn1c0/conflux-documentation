---
sidebar_position: 5
title: Glosario
displayed_sidebar: generalSidebar
---

## Introducción

Bienvenido a la sección Glosario de la documentación de Conflux. Esta sección está diseñada para proporcionarle definiciones claras y concisas de términos y conceptos clave utilizados en Conflux y en la industria de blockchain.

Los términos están organizados en orden alfabético para facilitar la navegación. Cada término incluye una definición directa y, en su caso, enlaces a explicaciones más detalladas dentro de nuestra documentación o recursos externos.

## Definiciones

### **Ataque del 51 %**
Un ataque del 51 % se refiere a un ataque potencial en una red blockchain, donde una única entidad u organización es capaz de controlar la mayoría de la tasa de hash de la minería de la red. Este control podría permitirles interrumpir la red modificando el orden de las transacciones, evitando que las nuevas transacciones obtengan confirmaciones o incluso permitan el doble gasto. Se llama un "ataque del 51%" porque normalmente requiere controlar al menos un 51% de la tasa de hash de la red para tener éxito.

### **Cuenta**
El estado global de Conflux se describe en un modelo de cuenta, con el componente de almacenamiento básico llamado cuenta. Cada actor, que es una persona o una entidad capaz de interactuar con el mundo de Conflux, tiene su información necesaria almacenada en una cuenta α como un par clave/valor de [la dirección](#address) y estado correspondiente. Consulte [General/Cuentas](./accounts.md) para obtener información detallada.

### **Dirección**
Una dirección en Conflux es el identificador de una [cuenta](#account). Es una cadena única de caracteres que representa la cuenta en la cadena de bloques. El formato de la dirección difieren en los diferentes [espacios de Conflux](./spaces.md). Hay diferentes formatos para direcciones de eSpace y direcciones del Core Space.

Por ejemplo:

``` 
// espace address
0x1e97870f263700f46aa00d967821199b9bc5a120
// Core Space Mainnet address
cfx:aatktb2te25ub7dmyag3p8bbdgr31vrbeackztm2rj
// Core Space Testnet address
cfxtest:aatktb2te25ub7dmyag3p8bbdgr31vrbeajcg9pwkc
```

Consulte [general-address](./accounts.md#address), [core-address](../../core/core-space-basics/addresses.md), [espace-address](../../espace/build/accounts.md#mapped-addresses-in-cross-space-operations) para más información.

### **Bloque**
En la tecnología blockchain, un bloque es un conjunto de transacciones. Es como una página de un libro de registro. Cada bloque está vinculado a un bloque anterior y a otro posterios de él, creando una cadena de bloques, de ahí el término "blockchain". En el contexto de Conflux, los bloques forman una estructura similar a un árbol, permitiendo la producción simultánea de múltiples bloques.

### **Cadena de bloques**
Una blockchain es un registro digital descentralizado y distribuido que registra transacciones en muchas computadoras para que cualquier registro involucrado no pueda ser modificado retroactivamente, sin la alteración de todos los bloques posteriores. Esta tecnología sustenta criptomonedas como Bitcoin y Ethereum, y es la tecnología fundamental para la red Conflux.

### **CFX**
CFX es la moneda nativa de la red Conflux. Es usado para incentivar el mantenimiento de la red Conflux y cobrar a los usuarios por el consumo de recursos. CFX juega un papel muy importante en la estabilidad del sistema, trabaja como recompensa por los mecanismos de consenso, las comisiones (fees) de cada transacción, y para la votación en la DAO.

La subdenominación más pequeña se denota por Drip, en la que todos los valores procesados en Conflux son enteros. Un CFX se define como 10^18 Drip. Las subdenominaciones de Conflux frecuentemente utilizadas se enumeran a continuación:

| Multiplicador (en Drip) |    Nombre    |
| ----------------------- |:------------:|
| 10^0                    |     Drip     |
| 10^9                    |    GDrip     |
| 10^12                   |     uCFX     |
| 10^18                   | Conflux(CFX) |

Para más información sobre la creación, distribución y lanzamiento de CFX, por favor consulte en:

- [White Paper de la Economía](https://confluxnetwork.org/files/Conflux_Economic_Paper_20201230.pdf)
- [El rol del token CFX en la red Conflux](https://medium.com/conflux-network/the-role-of-the-cfx-token-in-the-conflux-network-5a56c2b43bb0)
- [Votación de la DAO en cadena para los parámetros de la cadena](https://github.com/Conflux-Chain/CIPs/blob/master/CIPs/cip-94.md)
- [Economía](./economics.md)

### **ChainId & NetworkId**
`chainId` es un número que indica dónde se pretende ejecutar una transacción. Se utiliza para prevenir ataques de repetición de transacciones. El chainId de las cadenas Conflux son constantes, actualmente:

- Conflux Core Mainnet: `1029`
- Conflux Core Testnet: `1`
- Conflux eSpace Mainnet: `1030`
- Conflux eSpace Testnet: `71`

`networkId` se utiliza para distinguir entre blockchains en la capa de red. Actualmente Conflux mainnet/testnet `networkId` es igual que `chainId`. Puede obtener ambos mediante el método RPC `cfx_getStatus`.

### **Ecosistema de Conflux**
El ecosistema de Conflux se refiere a los diversos proyectos, aplicaciones, plataformas y servicios que han sido construidos o están integrados con la red Conflux. Esto incluye aplicaciones descentralizadas (DApps), plataformas de finanzas descentralizadas (DeFi), billeteras y más. El ecosistema de Conflux es una vibrante y creciente comunidad de desarrolladores, usuarios y organizaciones que contribuyen a la red Conflux.

### **Conflux Scan**
[Conflux Scan](https://confluxscan.io/) es el explorador oficial de blockchain para la red Conflux. Proporciona una interfaz fácil de usar, basada en detalles para que los usuarios puedan ver, confirmar e inspeccionar transacciones y contratos en la red Conflux. Con Conflux Scan, los usuarios pueden rastrear el estado de sus transacciones, ver el saldo de sus cuentas, explorar contratos inteligentes y mucho más.

### **Algoritmo de consenso**
Un algoritmo de consenso es un proceso en ciencias de la computación usado para alcanzar un acuerdo sobre un único valor de datos entre los procesos o sistemas distribuidos. En el contexto de blockchain, se utiliza para acordar el (total) orden de las transacciones. Conflux utiliza un algoritmo de consenso único basado en la estructura Tree-Graph, que permite un alto rendimiento y baja latencia en redes descentralizadas a gran escala.

### **DAG (Directed Acyclic Graph)**
En el contexto de Conflux, DAG se utiliza para representar la estructura de bloques de la red Conflux. A diferencia de los sistemas tradicionales de blockchain que siguen una cadena lineal, Conflux forma una estructura de bloques DAG, permitiendo que múltiples bloques se produzcan simultáneamente. Esta estructura es clave para que Conflux tenga la capacidad de lograr un alto rendimiento y baja latencia.

### **Aplicación descentralizada (DApp)**
Una aplicación descentralizada (DApp) es una aplicación de computadora que se ejecuta en un sistema de cómputo distribuido como una cadena de bloques. A diferencia de las aplicaciones tradicionales que funcionan en servidores centralizados, las DApps aprovechan el poder de la red peer-to-peer de la blockchain para proporcionar transparencia, inmutabilidad y resistencia a la censura. El framework típico de un DApp incluye 2 capas: el front-end o interfaz de usuario, y los contratos inteligentes que se ejecutan en la blockchain actuando como la lógica del back-end. El front-end, desarrollado usando lenguajes estándar como HTML, CSS y JavaScript, interactúa con la cadena de bloques a través de contratos inteligentes. Estos contratos inteligentes, escritos en idiomas como Solidity, definen las reglas y la lógica de la DApp, y se almacenan y ejecutan en la cadena de bloques, asegurando una operación consistente y de confianza.

### **Doble gasto**
El doble gasto es un defecto potencial en un sistema de dinero digital en el que se puede gastar más de una vez un solo token digital. Esto es posible porque un token digital consiste en un archivo digital que puede ser duplicado o falsificado. La red Conflux, al igual que otras redes de blockchain, utiliza un mecanismo de consenso para prevenir el doble gasto.

### **Epoch**

En Conflux,el epoch es la unidad fundamental que se utiliza para actualizar el estado general, estableciéndola aparte de blockchains como Bitcoin o Ethereum, donde las actualizaciones son realizadas por bloque. Epoch en Conflux es una partición específica de bloques que determina su orden total. Esta particióno se basa en la cadena pivot de la estructura Tree-Graph, y el bloque pivot será el último bloque en cada epoch. Una vez que se determina la cadena pivot y no se revierte, la partición de epochs se vuelve inmutable significa que el orden de las transacciones y los resultados de la ejecución no pueden cambiarse.

### **ERC20**
ERC20 es un estándar para tokens en la blockchain de Ethereum. Especifica un conjunto de funciones y eventos que un contrato de token tiene que implementar. While this is a standard on the Ethereum network, tokens on the Conflux network can also follow this standard, especially if they are transferred from the Ethereum network via the [Zero Gravity protocol](../tutorials/transferring-funds/across-chains/zero-gravity.md).

### **ERC721**
ERC721 is a standard for non-fungible tokens (NFTs) on the Ethereum blockchain. Unlike ERC20 tokens, which are identical to each other, each ERC721 token is unique. This makes them suitable for representing ownership of unique items or assets. Like ERC20, ERC721 tokens can also exist on the Conflux network, especially if they are transferred from the Ethereum network.

### **Fork**
In blockchain, a fork is a change to the software that creates two separate versions of the blockchain with a shared history. Forks can be either "hard" or "soft", depending on whether the change is compatible with previous versions of the software. In the context of Conflux, forks are less common due to the Tree-Graph structure of the network, which allows for concurrent block production.

### **Gas**
In the context of blockchain, gas refers to the fee required to successfully conduct a transaction or execute a contract on the Ethereum blockchain. In Conflux, the concept of gas also exists, but with a unique twist: the gas fee for contract execution is paid by contract sponsors, not by users. This improves the user experience by allowing users to interact with smart contracts without worrying about gas fees.

Refer to [Gas](./gas.md) for more information.

### **GHAST**
GHAST (Greedy Heaviest Adaptive SubTree) is the Conflux protocol's rule for selecting a chain from the Tree-Graph structure. It's designed to ensure safety and liveness properties in the network. GHAST is a key part of Conflux's unique consensus mechanism.

Refer to [GHAST](../conflux-basics/consensus-mechanisms/proof-of-work/ghast.md) for more information.

### **Hard Fork**
A hard fork is a type of fork that creates a permanent divergence from the previous version of the blockchain. Nodes running the old version will not be accepted by the new version. This is a common concept in many blockchains, but due to the unique structure of Conflux, hard forks are less common.

### **Hash**
A hash is a function that converts the input data into an encrypted output of a fixed length. In the context of blockchain, a hash function is used to secure data. Each block in a blockchain has a unique hash, and any change to the block's data will result in a different hash.

### **Internal Transactions**
Internal transactions in blockchain refer to value transfers or operations within a smart contract. These transactions are triggered by external transactions and can involve actions such as transferring tokens, creating new tokens, executing function calls, or interacting with other smart contracts. These transactions are not recorded individually on the blockchain, but they can be tracked and displayed for analysis and visibility.

[ConfluxScan](https://confluxscan.io) and [trace JSON-RPC API](../../core/build/json-rpc/trace-namespace.md) can track and display internal transactions for analysis and visibility.

Related links:

- [trace JSON-RPC API](../../core/build/json-rpc/trace-namespace.md)

### **Merkle Tree**
A Merkle tree, in cryptography and computer science, is a tree in which every leaf node is labelled with the hash of a data block, and every non-leaf node is labelled with the cryptographic hash of the labels of its child nodes. Merkle trees are used in blockchains to efficiently verify the contents of large data structures.

### **Mining**
Mining is like a competition where people use powerful computers to solve puzzles. Each puzzle solved helps confirm new transactions and safely add them to the blockchain. Think of **miners** as special participants who use advanced equipment, like ASICs or high-performance GPUs, to take part in this puzzle-solving contest. The contest involves lots of trial and error to find a special code (hash value) that fits certain rules. When a miner finds the right code, it's like they win the round, allowing them to add a page (block) of confirmed transactions to the ledger. The first one to do this gets a prize in the form of digital money (cryptocurrency). In the Conflux network, this process helps to build a unique ledger structure known as the Tree-Graph, which organizes transactions in a special way.

Refer to [Mining](../mine-stake/mine/running-mining-node.md) for more information about running a mining node.

### **Node**
In the context of blockchain, a node is a server that participates in the blockchain network. Each node keeps a copy of the blockchain in some way (depending on its type) and follows the rules of the network. Nodes validate transactions, maintaining the network's security and decentralization.

Refer to [Run a Node](../run-a-node) section for more information about running nodes.

### **Nonce**
In blockchain technology, nonce ("number only used once") has different meaning in different context.

In mining, nonce is a number added to let the block header meet the difficulty level restrictions. The nonce is the number that blockchain miners are solving for.

In transaction, nonce is the execution sequence number of transactions sent from an account. A transaction with incorrect nonce won't be included in blockchain, so correctly setting the nonce is critical to transaction execution. Refer to [nonce](/docs/core/core-space-basics/transactions/tx-fields.md#nonce) for more information.

### **Oracles**
In the context of blockchains and smart contracts, an oracle is an agent that finds and verifies real-world occurrences and submits this information to a blockchain to be used by smart contracts. Oracles are used in the Conflux network to bring external information into smart contracts, enabling them to interact with the outside world.

### **Peer-to-Peer Network (P2P)**
A peer-to-peer network is one in which each computer in the network can act as a client or server for the other computers in the network, allowing shared access to files and peripherals without the need for a central server. Conflux, like other blockchain networks, operates as a peer-to-peer network, with each node communicating directly with others.

### **Proof of Stake (PoS)**
Proof of Stake (PoS) is a type of consensus algorithm where block creators are chosen based on the number of tokens they hold or are willing to "stake". PoS is used in the Conflux network to prevent 51% attacks and to finalize blocks.

Refer to [PoS](../conflux-basics/consensus-mechanisms/proof-of-stake/pos_overview.md) for more information.

### **Proof of Work (PoW)**
Proof of Work (PoW) is a type of consensus algorithm where the first participant to solve a complex mathematical problem gets to add a new block to the blockchain. PoW is used in many blockchains, including Bitcoin and Ethereum before September 15, 2022. While Conflux uses a unique consensus mechanism based on a Tree-Graph structure, it shares similarities with PoW in terms of incentivizing participants to maintain the network.

Refer to [PoW](../conflux-basics/consensus-mechanisms/proof-of-work/proof-of-work.mdx) for more information.

### **Public/Private Key**
A public key is a cryptographic code that allows a user to receive cryptocurrencies into his or her account. The private key is used to sign transactions or digital messages and the public key is used to verify the signature. In the context of Conflux, users have a pair of public and private keys that they use to interact with the network.

### **Smart Contract**
A smart contract is a self-executing contract with the terms of the agreement directly written into code. They run on the blockchain, so they are stored on a public database and cannot be changed. In the Conflux network, users can create and interact with smart contracts, which can automate a wide range of applications and processes.

### **Space**
In the Conflux network, "Space" refers to a specific environment within the network. For example, Core Space refers to the original Conflux network, while eSpace is the virtualized Ethereum chain running on top of the Core Space network. The two spaces are logically independent of each other and do not affect each other except for certain cross-space operations.

Refer to [Spaces](./spaces.md) for more information.

### **Sponsorship Mechanism**
In Conflux, the transaction fee for contract execution can be paid by users but also by contract sponsors. This sponsorship mechanism allows DApp users on Conflux to not worry about gas fees, improving user experience. Sponsors can set up a sponsorship by depositing CFX into a contract.

Refer to [Sponsor Mechanism](../../core/core-space-basics/sponsor-mechanism.md) for more information.

### **Staking (in Conflux)**
Staking in Conflux typically refers to the PoS staking, the process of participating in the network PoS consensus by locking up a certain amount of CFX. Stakers can earn rewards for their participation. This mechanism helps to secure the network and incentivize participation.

Refer to [Staking FAQs](../mine-stake/stake/faqs.md) for more information.

### **Transactions**
A Conflux transaction is a single instruction composed by an external actor with a Conflux account, and this instruction is cryptographically signed using the sender account's private key to prevent transaction forge. A transaction can involve a simple transfer of CFX (the native currency of Conflux), a transfer of tokens (such as ERC20 or ERC721), a deployment of a new smart contract, or an execution of a function on an existing smart contract. Transactions are the only way to store or update data on the blockchain.

Refer to [Transactions](./transactions.md) for more information.

### **Tree Graph**
In the context of Conflux, the Tree-Graph is a novel consensus mechanism that allows for high throughput and low latency in large-scale decentralized networks. Unlike traditional blockchain systems that follow a linear chain, Conflux forms a tree-like structure of blocks, allowing for multiple blocks to be produced concurrently. This structure is key to Conflux's ability to process a high number of transactions per second.

Refer to [Tree-Graph](../conflux-basics/consensus-mechanisms/proof-of-work/tree-graph.md) for more information.


### **Wallet (billetera)**
In the context of blockchain, a wallet is a digital place to store cryptocurrency. It can be in the form of a software (online or offline) or hardware device. In the Conflux Network, users can use wallets like Fluent to manage their CFX and interact with the network.

Refer to [Wallets](../tutorials/wallets/wallets.mdx) for more information about supported wallets.
