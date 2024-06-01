// Define the NFT collection
class NFTCollection {
  constructor() {
    this.nfts = [];
  }

  // Method to mint a new NFT
  mintNFT(name, creator, description) {
    const nft = {
      id: this.nfts.length + 1,
      name: name,
      creator: creator,
      description: description,
      mintedAt: new Date()
    };
    this.nfts.push(nft);
    console.log(`NFT Minted: ${nft.name} by ${nft.creator}`);
  }

  // Method to print details of all NFTs
  printNFTDetails() {
    console.log('NFT Collection Details:');
    this.nfts.forEach(nft => {
      console.log(`ID: ${nft.id}, Name: ${nft.name}, Creator: ${nft.creator}, Description: ${nft.description}, Minted At: ${nft.mintedAt}`);
    });
  }

  // Method to print the total supply of NFTs
  printTotalSupply() {
    console.log(`Total NFT Supply: ${this.nfts.length}`);
  }
}

// Create an instance of the NFTCollection
const myNFTCollection = new NFTCollection();

// Minting at least three NFTs
myNFTCollection.mintNFT('NFT One', 'Alice', 'The first NFT in the collection.');
myNFTCollection.mintNFT('NFT Two', 'Bob', 'The second NFT in the collection.');
myNFTCollection.mintNFT('NFT Three', 'Charlie', 'The third NFT in the collection.');

// Print details of all NFTs
myNFTCollection.printNFTDetails();

// Print the total supply of NFTs
myNFTCollection.printTotalSupply();
