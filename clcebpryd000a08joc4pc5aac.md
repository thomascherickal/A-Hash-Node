---
title: "Part 7: Source Code for a TDD Telephone Directory in Golang"
datePublished: Mon Jan 02 2023 04:50:38 GMT+0000 (Coordinated Universal Time)
cuid: clcebpryd000a08joc4pc5aac
slug: part-7-source-code-for-a-tdd-telephone-directory-in-golang
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1672635021303/3fa84b3d-92bc-4899-9930-aee94d8a7a1b.jpeg
tags: tdd, go, google, abcd

---

Here is an example of a simple telephone directory implemented in Go using Test-Driven Development (TDD) principles:

```go
package main

import (
	"fmt"
	"strings"
)

type Directory struct {
	contacts map[string]string
}

func (d *Directory) AddContact(name, phoneNumber string) {
	d.contacts[name] = phoneNumber
}

func (d *Directory) RemoveContact(name string) {
	delete(d.contacts, name)
}

func (d *Directory) UpdateContact(name, phoneNumber string) {
	d.contacts[name] = phoneNumber
}

func (d *Directory) FindContact(name string) (string, bool) {
	phoneNumber, ok := d.contacts[name]
	return phoneNumber, ok
}

func (d *Directory) FindContacts(query string) []string {
	var results []string
	for name, phoneNumber := range d.contacts {
		if strings.Contains(strings.ToLower(name), strings.ToLower(query)) {
			results = append(results, fmt.Sprintf("%s: %s", name, phoneNumber))
		}
	}
	return results
}

func main() {
	// Test the Directory using TDD principles
	d := &Directory{
		contacts: make(map[string]string),
	}
	d.AddContact("Alice", "123-456-7890")
	d.AddContact("Bob", "234-567-8901")
	d.AddContact("Eve", "345-678-9012")

	if phoneNumber, ok := d.FindContact("Alice"); !ok || phoneNumber != "123-456-7890" {
		fmt.Println("Error: Alice's phone number not found or incorrect")
	}
	if phoneNumber, ok := d.FindContact("Charlie"); ok {
		fmt.Println("Error: Charlie should not be in the directory")
	}

	d.UpdateContact("Bob", "333-333-3333")
	if phoneNumber, ok := d.FindContact("Bob"); !ok || phoneNumber != "333-333-3333" {
		fmt.Println("Error: Bob's phone number not updated correctly")
	}

	d.RemoveContact("Eve")
	if _, ok := d.FindContact("Eve"); ok {
		fmt.Println("Error: Eve should have been removed from the directory")
	}

	results := d.FindContacts("b")
	if len(results) != 1 || results[0] != "Bob: 333-333-3333" {
		fmt.Println("Error: FindContacts not working correctly")
	}

	fmt.Println("All tests pass.")
}
```

This code defines a `Directory` struct that has a `contacts` map field to store the name-phone number pairs. It also defines several methods to add, remove, update, and find contacts in the directory. Finally, it has a `main` function that tests these methods using TDD principles.

Next : [Reinforcement Learning for Table Tennis Game with Graphics in Python](https://hashnode.com/post/clcecz9sk000g08l1h7c8b2yz)