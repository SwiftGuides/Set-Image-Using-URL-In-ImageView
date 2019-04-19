# Set-Image-Using-URL-In-ImageView
This is a extension to set image in imageView using URL

#### UIImageView Extension
```swift

extension UIImageView{
    
    func setImageFromURl(stringImageUrl url: String){
        
        if let url = NSURL(string: url) {
            if let data = NSData(contentsOf: url as URL) {
                self.image = UIImage(data: data as Data)
            }
        }
    }
}

```


### Call The Extension 

```swift
let myImageView:UIImageView!

let imageURL = "https://pintreset.co/images/2356/mountain.img"

myImageView.setImageFromURl(stringImageUrl: imageURL)

```
