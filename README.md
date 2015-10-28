---
layout: post
title: Getting started guide for JBoss Fuse (with Fabric8)
published: false
categories:
    - technical
tags:
    - Integration
    - jboss-fuse
    - fabric8
    - how-to
---

# Overview of JBoss Fuse
[JBoss Fuse][471ee006] is a lightweight _enterprise service bus (ESB)_ with an elastic footprint that supports integration in the cloud.
JBoss Fuse allows deployment in several different configurations facilitating intelligent integration - on premise or in the cloud.

## Components of JBoss Fuse
1. Apache Camel - compose your integration applications using standard _Enterprise Integration Patterns (EIPs)_
2. Apache CXF - allows web service (SOAP and REST) integration
3. Apache ActiveMQ - provides core messaging with ESB and integration with external applications
4. Apache Karaf - offers a lightweight [OSGi](http://www.osgi.org/Main/HomePage) based container
5. Fabric8 - simplifies management of distributed JBoss Fuse deployments from a central location

## Getting started
We will be using [JBoss Development Studio (JBDS)][ec7a0d7a] as the development IDE.

1. Create a simple [maven][faab988c] project with packaging type as _bundle_
2. Add following JBoss related maven repositories to resolve dependencies

    ``` xml
    <repositories>
        <repository>
            <id>jboss.m2</id>
            <name>JBoss Community Release Repository</name>
            <url>http://origin-repository.jboss.org/nexus/content/groups/public-jboss/</url>
            <layout>default</layout>
        </repository>
        <repository>
            <id>jboss.ea</id>
            <name>JBoss Community Early Access Release Repository</name>
            <url>http://origin-repository.jboss.org/nexus/content/groups/ea</url>
            <layout>default</layout>
        </repository>
    </repositories>

    <pluginRepositories>
        <pluginRepository>
            <id>jboss.m2</id>
            <name>JBoss Community Release Repository</name>
            <url>http://origin-repository.jboss.org/nexus/content/groups/public-jboss/</url>
            <layout>default</layout>
        </pluginRepository>
        <pluginRepository>
            <id>jboss.ea</id>
            <name>JBoss Community Early Access Release Repository</name>
            <url>http://origin-repository.jboss.org/nexus/content/groups/ea</url>
            <layout>default</layout>
        </pluginRepository>
    </pluginRepositories>
    ```

+ Add appropriate JBoss Fuse version as a property to the pom

    ``` xml
    <version.jboss.fuse>6.2.1.redhat-070</version.jboss.fuse>
    ```
