package com.example.demo.controller;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;

import com.example.demo.model.Person;
import com.example.demo.service.PersonService;

@RestController
public class PersonController {

	 @Autowired
	 private PersonService personService;
	 
	 @RequestMapping("/create")
	 public String create(@RequestParam String firstName, @RequestParam String lastName,@RequestParam int age) {
		 Person p = personService.create(firstName, lastName, age);
		 return p.toString();
	 }
	 
	 @RequestMapping("/get")
	 public Person getPerson(@RequestParam String firstName) {
		 return personService.getByFirstName(firstName); 
	 }
	 
	 @RequestMapping("/update")
	 public String update (@RequestParam String firstName, @RequestParam String lastName,@RequestParam int age) {
		 Person p = personService.update(firstName, lastName, age);
		 return p.toString();
	 }
	 
	 @RequestMapping("/delete")
	 public String delete(@RequestParam String firstName) {
		 personService.delete(firstName);
		 return "deleted"+firstName;
	 }
	 
}

