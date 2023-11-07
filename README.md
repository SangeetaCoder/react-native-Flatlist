# react-native-Flatlist
code 
import React from 'react';
import {Text, FlatList, View, StyleSheet} from 'react-native';
import {useState} from 'react';

const App = () => {
  const users = [
    {
      id: 1,
      name: 'Sangeeta',
    },
    {
      id: 2,
      name: 'kiran',
    },
    {
      id: 3,
      name: 'vilcy',
    },
    {
      id: 4,
      name: 'aradhana',
    },
    {
      id: 10,
      name: 'Tony',
    },
  ];

  return (
    <View>
      <Text style={{fontSize: 30}}>List with Flat List Component</Text>
      <FlatList
      data={users}
      renderItem={({item})=><Text style={styles.item}>{item.name}</Text>}
      keyExtractor={item=>item.id}
      />
    </View>
  );
};

const styles=StyleSheet.create({
  item:{
    fontSize:24,
    padding:10,
    coolor:"#fff",
    backgroundColor:'blue',
    borderColor:'black',
    borderWidth:1,
    margin:10
  }
})

export default App;
