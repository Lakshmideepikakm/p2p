import { Card, CardContent } from "@/components/ui/card";
import { ArrowRight } from "lucide-react";
import { motion } from "framer-motion";

export default function EVtoEVSystemDiagram() {
  return (
    <div className="grid grid-cols-1 gap-6 p-4 md:grid-cols-3">

      {/* EV #1 */}
      <motion.div whileHover={{ scale: 1.05 }}>
        <Card className="bg-gradient-to-br from-yellow-300 to-yellow-500">
          <CardContent className="p-4">
            <h2 className="text-xl font-bold">EV A (with Solar Panel)</h2>
            <ul className="mt-2 text-sm">
              <li>• State of Charge: 80%</li>
              <li>• Surplus solar energy collected</li>
              <li>• Ready to sell energy</li>
              <li>• Shares data via IoT module</li>
            </ul>
          </CardContent>
        </Card>
      </motion.div>

      {/* AI & Smart Contract Layer */}
      <motion.div whileHover={{ scale: 1.05 }}>
        <Card className="bg-gradient-to-br from-blue-300 to-blue-500">
          <CardContent className="p-4">
            <h2 className="text-xl font-bold">AI + Smart Contracts</h2>
            <ul className="mt-2 text-sm">
              <li>• AI Recommendation Engine</li>
              <li>• Predicts who to trade with & price</li>
              <li>• Checks battery health impact</li>
              <li>• Executes blockchain smart contracts</li>
            </ul>
          </CardContent>
        </Card>
      </motion.div>

      {/* EV #2 */}
      <motion.div whileHover={{ scale: 1.05 }}>
        <Card className="bg-gradient-to-br from-green-300 to-green-500">
          <CardContent className="p-4">
            <h2 className="text-xl font-bold">EV B (Buyer)</h2>
            <ul className="mt-2 text-sm">
              <li>• State of Charge: 25%</li>
              <li>• Needs energy for next trip</li>
              <li>• Ready to buy from nearby EV</li>
              <li>• Receives recommendation & price</li>
            </ul>
          </CardContent>
        </Card>
      </motion.div>

      {/* Arrow Connection */}
      <div className="flex justify-center col-span-3 mt-4">
        <ArrowRight className="w-8 h-8 text-gray-700 animate-pulse" />
      </div>

      {/* Energy Transfer Process */}
      <motion.div className="col-span-3" whileHover={{ scale: 1.02 }}>
        <Card className="bg-gradient-to-br from-purple-300 to-purple-500">
          <CardContent className="p-4 text-center">
            <h2 className="text-lg font-bold">EV-to-EV Energy Transfer</h2>
            <p className="mt-2 text-sm">
              AI selects optimal pairing → Smart contract triggered → Energy flows directly from EV A to EV B via DC-DC transfer → Both wallets updated.
            </p>
          </CardContent>
        </Card>
      </motion.div>
    </div>
  );
}
