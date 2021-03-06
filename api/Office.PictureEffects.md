---
title: PictureEffects object (Office)
ms.prod: office
api_name:
- Office.PictureEffects
ms.assetid: bc0e1cfd-7328-360d-872e-c71ae93162ed
ms.date: 06/08/2017
localization_priority: Normal
---


# PictureEffects object (Office)

Represents a collection of  **PictureEffects** objects.


## Remarks

Picture Effects are processed as a chain composed of individual items which are applied in sequence to create the final composited image. An Effects chain will allow an effect to be added to the chain, reordered, or removed from the chain.


## Example

The following code sets several Picture Effect fill properties on a shape in a Microsoft PowerPoint slide.


```vb
Sub PictureEffectSample() 
' Setup a slide with one picture shape. 
With ActivePresentation.Slides(1).Shapes(1).Fill.PictureEffects 
 
 ' Insert a 150% Saturation effect. 
 .Insert(msoEffectSaturation).EffectParameters(1).Value = 1.5 
 
 ' Insert Brightness/Contrast effect and set values to -50% Brightness and +25% Contrast. 
 Dim brightnessContrast As PictureEffect 
 Set brightnessContrast = .Insert(msoEffectBrightnessContrast) 
 brightnessContrast.EffectParameters(1).Value = -0.5 
 brightnessContrast.EffectParameters(2).Value = 0.25 
 
 ' Remove all Picture effects. 
 While .Count > 0 
 .Delete (1) 
 Wend 
 
End With 
End Sub 

```


## See also


[Object Model Reference](./overview/Library-Reference/reference-object-library-reference-for-office.md)


[PictureEffects Object Members](./overview/Library-Reference/pictureeffects-members-office.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]