# State

state는 변경 될 데이터인 경우에 사용하게 됩니다.

    import React, { Component } from 'react';
    import { AppRegistry, Text, View } from 'react-native';

    class Blink extends Component {
    constructor(props) {
        super(props);
        this.state = {isShowingText: true};

        // Toggle the state every second
        setInterval(() => {
        this.setState(previousState => {
            return { isShowingText: !previousState.isShowingText };
        });
        }, 1000);
    }

    render() {
        let display = this.state.isShowingText ? this.props.text : ' ';
        return (
        <Text>{display}</Text>
        );
    }
    }

    export default class BlinkApp extends Component {
    render() {
        return (
        <View>
            <Blink text='I love to blink' />
            <Blink text='Yes blinking is so great' />
            <Blink text='Why did they ever take this out of HTML' />
            <Blink text='Look at me look at me look at me' />
        </View>
        );
    }
    }

    // skip this line if using Create React Native App
    AppRegistry.registerComponent('AwesomeProject', () => BlinkApp);

위의 예제에서는 text 자체는 prop에 해당하며, 1초마다 on/off 반복하는 것을 state라고 할 수 있습니다.

실제 어플리케이션에서는 사용자의 입력이나 서버로부터 새로운 데이터를 받았을때를 고려해서 state를 만들어야합니다.

Redux와 같은 state container를 사용하여 data flow를 제어할 수 있습니다.