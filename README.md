# STKitSwift

<p align="center">
<img src="Resources/Banner.png" alt="STKitSwift Banner">
</p>

[![Platform](https://img.shields.io/cocoapods/p/STKitSwift.svg?style=flat)](https://github.com/STShenZhaoliang/STKitSwift)
![Version](https://img.shields.io/cocoapods/v/STKitSwift.svg?style=flat)
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)
[![Language](https://img.shields.io/badge/language-Swift%205.0-orange.svg)](https://swift.org/)
[![License](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://github.com/STShenZhaoliang/STKitSwift/blob/master/LICENSE)


STKitSwift is a collection of useful classes, structs and extensions to **develop Apps faster**.

Installing and Usage
====================

```ruby

    platform :ios, '12.0'
    xcodeproj 'Project.xcodeproj'
    use_frameworks!
    pod 'STKitSwift'
    
```

Effect Picture
====================
<img src="Resources/STAlertView01.png" width="25%" height="25%"><img src="Resources/STAlertView02.png" width="25%" height="25%"><img src="Resources/STGradientButton01.png" width="25%" height="25%"><img src="Resources/STGradientView01.png" width="25%" height="25%"><img src="Resources/STHUD01.png" width="25%" height="25%"><img src="Resources/STHUD02.png" width="25%" height="25%"><img src="Resources/STMoveButton01.png" width="25%" height="25%"><img src="Resources/STPhoneTextField01.png" width="25%" height="25%"><img src="Resources/STProgressView01.png" width="25%" height="25%"><img src="Resources/STSegmentedControl01.png" width="25%" height="25%">


## 1.STAlertView

### Installing

```ruby
pod 'STKitSwift/STAlertView'
```

### Example

```swift
let title = "Flutter 与 iOS 原生 WebView 对比"
STAlertView.show(title: title, message: nil, cancelTitle: "取消", otherTitle: "确定") { (item) in
    print(item)
}
```

## 2.STGradientButton

### Installing

``` ruby
pod 'STKitSwift/STGradientButton'
```

### Example

```swift
    private lazy var gradientButton: STGradientButton = {
        let gradientButton = STGradientButton()
        gradientButton.startColor = UIColor.init(red: 255.0/255, green: 76.0/255, blue: 21.0/255, alpha: 1)
        gradientButton.endColor =  UIColor.init(red: 255.0/255, green: 156.0/255, blue: 121.0/255, alpha: 1)
        gradientButton.setTitle("使用layer", for: .normal)
        gradientButton.layer.cornerRadius = 22
        gradientButton.layer.masksToBounds = true
        view.addSubview(gradientButton)
        return gradientButton
    }()
```

## 3.STGradientView

### Installing and Usage

```
pod 'STKitSwift/STGradientView'
```

## 4.STHUD

### Installing and Usage

```
pod 'STKitSwift/STHUD'
```

### Example

```swift
STHUD.show("Hello World")
```

## 5.STMoveButton

### Installing and Usage

```
pod 'STKitSwift/STMoveButton'
```

### Example

```swift
private lazy var moveButton: STMoveButton = {
    let moveButton = STMoveButton()
    moveButton.setImage(UIImage.init(named: "icon_wheel"), for: .normal)
    view.addSubview(moveButton)
    return moveButton
    }()
```

## 6.STPhoneTextField

### Installing and Usage

```
pod 'STKitSwift/STPhoneTextField'
```

### Example

```swift
let tf3 = STPhoneTextField()
tf3.config.defaultConfig = STPhoneFormat.init(defaultPhoneFormat: "(####) #######")
tf3.prefix = "+86 "
tf3.placeholder = "format:+86 (####) #######"
```

## 7.STProgressView

### Installing and Usage

```
pod 'STKitSwift/STProgressView'
```

## 8.STSegmentedControl

### Installing and Usage

```
pod 'STKitSwift/STSegmentedControl'

```

### Example

```swift
let titles = ["关注", "推荐", "国际", "娱乐", "视频", "科技", "军事", "设计", "体育", "读书"]
let segmentedControl = STSegmentedControl()
segmentedControl.titles = titles
segmentedControl.selectBlock = { (item) in
            print(item)
        }
segmentedControl.currentIndex = 3
```
