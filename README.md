# 214---Loyalty-Program
This repository if to manage the Loyalty Program created for FlyDreamAir
Code for the app to manage Loaylty Points: 
Develop Version 1.0 - Basic Points Display: 

import SwiftUI
struct ContentView: View {
    @State private var points: Int = 1000
    
    var body: some View {
        VStack {
            Text("Your Points")
                .font(.largeTitle)
                .padding()
            Text("\(points)")
                .font(.title)
                .padding()
            Spacer()
        }
        .padding()
    }
}

struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}

