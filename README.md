# swiftPolymorphism

```swift
import UIKit

class Album {
    var name: String
    
    init(name: String) {
        self.name = name
    }
    func getPerformance() -> String {
        return name
    }
}

class StudioAlbum: Album {
    var studio: String
    
    init(name: String, studio:String) {
        self.studio = studio
        super.init(name: name)
    }
    override func getPerformance() -> String {
        return name
    }
}

class LiveAlbum: Album {
    var location: String
    
    init(name: String, location: String) {
        self.location = location
        super.init(name: name)
    }
    override func getPerformance() -> String {
        return name
    }
}

var barryGibb = StudioAlbum(name: "Barry Gibb", studio: "Star Studios")
var andyGibb = StudioAlbum(name: "Andy Gibb", studio: "The Castle Studio")
var iTunesLive = LiveAlbum(name: "iTunes Live from Harlow", location: "London")

var allAlbums: [Album] = [barryGibb,andyGibb,iTunesLive]

for album in allAlbums {
    print(album.getPerformance())
}
```
