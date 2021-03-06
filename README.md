# Open Source at Aquatic Informatics

![Logo](https://github.com/AquaticInformatics/aquarius-sdk-net/raw/develop/images/aquatic-informatics.png)

Welcome to the Aquatic Informatics open source offerings on GitHub. Hopefully this guide can get you pointed in the right direction.

# Are you a customer, just looking for some files?

You may have been directed here, and are just looking to download some prepackaged tool or extension for an AQUARIUS product you own. The GitHub web pages are very programmer-centric, and it can be a bit hard to navigate and find the specific files you need.

| AQUARIUS Product | Download link | Documentation | Description |
| --- | --- | --- | --- |
| AQUARIUS Time-Series 2018.2 | [2018.2 Report plugins](https://github.com/AquaticInformatics/getting-started/releases/download/v2018.2-aqts/2018.2.Reports.zip) | [Operation](https://github.com/AquaticInformatics/getting-started/releases/download/v2018.2-aqts/Report.Documentation.-.2018.2.Beta.Release.pdf) and [Installation](https://github.com/AquaticInformatics/getting-started/releases/download/v2018.2-aqts/ReportPluginInstaller.Readme.pdf) | This ZIP archive contains 7 report plugins and a report plugin installer, to add more reporting features to AQTS 2018.2. |
| AQUARIUS Time-Series 3.x and 201x | [Sample field data files](https://github.com/AquaticInformatics/examples/tree/master/TimeSeries/SampleFiles/FieldData) | [Here](https://github.com/AquaticInformatics/examples/tree/master/TimeSeries/SampleFiles/FieldData/Readme.md)| This page lists a description of each field data file formats supported by AQUARIUS Time-Series. A sample of each file type is provided for download. |
| AQUARIUS Time-Series 3.x | [FlowTracker2Converter.exe](https://github.com/AquaticInformatics/flowtracker2-field-data-plugin/releases/download/v17.4.30/FlowTracker2Converter.exe) | [Here](https://github.com/AquaticInformatics/flowtracker2-field-data-plugin/blob/master/src/FlowTracker2Converter/Readme.md)| Use this GUI tool to convert FlowTracker2 `*.ft` files into FlowTracker1 `*.dis` files which can be imported into your AQTS 3.X system. |
| AQUARIUS Time-Series 201x | [FieldDataPluginTool.exe](https://github.com/AquaticInformatics/aquarius-field-data-framework/releases/download/v18.2.0/FieldDataPluginTool.exe) | [Here](https://github.com/AquaticInformatics/aquarius-field-data-framework/blob/master/src/FieldDataPluginTool/Readme.md)| You'll need to download and use this GUI tool to install a field data plugins like FlowTracker2. |
| AQUARIUS Time-Series 201x | [FlowTracker2Plugin.plugin](https://github.com/AquaticInformatics/flowtracker2-field-data-plugin/releases/download/v17.4.30/FlowTracker2Plugin.plugin) | [Here](https://github.com/AquaticInformatics/flowtracker2-field-data-plugin/blob/master/README.md)| A field data plugin to import FlowTracker2 `*.ft` discharge measurements. |
| AQUARIUS Time-Series 201x | [StageDischargeReadings.plugin](https://github.com/AquaticInformatics/stage-discharge-readings-field-data-plugin/releases/download/v1.0.17/StageDischargeReadings.plugin) | [Here](https://github.com/AquaticInformatics/stage-discharge-readings-field-data-plugin/blob/master/src/StageDischargeReadings/Readme.md)| A field data plugin to import stage/discharge measurements and parameter readings into new visits. This plugin can replace the stock Stage/Discharge plugin. |
| AQUARIUS Time-Series 201x | [UserImporter.exe](https://github.com/AquaticInformatics/examples/releases/download/v1.0.22/UserImporter.exe) | [Here](https://github.com/AquaticInformatics/examples/tree/master/TimeSeries/PublicApis/SdkExamples#userimporter)| A console tool for quickly provisioning users in your AQTS system from a CSV file. |
| AQUARIUS Time-Series 201x | [PointZilla.exe](https://github.com/AquaticInformatics/examples/releases/download/v1.0.22/PointZilla.exe) | [Here](https://github.com/AquaticInformatics/examples/blob/master/TimeSeries/PublicApis/SdkExamples/PointZilla/Readme.md)| A console tool for quickly appending points to a time-series. |
| AQUARIUS Time-Series 201x | [TimeSeriesChangeMonitor.exe](https://github.com/AquaticInformatics/examples/releases/download/v1.0.22/TimeSeriesChangeMonitor.exe) | [Here](https://github.com/AquaticInformatics/examples/blob/master/TimeSeries/PublicApis/SdkExamples/TimeSeriesChangeMonitor/Readme.md)| A console tool for monitoring how quickly changes in a time-series become available on the Publish API. Use it along side PointZilla to precisely measure the behaviour of your data flow. |
| AQUARIUS Time-Series 201x | [LocationDeleter.exe](https://github.com/AquaticInformatics/examples/releases/download/v1.0.22/LocationDeleter.exe) | [Here](https://github.com/AquaticInformatics/examples/blob/master/TimeSeries/PublicApis/SdkExamples/LocationDeleter/Readme.md)| A console tool for deleting locations and/or visits and/or time-series during initial system configuration. You obviously won't want to run this on a production system. |

# Are you a developer, looking for code?

We have many software projects that allow you to easily extend or integrate with your AQUARIUS products.

Some are full software projects, with contiuous integration and unit tests, deployed via standard package distribution networks like NuGet or the Maven Central Repository.

Other projects are smaller proof-of-concept examples, which can be a useful starting point or inspiration for you own integrations.

### Platform SDKs

We have two SDK offerings, one for .NET and one for Java. These SDKs provide complete support for all the AQUARIUS products with public APIs (currently AQUARIUS Time-Series and AQUARIUS Samples, but more products will be added soon to these SDKs).

https://github.com/AquaticInformatics/aquarius-sdk-net - The .NET Platform SDK, available via [NuGet](https://www.nuget.org/packages/Aquarius.SDK).
https://github.com/AquaticInformatics/aquarius-sdk-java - The Java Platform SDK, available via the [Maven Central Repository](https://search.maven.org/#artifactdetails%7Ccom.aquaticinformatics%7Caquarius.sdk%7C18.5.1%7Cjar).

The functionality within each SDK is equivalent, handling the fussy parts of consuming REST APIs robustly:
- Authentication
- Session management
- JSON serialization
- Error handling
- File upload events
- Version checking

With these fussy parts handled for you, your integration code can more succicntly focus on consuming the documented public APIs. Using one of the SDKs greatly improves your team's productivity when writing large integrations.

### Which SDK should I choose? .NET or Java?

If you can choose your integration environment, we recommend using the .NET SDK over the Java SDK, simply because the .NET SDK is integrated into a number of AQUARIUS add-on products like AQUARIUS WebPortal, AQUARIUS DAS, AQUARIUS EnviroSCADA, and AQUARIUS Forecast. Since we use the .NET SDK internally for our own products, any issues tend to be noticed and resolved very quickly.

That said, the Java SDK is a fine choice if you prefer to work in Java, and we welcome any suggestions or contributions from the community to improve either SDK.

## Other open-source projects we host
| Project | Description |
| --- | --- |
| https://github.com/AquaticInformatics/aquarius-field-data-framework | A field data plugin development framework, so you can write custom plugins to consume your organization's unique field data. The framework is available on [NuGet](https://www.nuget.org/packages/Aquarius.FieldDataFramework) and includes testing and packaging tools. |
| https://github.com/AquaticInformatics/flowtracker2-field-data-plugin | A plugin for parsing SonTek's FlowTracker2 `*.ft` files. |
| [Python integration](https://github.com/AquaticInformatics/examples/tree/master/TimeSeries/PublicApis/Python) | A sample API wrapper for AQUARIUS Time-Series. |
| [R integration](https://github.com/AquaticInformatics/examples/tree/master/TimeSeries/PublicApis/R) | A fairly rich API wrapper for consuming time-series data in R. |
| https://github.com/AquaticInformatics/examples | Many examples, in many technologies. |


# What level of support can I expect?
Aquatic Informatics hosts some open source software projects on GitHub at https://github.com/AquaticInformatics. These projects can provide sample code, freely-downloadable tools, and/or extensions compatible with AQUARIUS products.

You can use them at your own risk, according to each project's open source license terms, which are clearly disclosed on the home page of each open source repository. These offerings are not part of the official released packages and therefore are not supported under the regular Service and Maintenance Agreement.

Our Support Team tries their best to help you but if you have questions/issues, it is recommended that you raise an issue on the project's Issues page. Our GitHub projects are managed by our Applications Engineering Team and they will get back to you.

# Code of Conduct

Each open source repository is governed by a code of conduct, derived from the from the [Contributor Covenant][homepage], version 1.4, available at [http://contributor-covenant.org/version/1/4][version].

The basic summary is "don't be a jerk" and everything should be fine.

[homepage]: http://contributor-covenant.org
[version]: http://contributor-covenant.org/version/1/4/

