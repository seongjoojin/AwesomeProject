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