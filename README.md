# StudentRecord.sol
Base - Smart Contract Deployed by Remix StudentRecord.sol
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract StudentRecord {
    struct Student {
        string name;
        uint score;
    }

    Student[] public students;

    function addStudent(string memory _name, uint _score) public {
        students.push(Student(_name, _score));
    }

    function getStudentCount() public view returns (uint) {
        return students.length;
    }
}
