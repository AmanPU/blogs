---
title: "How to Fix Baked Shadows in Unity?"
date: 2023-04-07T23:34:51-04:00
draft: false
---

These are the possible solutions that can help address issues with shadows in a Unity game. Here is a brief explanation of each:

- **Generate Lightmap UVs :** Unity needs to create a second set of UV coordinates to map light and shadow information onto the mesh. Make sure this is enabled in the Import Settings for all your models.
- **Mark gameobjects as static :** This allows Unity to bake lighting information into the scene, including shadow information. Dynamic objects won't cast shadows or receive them.
- **Use standard shader :** or If you are using a custom shader, make sure it supports lighting or that you have included lighting information in the shader code.
- **Set Metallic property to 0 :** This property affects the way the object reflects light and can cause issues with shadow rendering if not set correctly. For objects that do not reflect light, set this value to 0.
- **Use appropriate lightmap size :** The lightmap resolution needs to be high enough to capture the details of all the objects. If it's too low, the shadows will be blurred or lost.
- **Break up terrain/ground into smaller, equally-sized objects:** If your terrain or ground object is too large, the shadows may be averaged out, resulting in less detail and accuracy. By breaking it up into smaller, equally-sized objects, you can improve the accuracy of the lighting and shadow information.
- **Set Cast Shadows to off in Mesh Renderer component:** If you do decide to break up ground objects, make sure to turn off `Cast Shadows` in the `Mesh Renderer` component for each of the smaller objects. Otherwise, you may get strange shadow artifacts at the intersections of each object, which can look unnatural and distracting.
