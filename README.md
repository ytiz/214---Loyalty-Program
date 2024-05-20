# 214---Loyalty-Program
This repository if to manage the Loyalty Program created for FlyDreamAir

Develop Version 3.0 - Display Available Rewards

    
    let rewards = [
        Reward(name: "Free Coffee", pointsRequired: 100),
        Reward(name: "Discount Voucher", pointsRequired: 200),
        Reward(name: "Free Flight Upgrade", pointsRequired: 500)
    ]
    
    func redeemPoints(for reward: Reward) {
        if points >= reward.pointsRequired {
            points -= reward.pointsRequired
            message = "Successfully redeemed \(reward.name)!"
        } else {
            message = "Not enough points to redeem \(reward.name)."
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
            List(rewards) { reward in
                HStack {
                    Text(reward.name)
                    Spacer()
                    Text("\(reward.pointsRequired) points")
                    Button(action: {
                        redeemPoints(for: reward)
                    }) {
                        Text("Redeem")
                            .padding(5)
                            .background(Color.blue)
                            .foregroundColor(.white)
                            .cornerRadius(5)
                    }
                }
                .padding()
            }
            if let message = message {
                Text(message)
                    .foregroundColor(.green)
                    .padding()
            }
            Spacer()
        }
        .padding()
    }
