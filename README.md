# Arrays-and-Struct
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract Storage {
    struct Animals {
        string name;
        string species;
        uint256 ages;
    }

    Animals[] public listOfAnimals;

    constructor () {
        listOfAnimals.push(Animals("Jon", "Cat", 5));
        listOfAnimals.push(Animals("Cena", "Dog", 6));
        listOfAnimals.push(Animals("Jim", "Mouse", 3));
    }

    function addAnimals (string memory _name, string memory _species, uint256 _ages) public {
        listOfAnimals.push(Animals(_name, _species, _ages));
    }

}
