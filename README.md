# SemanticImage

The collection of image filters.

# How to use

### Setting Up

1, Add SemanticImage to your project as Swift Package with Swift Package Manager. 
   Or just drag SemanticImage.swift to your project.

2, Import and initialize SemanticImage

```swift
import SemanticImage
```

```swift
let semanticImage = SemanticImage()
```

Requires iOS 15 or above

# Filter Collection

## Image

### Get Person Mask

<img width="300" src="https://user-images.githubusercontent.com/23278992/146860733-acf875a5-043c-4ebb-ab3c-f98e124f6a93.jpg"> <img width="300" src="https://user-images.githubusercontent.com/23278992/146860762-01faf109-019f-4644-9e02-65c04adc1b79.JPG">


```swift
let maskImage:UIImage? = semanticImage.personMaskImage(uiImage: yourUIImage)
```



### Swap the background of a person

<img width="300" src="https://user-images.githubusercontent.com/23278992/146860733-acf875a5-043c-4ebb-ab3c-f98e124f6a93.jpg"> <img width="300" src="https://user-images.githubusercontent.com/23278992/146862832-14c0f002-b4e7-43c6-92e4-8595e99e15fd.JPG">

```swift
let swappedImage:UIImage? = sematicImage.swapBackgroundOfPerson(personUIImage: yourUIImage, backgroundUIImage: yourBackgroundUIImage)
```

### Blur the backgrond of a person

<img width="300" src="https://user-images.githubusercontent.com/23278992/146860733-acf875a5-043c-4ebb-ab3c-f98e124f6a93.jpg"> <img width="300" src="https://user-images.githubusercontent.com/23278992/147166740-a762db75-142b-401c-a726-2a78d84c2496.JPG">

```swift
let blurredPersonImage:UIImage? = sematicImage.personBlur(uiImage:UIImage, intensity:Float)
// Blur intensity: 0~100 
```

### Crop a face rectangle

<img width="300" src="https://user-images.githubusercontent.com/23278992/146860733-acf875a5-043c-4ebb-ab3c-f98e124f6a93.jpg"> <img width="300" src="https://user-images.githubusercontent.com/23278992/147011663-326292e3-982b-4214-bbb5-ebb1ceb06e02.JPG">

```swift
let faceImage:UIImage? = sematicImage.faceRectangle(uiImage: image)
```

### Crop a body rectangle

<img width="300" src="https://user-images.githubusercontent.com/23278992/146860733-acf875a5-043c-4ebb-ab3c-f98e124f6a93.jpg"> <img width="300" src="https://user-images.githubusercontent.com/23278992/147012402-f3866730-4996-4036-b7c5-1358bad547b1.JPG">

```swift
let bodyImage:UIImage? = sematicImage.humanRectangle(uiImage: image)
```

### Crop face rectangles

<img width="300" src="https://user-images.githubusercontent.com/23278992/147014241-fca3ceb0-c042-4a64-96a5-ad54c3dde96e.JPEG"> <img width="100" src="https://user-images.githubusercontent.com/23278992/147014227-3a4aa167-3cd4-492f-a515-48ec7a7e2489.JPG"><img width="100" src="https://user-images.githubusercontent.com/23278992/147014232-559a7373-2288-4ee1-ac88-5b2cd7a9e65d.JPG"><img width="100" src="https://user-images.githubusercontent.com/23278992/147014233-819fd97a-138f-4de8-8c44-3f59742e68a0.JPG"><img width="100" src="https://user-images.githubusercontent.com/23278992/147014235-08347066-d97f-46aa-8810-9349f6481917.JPG"><img width="100" src="https://user-images.githubusercontent.com/23278992/147014237-8bb38476-3073-4dd7-9a72-b836e029dc9e.JPG"><img width="100" src="https://user-images.githubusercontent.com/23278992/147014238-8e9b5727-2821-4798-b66b-ae2fa8673c57.JPG">

```swift
let faceImages:[UIImage] = sematicImage.faceRectangles(uiImage: image)
```

### Crop body rectangles

<img width="300" src="https://user-images.githubusercontent.com/23278992/147015645-f8b5d6a1-95cb-4656-8b51-57b24b8e82a5.jpeg"> <img width="100" src="https://user-images.githubusercontent.com/23278992/147015635-52e77dc8-87b7-44f4-89ba-cbad4e7d94d4.JPG"><img width="100" src="https://user-images.githubusercontent.com/23278992/147015636-d36a4cfc-202f-4ea1-bd17-860180e1001a.JPG"><img width="100" src="https://user-images.githubusercontent.com/23278992/147015640-33d58d38-af34-4dc5-bb6a-f46994732d8a.JPG"><img width="100" src="https://user-images.githubusercontent.com/23278992/147015642-ada60f8d-7637-4823-b343-e5fb4dd4c275.JPG">

```swift
let bodyImages:[UIImage] = sematicImage.humanRectangles(uiImage: image)
```

### Crop an animal(Cat/Dog) rectangle

<img width="300" src="https://user-images.githubusercontent.com/23278992/147165331-d99b2fbe-b04e-4de9-a215-226da16ab232.jpeg"> <img width="300" src="https://user-images.githubusercontent.com/23278992/147165338-1056ce1a-86e7-441e-b782-517b1129e2a2.JPG">

```swift
let animalImage:UIImage? = sematicImage.animalRectangle(uiImage: image)
```

### Crop multiple animal(Cat/Dog) rectangles

<img width="300" src="https://user-images.githubusercontent.com/23278992/147165104-f3cace3c-ab5c-4e26-a28d-ac50e16eeb23.jpg"> <img width="100" src="https://user-images.githubusercontent.com/23278992/147165102-826e9262-0256-40c8-9fbb-4195ed1485e4.JPG"><img width="100" src="https://user-images.githubusercontent.com/23278992/147165100-4afe5856-e0e1-4c82-a725-8a149731e5a9.JPG"><img width="100" src="https://user-images.githubusercontent.com/23278992/147165097-0e7b946c-83bb-4f63-85df-3cf2036620a5.JPG"><img width="100" src="https://user-images.githubusercontent.com/23278992/147165096-3e0c901b-b973-4086-a86f-b6c96d741b33.JPG"><img width="100" src="https://user-images.githubusercontent.com/23278992/147165093-613875ed-107c-42eb-8ee4-376a01789523.JPG"><img width="100" src="https://user-images.githubusercontent.com/23278992/147165092-a5037cc7-14ff-436c-bb1a-b1fe79ece681.JPG"><img width="100" src="https://user-images.githubusercontent.com/23278992/147165088-3fd812f9-aab5-4ca3-8b68-9e631d334039.JPG">

```swift
let animalImages:[UIImage] = sematicImage.animalRectangles(uiImage: image)
```

## Video

### Apply CIFilter to Video

<img width="600" src="https://user-images.githubusercontent.com/23278992/147177254-06633831-7dcd-4b4f-be3c-fc97eadbceac.gif">

```swift
guard let ciFilter = CIFilter(name: "CIEdgeWork", parameters: [kCIInputRadiusKey:3.0]) else { return }
sematicImage.ciFilterVideo(videoURL: url, ciFilter, { err, processedURL in
    // Handle processedURL in here.
})
```
