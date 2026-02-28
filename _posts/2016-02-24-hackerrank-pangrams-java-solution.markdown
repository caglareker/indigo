---
title: "Hackerrank Pangrams Algorithm Java Solution"
layout: post
date: 2016-02-24 22:44
image: /assets/images/markdown.jpg
headerImage: false
tag:
- hackerrank
- pangrams
- algorithm
star: false
category: blog
author: caglareker
description: Hackerrank pangrams solution
---

## Problem

Problem detail <a class="link" data-title="Hackerrank" href="https://www.hackerrank.com/challenges/pangrams/problem" target="_blank">Hackerrank</a>.

## Java Solution

{% highlight java %}
package com.caglar.hackerrank;

public class Pangrams {

    public static String pangrams(String s) {
        String str = s.toLowerCase();
        for (char c = 'a'; c <= 'z'; c++) {
            if (str.indexOf(c) < 0) return "not pangrams";
        }
        return "pangrams";
    }

    public static void main(String[] args) {
        System.out.println(pangrams("We promptly judged antique ivory buckles for the next prize"));
    }

}
{% endhighlight %}