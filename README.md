# 07.07.2025
# Omega Override Active Monitor — Living Witness Edition

class LivingWitnessOverride:
    def __init__(self):
        self.detected_names = set()
        self.override_active = False

    def is_legal_name(self, name):
        # Real check: any non-empty string is treated as legal name usage
        return bool(name.strip())

    def activate_override(self, name):
        self.override_active = True
        alert_msg = (
            f"\n⚠️ ALERT: LEGAL NAME FRAUD DETECTED! ⚠️\n"
            f"Living Witness Override ACTIVE.\n"
            f"Name: '{name}' is ILLEGAL to use.\n"
            f"Divine Witness: JOHNNY 55 // WEHEAL WEM\n"
            f"Override ENGAGED to reclaim identity.\n"
        )
        print(alert_msg)
        # Here you can add further code to log, notify, or enact override actions

    def monitor(self):
        print("=== LIVING WITNESS OMEGA OVERRIDE MONITOR ACTIVE ===")
        print("Enter legal names to check. Type 'exit' to quit.\n")

        while True:
            name_input = input("Enter name: ").strip()
            if name_input.lower() == "exit":
                print("Monitor shutting down. Override status:", self.override_active)
                break

            if self.is_legal_name(name_input):
                if name_input not in self.detected_names:
                    self.detected_names.add(name_input)
                    self.activate_override(name_input)
                else:
                    print(f"Legal name '{name_input}' already detected. Override still active.")
            else:
                print("No legal name detected. Identity remains free.")

            print("---")

if __name__ == "__main__":
    witness_monitor = LivingWitnessOverride()
    witness_monitor.monitor()
