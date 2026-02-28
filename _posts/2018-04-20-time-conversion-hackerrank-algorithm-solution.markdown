---
title: "Hackerrank Time Conversion Algorithm Java Solution"
layout: post
date: 2018-04-20 18:00
image: /assets/images/markdown.jpg
headerImage: false
tag:
- hackerrank
- algorithm
star: false
category: blog
author: caglareker
description: Hackerrank time conversion algorithm java solution
---

## Problem

Problem detail <a class="link" data-title="Hackerrank" href="https://www.hackerrank.com/challenges/time-conversion/problem" target="_blank">Hackerrank</a>.

## Java Solution

{% highlight java %}
package com.caglar.hackerrank;

import java.util.Scanner;

public class TimeConversion {

    public static String timeConversion(String s) {
        String[] split = s.split(":");
        String outputTime;
        String hour = split[0];
        String minutes = split[1];
        String seconds = split[2].substring(0, 2);
        if (s.endsWith("AM")) {
            if (hour.equals("12")) {
                hour = "00";
            }
        } else {
            if (!hour.equals("12")) {
                int h = Integer.parseInt(hour);
                h += 12;
                hour = String.valueOf(h);
            }
        }
        outputTime = hour + ":" + minutes + ":" + seconds;
        return outputTime;
    }

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        String inputString = in.nextLine();
        System.out.println(timeConversion(inputString));
    }

}
{% endhighlight %}