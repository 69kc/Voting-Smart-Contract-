# Voting-Smart-Contract-
A voting smart contract is a more complex smart contract that can be used to conduct secure and transparent voting. This is an excellent way to learn how to create a smart contract that interacts with multiple parties. The following code shows how to create a basic voting smart contract:

pragma solidity ^0.8.0;

contract Voting {
    mapping(bytes32 => uint256) public votes;

    function vote(bytes32 candidate) public {
        require(votes[candidate] >= 0);
        votes[candidate] += 1;
    }

    function getVotes(bytes32 candidate) public view returns (uint256) {
        return votes[candidate];
    }
}
