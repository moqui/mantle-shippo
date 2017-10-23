# Mantle Shippo Integration

[![license](http://img.shields.io/badge/license-CC0%201.0%20Universal-blue.svg)](https://github.com/moqui/mantle-shippo/blob/master/LICENSE.md)
[![release](http://img.shields.io/github/release/moqui/mantle-shippo.svg)](https://github.com/moqui/mantle-shippo/releases)
[![commits since release](http://img.shields.io/github/commits-since/moqui/mantle-shippo/v1.0.0.svg)](https://github.com/moqui/mantle-shippo/commits/master)

Mantle USL integration with Shippo (goshippo.com) for address verification, shipping rates, labels, and tracking across a wide 
variety of carriers including UPS, FedEx, DHL, USPS, and many more.

To add this component to Moqui the easiest approach is to use the Gradle get component task:

    $ ./gradlew getComponent -Pcomponent=mantle-shippo

Or add a dependency in your component.xml file like:

    <depends-on name="mantle-shippo"/>

To use simply:

1. load the setup data in data/ShippoSetupData.xml
2. load the demo configuration data in data/ShippoZaaDemoData.xml or create your own configuration and load it; if you use the demo data, add your API token (SgoApiToken option)
3. configure the store shipping gateway with a ShippingGatewayConfig record (see the demo data file for an example)
4. test the gateway with some test orders/shipments, retrieving rates and labels

Note that PopCommerce and various screens in SimpleScreens have support for Shippo and other shipping plugins to mantle-usl. 
