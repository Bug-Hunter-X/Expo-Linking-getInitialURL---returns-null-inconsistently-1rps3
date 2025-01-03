# Expo Linking.getInitialURL() Inconsistent null Return

This repository demonstrates a bug where `Expo.Linking.getInitialURL()` inconsistently returns `null`, even when a deep link is successfully opened. This can lead to unexpected app behavior and makes it difficult to reliably handle deep links.

## Problem

The `Linking.getInitialURL()` method is intended to retrieve the initial URL that launched the app. However, in some cases, it returns `null` even when a valid deep link is used to open the app. This behavior is inconsistent and makes handling deep links challenging.

## Solution

The provided solution implements a retry mechanism with exponential backoff. This approach enhances the reliability of retrieving the initial URL, accounting for potential delays in the Linking API's response. It also includes better error handling to provide more informative feedback to the user and the developer.