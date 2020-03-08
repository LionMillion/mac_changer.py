#!/ust/bin/evn python
import subprocess
import optparse
import re


def get_arguments():
    parser = optparse.OptionParser()
    parser.add_option("-i", "--interface", dest="interface", help="Interface to change its mac address")
    parser.add_option("-m", "--Mac", dest="new_mac", help="New Mac Address")
    (options, arguments) = parser.parse_args()
    if not options.interface:
        parser.error("[-] Please specity an interface, use --help for more info")
    elif not options.new_mac:
        parser.error("[-] Please specity an mac address, use --help for more info")
    return options


def change_mac(interface, new_mac):
    print("[+] Changing Mac address for " + interface + " to " + new_mac)
    subprocess.call(["ifconfig", interface, "down"])
    subprocess.call(["ifconfig", interface, "hw", "ether", new_mac])
    subprocess.call(["ifconfig", interface, "up"])

def get_current_mac(interface):
    ifconfig_r = subprocess.check_output(["ifconfig", interface])
    mac_address_search_result = re.search(r"\w\w:\w\w:\w\w:\w\w:\w\w:\w\w", ifconfig_r)
    if mac_address_search_result:
        return (mac_address_search_result.group(0))
    else:
        print("[-] Could not read MAC address.")

options = get_arguments()

current_mac = get_current_mac(options.interface)
print("Current Mac = " + str(current_mac))

change_mac(options.interface, options.new_mac)

current_mac = get_current_mac(options.interface)
if current_mac == options.new_mac:
    print("[+] Mac Address was successfully changed to " + current_mac)
else:
    print("[-] Mac address did not get changed. ")
