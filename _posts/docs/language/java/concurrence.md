---
title: Java进阶
author: teen
date: 2023-08-10
category: language/java
layout: post
---

## 一、前言

本部分内容是关于Java并发的一些知识总结，既是学习的难点，同时也是面试中几乎必问的知识点。

面试中可能会问的一些问题：

- 创建线程的方式
- Synchronized/ReentrantLock 
- 生产者/消费者模式
- volatile关键字
- 乐观锁/悲观锁
- 死锁
- 了解的并发集合

因此针对以上问题，整理了相关内容。

## 二、目录

- [Java创建线程的三种方式](/docs/language/java/concurrence/CreateThread.md)
- [Java线程池](/docs/language/java/concurrence/thread-pool.md)
- [死锁](/docs/language/java/concurrence/deadlock.md)
- [Synchronized/ReentrantLock](/docs/language/java/concurrence/synchronized-reentrantlock.md)
- [生产者/消费者模式](/docs/language/java/concurrence/producer-consumer.md)
- [volatile关键字](/docs/language/java/concurrence/volatile.md)
- [CAS原子操作](/docs/language/java/concurrence/CAS.md)
- [AbstractQueuedSynchronizer详解](/docs/language/java/concurrence/AbstractQueuedSynchronizer.md)
- [深入理解ReentrantLock](/docs/language/java/concurrence/ReentrantLock.md)
- [Java并发集合——ArrayBlockingQueue](/docs/language/java/concurrence/ArrayBlockingQueue.md)
- [Java并发集合——LinkedBlockingQueue](/docs/language/java/concurrence/LinkedBlockingQueue.md)
- [Java并发集合——ConcurrentHashMap](/docs/language/java/concurrence/ConcurrentHashMap.md)