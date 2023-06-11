# Redirecting-the-scene

## Aim:

To redirect a scene using C# program in Unity engine.

## Algorithm:

### Step 1:

To open the unity engine.

### Step 2:

Create a new plane and create a cube and give color for the cube.

### Step 3:

Next create sphere in the orgin and change the z-axis and Give the color for the sphere.

### Step 4:

Create a tag for the Sphere and Make the sphere and cube as a Rigidbodies and Make the sphere use Gravity.

### Step 5:

Create the C# script file in the Assets and write the Coding for the Redirecting to the scene1 after hit the sphere to cube.

### Step 6:

Next Create a another new scene named as scene1.

### Step 7:

In File->Build settings and drop the both first scene and scene1 scene in the Scenes in build setting.

### Step 8:

Click the Build and run button in the Build settings and run the scene.

### Step 9:

The Sphere after touching the cube it will disappeared and Press the key [R] the redircting to the new scene that is scene1.

## Program:
~~~
using System.Collections;
using System.Collections.Generic;
using UnityEngine.SceneManagement;
using UnityEngine;

public class objectone1 : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinText;
    // Start is called before the first frame update
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("exp71");
        }
    }
    public void OnMouseDown()
    {
        Destroy(gameObject);
    }
    private void OnCollisionEnter(Collision collision)
    {
        if (collision.gameObject.tag == "square")
        {
            Destroy(collision.gameObject);
            WinText.SetActive(true);
        }
    }
}
~~~

## Output:

![img 1](https://github.com/ragulmani936/Redirecting-the-scene/assets/94881918/4a5657ab-5b18-48e2-b3af-4b1b62f18377)

![img 2](https://github.com/ragulmani936/Redirecting-the-scene/assets/94881918/e6f11739-6b8b-4e7a-906c-131a6225a0b8)

![img 3](https://github.com/ragulmani936/Redirecting-the-scene/assets/94881918/0620e4c0-8d0e-44df-b472-f7d7358085f2)

## Result:

Thus, a scene is redirected in Unity engine using a C# program.
