---
layout: post
title:  "Installing the Scala IDE for Eclipse with the Scala Worksheet on Windows"
date:   2019-09-08
desc: "Installing the Scala IDE for Eclipse with the Scala Worksheet on Windows"
keywords: "Scala IDE, Eclipse, Scala Worksheet"
categories: [Open source]
tags: [Scala IDE, Scala Worksheet, Eclipse]
icon: icon-html
---

Scala IDE provides advanced editing and debugging support for the development of pure Scala and mixed Scala-Java applications.

You can download the Scala IDE for eclipse with the Scala Worksheet pre-installed from the following link below:

<a href="http://scala-ide.org/download/sdk.html">Download Scala IDE</a> (Make sure to download the IDE for Scala version 2.11.x!)

After downloading the archive for your operating system, simply unpack it and start eclipse. Eclipse requires you to select a workspace on startup. 

<b>Hello World Example: Scala IDE and the Scala Worksheet</b>

To familiarize yourself with the Scala IDE, create a simple "Hello World" project in eclipse:

1. Go to "File" - "New" - "Other..." and select "Scala Project" from the folder "Scala Wizards"

2. Choose a project name and select "Finish"

3. Select "File" - "New" - "Scala Object" to create a new object

4. Enter Hello as the name for the object

5. Change the source code to below:
  
     object Hello extends App {
        println("Hello, world!")
     }
   
6. Save the file and select from the top menu bar, "Run" -> "Run as" -> "Scala Application"

You should see a the hello world output in the Eclipse console:

Hello, world!
