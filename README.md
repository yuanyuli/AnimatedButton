# Button

Button 是一个可以动态改变图片和文本样式的纯JavaScript编写的控件,支持安卓和iOS. 用户可以通过传入属性,自定义ActiveStyle和要显示的动画效果,同时对于图片可以即时响应Source的变化.

## Demo

![Demo](./gif/Demo.gif)

## Installation

`npm install react-native-animated-button -save`

## Documentaion

### Usage
```javascript	
import Button from 'react-native-animated-button';
	
class Demo extends Component {
	render() {
    	return (
        <Button/>
    	)	
      }
 }
 
```
### Examples
```
<Button
            style={{marginTop:10,alignSelf:'center', height: 55,width:80, backgroundColor: 'white', borderWidth: 1 / PixelRatio.get(), borderColor: '#0033FF', borderRadius: 5}}
            imageStyle={{height:50,width:50}}
            activeStyle={{marginTop:10,alignSelf:'center',height: 55,width:100, backgroundColor: 'white', borderWidth: 1 / PixelRatio.get(), borderColor: '#0033FF', borderRadius: 5}}
            source={require('./jpg/head.jpg')}
            text="左⬅️️"
            animated={true}
            type="iconLeft"
            onLongPress={() => {
          console.log('onLongPress...');
        }}
            onPress={() => {
          console.log('onPress...');
        }}
            onPressIn={() => {
          console.log('onPressIn...');
        }}
            onPressOut={() => {
          console.log('onPressOut...');
        }}
          >
```
## Props
- `animated` (Boolean) `false` - animated or not for Button
- `animations` (Object) animations for the style of Button from unactive to active 
- `onPressIn`(Function) callback when pressin
- `onPressOut`(Function) callback when pressout
- `type` (Oneof:(['iconLeft', 'iconRight', 'iconTop', 'iconBottom'])) `iconBottom` - the relative position for Image and Text
- `style` (OneOf([Number,Object]))  - style of the Button which is unactive 
- `activeStyle` (OneOf([Number,Object]))  - style of the Text which is active 
- `text` (String)  - text in Button
- `activeText` (String)  - text when Button is active
- `fontStyle` (OneOf([Number,Object]))  - style of the Text which is unactive 
- `activeFontStyle` (OneOf([Number,Object]))  - style of the Text which is active 
- `source` (OneOf([Number,Shape])) - source of Image which is unactive 
- `activeSource` (OneOf([Number,Shape])) - source of Image which is active 
- `imageStyle` (OneOf([Number,Object]))  - style of the Image which is unactive 
- `activeImageStyle` (OneOf([Number,Object]))  - style of the Image which is unactive 



