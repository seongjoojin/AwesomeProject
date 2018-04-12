# style

    import React, { Component } from 'react';
    import { AppRegistry, StyleSheet, Text, View } from 'react-native';

    export default class LotsOfStyles extends Component {
    render() {
        return (
        <View>
            <Text style={styles.red}>just red</Text>
            <Text style={styles.bigblue}>just bigblue</Text>
            <Text style={[styles.bigblue, styles.red]}>bigblue, then red</Text>
            <Text style={[styles.red, styles.bigblue]}>red, then bigblue</Text>
        </View>
        );
    }
    }

    const styles = StyleSheet.create({
    bigblue: {
        color: 'blue',
        fontWeight: 'bold',
        fontSize: 30,
    },
    red: {
        color: 'red',
    },
    });

    // skip this line if using Create React Native App
    AppRegistry.registerComponent('AwesomeProject', () => LotsOfStyles);

![Alt text](result01.jpg)

기본적으로 지정하는 것은 css 문법과 비슷하지만 camel case를 사용하여 작성하게 됩니다. ( ex ) background-color -> backgroundColor )