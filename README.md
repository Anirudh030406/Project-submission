/*
Assessment Requirements
1. Create a variable that can hold a number of NFT's. What type of variable might this be?
2. Create an object inside your mintNFT function that will hold the metadata for your NFTs. 
   The metadata values will be passed to the function as parameters. When the NFT is ready, 
   you will store it in the variable you created in step 1
3. Your listNFTs() function will print all of your NFTs metadata to the console (i.e. console.log("Name: " + someNFT.name))
4. For good measure, getTotalSupply() should return the number of NFT's you have created
*/

// create a variable to hold your NFT's
const NFTHolder =[];

// this function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function mintNFT (id,name, age, screentime, grade) {
    const student = {
    "id": id,
    "name": name,
    "age" : age,
    "screentime(in Hours)" :screentime,
    "grade" : grade
    }
    NFTHolder.push(student);
}

// create a "loop" that will go through an "array" of NFT's
// and print their metadata with console.log()
function listNFTs () {
   for(let i=0; i<NFTHolder.length;i++){
      console.log(NFTHolder[i])
   }
}

// print the total number of NFTs we have minted to the console
function getTotalSupply() {
    const total_supply = NFTHolder.length;
    console.log(total_supply);
}

// call your functions below this line

mintNFT("12994","Anirudh",21,4,"A");    //1
mintNFT("12134","Rowan",18,10,"B");     //2
mintNFT("14421","Ajay",24,15,"C");      //3
mintNFT("16473","Jack",20,13,"B");      //4

console.log("The NFTs are provided to you below:\n")
listNFTs();
console.log("Total number of NFTs are:\t")
getTotalSupply();
