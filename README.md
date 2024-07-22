# Avalanche-HyperSDK
The HyperSDK provides the ability to create a custom virtual machine, which offers complete control over a custom blockchain. With the HyperSDK, you can design a blockchain that perfectly suits your needs, such as creating and transferring tokens or implementing a traditional order book for asset trading. This level of customization provides a powerful tool for businesses and organizations seeking a tailored solution.

By using the HyperSDK, you have full control over the rules and functionality of your chain, allowing you to create a custom blockchain that is tailored to your startup's specific needs. This offers an unparalleled level of control and flexibility, making it a valuable tool for organizations seeking a custom solution.

This level of control allows your startup to create a unique solution that meets the needs of your users and provides a competitive edge in the market.

Since HyperSDK is alpha software, we are using the example token VM, this is one of the few that has been tested and is guarantee to be maintained in the upcoming future.

## Installing GO
Before we begin, you’ll need to install GO on your system. You can do so by clicking [this link](https://go.dev/doc/install) and following the installation instructions for your operating system.

## Project: Step By Step

1) Clone the initial repository
2) Inside your project folder, run go mod tidy to normalize all the dependencies
3) Configure your project constants
  a) Go to consts/consts.go and add the missing parts.
4) Register the Create_Asset and Mint_Assest actions in registry/registry.go
5) Run your VM locally
   a) Make sure Go is on your path, defined on your terminal, if not you can do so by running export PATH=$PATH:$(go env GOPATH)/bin
   
     i)  If this path doesn’t work, you can also try export PATH=$PATH:/usr/local/go/bin
   
   b) Run MODE="run-single" ./scripts/run.sh
   
   c) Run ./scripts/build.sh
   
     i) If you get a permissions denied error, try running these scripts with the bash command (i.e.bash ./scripts/run.sh)
   
   d) Load the demo private key included on the project ./build/token-cli key import demo.pk and ./build/token-cli chain import-anr
   
7) Interact with your own HyperChain!
   a) Use the demos included in the README file or located at the repo in step 1
   
9) To close your Local Avalanche Network run killall avalanche-network-runner
