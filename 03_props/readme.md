# Props

    import React, { Component } from 'react';
    import { AppRegistry, Image } from 'react-native';

    export default class Bananas extends Component {
    render() {
        let pic = {
        uri: 'https://upload.wikimedia.org/wikipedia/commons/d/de/Bananavarieties.jpg'
        };
        return (
        <Image source={pic} style={{width: 193, height: 110}}/>
        );
    }
    }

    // skip this line if using Create React Native App
    AppRegistry.registerComponent('AwesomeProject', () => Bananas);

Most components can be customized when they are created, with different parameters. These creation parameters are called props.

예를 들면, component는 'Image'이고 image를 만들 때 사용하는 prop 이름은 'source'

만약 single component를 앱 여러 곳에 쓰고 싶다면 아래 예 같이쓰면 됨.

    import React, { Component } from 'react';
    import { AppRegistry, Text, View } from 'react-native';

    class Greeting extends Component {
    render() {
        return (
        <Text>Hello {this.props.name}!</Text>
        );
    }
    }

    export default class LotsOfGreetings extends Component {
    render() {
        return (
        <View style={{alignItems: 'center'}}>
            <Greeting name='Rexxar' />
            <Greeting name='Jaina' />
            <Greeting name='Valeera' />
        </View>
        );
    }
    }

    // skip this line if using Create React Native App
    AppRegistry.registerComponent('AwesomeProject', () => LotsOfGreetings);

render function안에 this.props를 써주면 되는것을 보실 수 있습니다.

props와 basic Text, Image 그리고 View component로 다양한 정적화면을 구성할 수 있습니다.

Text : https://facebook.github.io/react-native/docs/text.html <br>
Image : https://facebook.github.io/react-native/docs/image.html <br>
View : https://facebook.github.io/react-native/docs/view.html


