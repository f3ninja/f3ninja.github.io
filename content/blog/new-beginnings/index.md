---
title: JavaScript Architecture Application
date: "2020-07-06T22:40:32.169Z"
description: What is JS architect application.
---

## Single Page Applications(SPAs)

It is sometimes referred to as Single Page Interface (SPI). This is the most common form of JavaScript applications available these days. These are a lot more responsive and resemble a desktop application. Unlike other web applications, these load the complete webpage with HTML, CSS, and JavaScript initially. Though the initial loading of the webpage takes time, it works faster with other user requests. The only disadvantage these applications have is that they rely heavily on JavaScript and thus reduce browsing speed in low power devices. Some examples of SPAs are Gmail, Facebook, Twitter, etc.

## Multi-page Applications
These applications work in a “traditional” way. This means that every change in the web application requests a new page from the server. They are larger than SPAs and take more time than necessary. We have to transfer a lot of data between the server and the browser which reduces the application’s speed. Even though it is much easier these days to do that with the help of AJAX (Asynchronous JavaScript), it isn’t very popular. AJAX allows us to refresh only certain sections of the applications without reloading the complete application. But using these applications adds complexity for the programmer and these are difficult to develop as compared to the SPAs.

## Isomorphic (Universal) Applications
JavaScript applications became ‘Isomorphic’ with the release of NodeJS i.e. they can execute on both client-side and server-side. These applications are very useful when you need faster interaction with the web pages. The same code must be compatible to execute on both the client-side and server-side to render the application components. Unlike SPAs, these applications support older devices and work even with poor internet connections. These applications have a lesser code, but this also makes them difficult to debug.