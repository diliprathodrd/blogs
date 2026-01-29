---
title: "TCP Working: 3-Way Handshake & Reliable Communication"
seoTitle: "TCP Working: 3-Way Handshake & Reliable Communication"
seoDescription: "TCP Working: 3-Way Handshake & Reliable Communication"
datePublished: Thu Jan 29 2026 02:05:38 GMT+0000 (Coordinated Universal Time)
cuid: cmkytb79d000702jmeoupf2xb
slug: tcp-working-3-way-handshake-and-reliable-communication
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1769651643604/9c9727e9-435d-461f-b955-bbfe19c499a5.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1769652289210/f6274f98-6d45-4407-9337-8311ac78b48b.png
tags: chaicode

---

## What is TCP and Why It Is Needed

When computers communicate over a network, data is broken into small pieces and sent independently. If there are no rules, these pieces can arrive late, out of order, duplicated, or not arrive at all. The internet itself does not guarantee correctness. This is why TCP exists.

TCP, or Transmission Control Protocol, is designed to make communication **reliable**. It ensures that data sent from one machine reaches the other machine completely, in the correct order, and without corruption. Most applications that care about accuracy depend on TCP.

## Problems TCP Is Designed to Solve

Without TCP, a sender would have no idea whether data reached the receiver. Some packets might be lost due to congestion. Others might arrive in a different order. The receiver could receive duplicate data or incomplete information. TCP solves these problems by adding rules for connection setup, ordering, acknowledgements, and retransmission.

In short, TCP exists to turn an unreliable network into a reliable communication channel.

## What Is the TCP 3-Way Handshake

Before any actual data is sent, TCP first establishes a connection between the client and the server. This setup process is called the **3-way handshake**.

The purpose of the handshake is to make sure both sides are ready to communicate, agree on starting parameters, and synchronize their communication state. Only after this handshake is complete does data transfer begin.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1769651971508/b5c88c05-6631-405c-a6b3-e8d152030f0f.png align="center")

## Step-by-Step Working of SYN, SYN-ACK, and ACK

The handshake works like a short conversation.

First, the client sends a message saying it wants to start communication. This message is called **SYN** (synchronize). It also includes an initial sequence number to track data later.

Next, the server responds with **SYN-ACK**. This means the server acknowledges the client’s request and sends its own synchronization information.

Finally, the client replies with **ACK**, acknowledging the server’s response. At this point, both sides know the connection is established, and data transfer can safely begin.

## How Data Transfer Works in TCP

Once the connection is established, data is sent in segments. Each segment has a sequence number. The receiver uses these numbers to reorder data correctly and detect missing pieces. After receiving data, the receiver sends acknowledgements back to the sender, confirming what has been received successfully.

This constant feedback loop allows TCP to manage communication smoothly.

## How TCP Ensures Reliability, Order, and Correctness

TCP ensures reliability by requiring acknowledgements for received data. If the sender does not receive an acknowledgement within a certain time, it assumes the data was lost and sends it again.

Ordering is maintained using sequence numbers, so even if data arrives out of order, it can be reconstructed correctly. Error detection mechanisms ensure corrupted data is discarded and retransmitted.

## How a TCP Connection Is Closed

When communication is complete, TCP does not simply stop. The connection is closed in an orderly way using **FIN** and **ACK** messages. One side sends a FIN to indicate it has finished sending data. The other side acknowledges it and sends its own FIN when ready. After the final acknowledgement, the connection is safely closed.

This careful shutdown ensures no data is lost at the end of communication.

TCP may seem complex, but every part of it exists to solve a real problem. The 3-way handshake, acknowledgements, and controlled shutdown together make reliable communication possible on an unreliable network.