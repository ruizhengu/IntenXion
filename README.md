# IntenXion

IntenXion is a test automation framework for XR applications developed with Unity, providing a set of testing APIs.

The repo contains the API set and the Unity XR project `VR Template` for our evaluation.

# Background

How to test Unity projects with Unity Test Framework: [Testing your code](https://docs.unity3d.com/6000.2/Documentation/Manual/test-framework/test-framework-introduction.html)

# Instructions

### Test Assembly

1. Create a test assembly following the guidelines provided by Unity Test Framework.
2. Set the assembly to support Play mode tests.
3. Add necessary Assembly Definition References (dependencies of the tests).

![Assembly Definition References](./figure/assembly_definition_references.png)

4. Alternatively, copy the `/IntenXion/lib/Tests.asmdef` to the `/Assets/Tests` folder of the Unity XR project under test.

### Write test cases

1. Copy the `.cs` files in the `/IntenXion/lib` to the `/Assets/Tests` folder.
2. Follow the templates provided by `TestTemplate.cs` to develop your test cases.

### Exeute test cases

1. In Unity Editor, open **Window > General > Test Runner**.
2. Select **PlayMode** in the **Test Runner**.
3. Find the test case(s) you would like to execute, double click it or click **Run Selected test(s)**.

* Currently, the Test Runner only supports executing one single test case, running multiple tests in one execution will cause errors. The issue is reported to Unity to be resolved. Unity Issue Link: [IN-111168](https://unity3d.atlassian.net/servicedesk/customer/portal/2/IN-111168).

# Examples

## Basic Usage

```c#
// Create an action sequence with ActionBuilder
var action = new ActionBuilder(this);
action.GrabHold(1.0f)
      .MoveUp(0.5f);
yield return action.Execute();
```

## Available APIs

### Navigation

* `NavigateTo`

### Selection

* `MoveControllerTo`
* `Grab`
* `GrabHold`
* `Trigger`
* `TriggerHold`

### Manipulation

* `MoveUp`
* `MoveDown`
* `MoveForward`
* `MoveBackward`
* `MoveLeft`
* `MoveRight`
* `RotateUp`
* `RotateDown`
* `RotateLeft`
* `RotateRight`
* `ReleaseAllKeys`

### Assertion

* `AssertGrabbed`
* `AssertTriggered`
* `AssertTranslated`
* `AssertRotated`

