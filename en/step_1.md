Navigate to your 'Scripts' folder and choose 'Create -> C# Script'.

Name the Script `PlaySound`.

Open the `PlaySound` script.

Enter the following code:

--- code ---
---
language: cs
filename: PlaySound.cs
line_numbers: true
line_number_start: 1
line_highlights: 
---

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlaySound : MonoBehaviour
{
    AudioSource audioSource;

    // Start is called before the first frame update
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        
    }

    void OnCollisionEnter(Collision other)
    {
        if (other.gameObject.CompareTag("Player"))
        {
            audioSource = this.gameObject.GetComponent<AudioSource>();
            audioSource.Play();
        }
    }
}

--- /code ---

**Save** and return to Unity.

Make sure that your ball is tagged with the 'Player' tag.

Select the GameObject that you wish to add a sound to.

Drag the `PlaySound` script onto the 'Add Component' area of the 'Inspector' window.

In the 'Inspector' window, click on 'Add Component'.

Add an 'AudioSource' component.

Uncheck the 'Play On Awake' box.

Drag your chosen sound onto the 'Audio Source'.
