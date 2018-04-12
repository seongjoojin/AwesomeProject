# Handling Text Input

TextInput은 텍스트를 입력할 수 있는 기본 구성 요소.

onChangeText prop는 text가 변경될때마다 호출되게 되고 onSubmitEditing prop는 text를 submitted될 때 호출되게 됩니다.

    import React, { Component } from 'react';
    import { AppRegistry, Text, TextInput, View } from 'react-native';

    export default class PizzaTranslator extends Component {
    constructor(props) {
        super(props);
        this.state = {text: ''};
    }

    render() {
        return (
        <View style={{padding: 10}}>
            <TextInput
            style={{height: 40}}
            placeholder="Type here to translate!"
            onChangeText={(text) => this.setState({text})}
            />
            <Text style={{padding: 10, fontSize: 42}}>
            {this.state.text.split(' ').map((word) => word && '🍕').join(' ')}
            </Text>
        </View>
        );
    }
    }

    // skip this line if using Create React Native App
    AppRegistry.registerComponent('AwesomeProject', () => PizzaTranslator);

![Alt text](result01.png)

React docs on controlled components : https://reactjs.org/docs/forms.html#controlled-components

reference docs for TextInput : https://facebook.github.io/react-native/docs/textinput.html