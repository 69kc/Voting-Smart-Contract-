# Voting-Smart-Contract-

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
