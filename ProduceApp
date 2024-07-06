import React, {useState} from "react";
import {SafeAreaView, View, Text, StyleSheet, Button, Image} from 'react-native';
import {Picker} from '@react-native-picker/picker';

export default function App() {
  /* vegetables- setting the original values*/
  const [picker1SelectedValue, setPicker1SelectedValue] = useState("0"); 
  const [picker3selectedValue, setPicker3SelectedValue] = useState("1");
  /* fruit- setting the original values*/
  const [picker2selectedValue, setPicker2SelectedValue] = useState("0");
  const [picker4selectedValue, setPicker4SelectedValue] = useState("1");
  
  const [calculatedValue, setCalculatedValue] = useState("Press the above button to calculate the total cost");

  return (
  <SafeAreaView style={styles.container}>

    <View style ={styles.layer1}> 
      <Text style={styles.heading1}>
        Welcome to the Produce Owner Group 
      </Text> 
    </View> 
      <Image source={require('./assets/assessment3 photo.jpg')}
    style={{ width: 400, height: 150 }}
       />
       <Text style={styles.heading3}>
       Select Vegetables Below:
      </Text> 
 <View style={styles.layer2}> 
  <Picker
    style={styles.picker1}
    selectedValue={picker1SelectedValue}
    onValueChange={(itemValue) => setPicker1SelectedValue(itemValue)}
  > 
  <Picker.Item label="None Selected" value="0"/>
    <Picker.Item label="Carrots - $5" value="carrot- 5"/>
    <Picker.Item label="Beans - $8" value="beans- 8"/>
    <Picker.Item label="Corn - $6" value="corn- 6"/>
    <Picker.Item label="Lettuce - $9" value="lettuce- 9"/>
    <Picker.Item label="Tomato - $6" value="Tomato- 6"/>
   
  </Picker>
  <Picker
    style={styles.picker3}
    selectedValue={picker3selectedValue}
    onValueChange={(itemValue) => setPicker3SelectedValue(itemValue)}
  >
    <Picker.Item label="1" value="1"/>
    <Picker.Item label="2" value="2"/>
    <Picker.Item label="3" value="3"/>
    <Picker.Item label="4" value="4"/>
    <Picker.Item label="5" value="5"/>
  </Picker>
</View>
    <Text style={styles.heading3}>
       Select Fruit Below:
      </Text> 

<View style={styles.layer2}> 

  <Picker
    style={styles.picker2}
    selectedValue={picker2selectedValue}
    onValueChange={(itemValue) => setPicker2SelectedValue(itemValue)}
  >
    <Picker.Item label="None Selected" value="00"/>
    <Picker.Item label="Apples - $10" value="apple- 10"/>
    <Picker.Item label="Mango - $13" value="mango- 13"/>
    <Picker.Item label="Raspberry - $12" value="raspberry- 12"/>
    <Picker.Item label="Peach - $14" value="peach- 14"/>
    <Picker.Item label="Pear - $10" value="pear- 10"/>
  
  </Picker>
  <Picker
    style={styles.picker4}
    selectedValue={picker4selectedValue}
    onValueChange={(itemValue) => setPicker4SelectedValue(itemValue)}
  >
    <Picker.Item label="1" value="1"/>
    <Picker.Item label="2" value="2"/>
    <Picker.Item label="3" value="3"/>
    <Picker.Item label="4" value="4"/>
    <Picker.Item label="5" value="5"/>
  </Picker>
</View>

<View style={styles.layer3}> 
  <View style={styles.buttonContainer}>
        <Button 
          title="COST CALCULATOR"
          onPress={() => {
           // Get the last char off the veg cost and turn it into an int 
            const lastVegChar = picker1SelectedValue[picker1SelectedValue.length - 1]; 
            const IntVegCost = parseInt(lastVegChar);
            const intVegQuantity = parseInt(picker3selectedValue);

            // Get the last 2 char off the fruit cost and turn it into an int 
            const last2FruitChar = picker2selectedValue.slice(-2)
            const intFruitCost = parseInt(last2FruitChar);
            const intFruitQuantity = parseInt(picker4selectedValue);
       
            // Calculate the total cost
            const totalCost = (IntVegCost * intVegQuantity) + (intFruitCost * intFruitQuantity);
            // Update the variable with the calculated value and new words
            setCalculatedValue("The total cost is: $" + totalCost);       
          }}
            //dispaly the total cost
        />
        </View>
      <Text style={styles.heading2}> {calculatedValue} </Text> 


      <Text style={styles.appDevelopedBy}>App Developed By: Sienna, Emily,Tania,Tashiya,</Text>
    </View>
    </SafeAreaView>
  );

}

  const styles = StyleSheet.create({
    container: {
      flex: 1,
      backgroundColor: '#ZZZZZZ',
      padding:20,
    },
    layer1:{},
    heading1:{ 
      fontSize: 30, 
      textAlign: 'center', 
      marginTop: 20, 
    }, 
    layer2:{ 
      flexDirection:'row', 
      padding:'500' ,
      flex: 10, 
    }, 
    picker1: { 
      flex: 4, 
      marginVertical: -60,
      
    }, 
    picker2:{ 
      flex: 4, 
      marginVertical: -60,

    }, 
    picker3: { 
      flex: 2, 
      marginVertical: -60,
      
    },
    picker4: { 
      flex: 2, 
      marginVertical: -60,
    },
    
    heading2:{ 
      textAlign: 'center',
      colour: '#67e487',
      fontSize: 19,
      fontWeight: 10,
      marginTop: 5,
    },
      heading3:{ 
      fontSize: 20, 
      textAlign: 'center', 
      marginTop: 4, 
    }, 
    appDevelopedBy:{ 
      textAlign: 'center',
      marginTop: 10,
      fontSize: 15,
      color: '#800080', // Purple color
      
    },
    buttonContainer: {
        marginVertical: 5,
       borderWidth: 1,
       borderColor: 'black',
       padding: 10,
       borderRadius: 10,
       backgroundColor: '#f0f0f0',
  },
    
  });
