The pr# MISYS
Project Json


Synopsis :

The project's goal is to do a bower module which allow someone to edit a JSON file thanks to a HTML form.
We have to manage any type of fields (input, checkbox, textearea, radio button) and create a github.
The project must run with a simple "bower install".
--------------------------------------------------------------------------------------------------------------------------
Code example :

var app = angular.module('myApp', []);
        // Anf=gularjs controller control the data of Angularjs application
		
     app.controller('customersCtrl', function($scope, $http) {
        
        //the angularjs function .get is used to recover a file	
     $http.get('studentc.json').then(function (response) {
     $scope.myData = response.data.student;
   });
        // the function .post serves to display the modification in the Json file
     $scope.save = function() {            						
     $http.post('studentc.json', $scope.myData).then(function(response) {
            
        // The last line serves display the new Json file
     $scope.msg = 'Data sent: '+ JSON.stringify($scope.myData);
    });
    };
  });
  
for use this js code we have to use the framework Angularsjs.
		//this tag connect the code and the Angularjs. 
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.1.5/angular.min.js"></script>  
------------------------------------------------------------------------------------------------------------------------
Motivation

We choised this project for increase our skills in JavaScript, to learn about JSON file and how to use github
------------------------------------------------------------------------------------------------------------------------
Tests

To run the project we needed a localhost (WampsServer) to separate the JSON and the js file because we cannot read the JSON file without it.







