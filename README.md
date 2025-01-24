# React Native FlatList Blank Rendering Bug

This repository demonstrates a common bug in React Native where a FlatList component renders blank after asynchronously fetching data, even when the data fetch is successful.  The issue is related to how state updates are handled within the component's lifecycle.

## Bug Description

The provided code attempts to fetch data from an API.  While the fetch is successful, and the data is successfully set in the `data` state variable, the FlatList does not render the items.  The loading indicator correctly appears and disappears, but the list remains empty.

## Solution

The solution addresses the issue by ensuring that the component re-renders after the data has been fetched successfully. The `useEffect` hook is used to trigger a re-render once the `data` state has changed.