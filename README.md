# 214---Loyalty-Program
This repository if to manage the Loyalty Program created for FlyDreamAir

Version 2.0 - Reward Redemption: Adding functionality to redeem points:
    
    func redeemPoints() {
        if points >= 100 {
            points -= 100
            message = "Successfully redeemed 100 points!"
        } else {
            message = "Not enough points to redeem."
        }
    }

    var body: some View {
        VStack {
            Text("Your Points")
                .font(.largeTitle)
                .padding()
            Text("\(points)")
                .font(.title)
                .padding()

            Button(action: redeemPoints) {
                Text("Redeem 100 Points")
                    .padding()
                    .background(Color.blue)
                    .foregroundColor(.white)
                    .cornerRadius(10)
            }
            .padding()
            if let message = message {
                Text(message)
                    .foregroundColor(.green)
                    .padding()
            }

            Spacer()
        }
        .padding()
    }

