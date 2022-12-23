 
import { View, Text } from "react-native";
import React from "react";
import { useNavigation } from "@react-navigation/native";
import { useLayoutEffect } from "react";

const Test = () => {
  const navigation = useNavigation();

  useLayoutEffect(() => {
    navigation.setOptions({
      headerShown: false,
    });
  });

  return (
    <View className="flex-1">
      <View className="bg-red-300 items-center justify-center flex-1">
        <Text>Test</Text>
      </View>
    </View>
  );
};

export default Test;




import { useNavigation } from "@react-navigation/native";

onPress={() => navigation.navigate("Scan QR")}
