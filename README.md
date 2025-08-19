# IntenXion

IntenXion is a test automation framework for XR applications developed with Unity.

# Background

How to test Unity projects with Unity Test Framework: [Testing your code](https://docs.unity3d.com/6000.2/Documentation/Manual/test-framework/test-framework-introduction.html)

# Examples

## Basic Usage

```c#
// Create an action sequence with ActionBuilder
var action = new ActionBuilder(this);
action.GrabHold(1.0f)
      .MoveUp(0.5f);
yield return action.Execute();
```

## Available Actions

### Navigation

### Selection

### Manipulation

