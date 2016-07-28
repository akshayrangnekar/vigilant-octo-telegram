# Massaging Input Data

## Initial Data Format

The initial document provided by our data service provider was in an XML format. The data consisted of an collection of restaurants, each described in this format:

```
<xoi identifier="404290" millesime="2016" type="RESTAURANT" language="eng"> <main_information> <name> <label language="eng">Trading Post</label> </name> <local_name>Trading Post</local_name> <street>170 John St.</street> <postcode>10038</postcode> <address_complement>at South St.</address_complement> <city>New York</city> <main_city>Manhattan</main_city> <state>NY</state> <country>USA</country> <ref_lieu>1156381</ref_lieu> <ref_main>1670351</ref_main> <local_phone1>(646) 370-3337</local_phone1> <int_phone1>+1 646-370-3337</int_phone1> <e164_phone1>+16463703337</e164_phone1> <web>www.tradingpostnyc.com</web> <access mode="subway"> <description>Fulton St</description> </access> </main_information> <geoposition> <lat>40.70594</lat> <lon>-74.00417</lon> </geoposition> <added_values> <data name="michelin_stars" type="criterion"> <value>0</value> </data> <data name="bib_gourmand" type="criterion"> <value>0</value> </data> <data name="rating" type="field"> <value>13</value> </data> <data name="disabled_access" type="criterion"> <value>1</value> </data> <data name="brunch" type="criterion"> <value>0</value> </data> <data name="bring_your_own_bottle" type="criterion"> <value>0</value> </data> <data name="interesting_beer_list" type="criterion"> <value>1</value> </data> <data name="interesting_wine_list" type="criterion"> <value>0</value> </data> <data name="cash_only" type="criterion"> <value>0</value> </data> <data name="classification" type="criterion"> <value>3</value> </data> <data name="cocktail" type="criterion"> <value>0</value> </data> <data name="currency" type="field"> <value>USD</value> </data> <data name="dim_sum" type="criterion"> <value>0</value> </data> <data name="opening_times" type="field"> <value language="eng">Lunch &amp; dinner Mon - Sat</value> </data> <data name="pleasant" type="criterion"> <value>0</value> </data> <data name="michelin_guide_selection" type="criterion"> <value>1</value> </data> <data name="no_smoke" type="criterion"> <value>1</value> </data> <data name="facilities" type="field"> <value>\035 \622 \523</value> </data> <data name="price_class" type="criterion"> <value>5</value> </data> <data name="breakfast" type="criterion"> <value>0</value> </data> <data name="price_max_gm21" type="field"> <value>49.99</value> </data> <data name="price_min_gm21" type="field"> <value>25</value> </data> <data name="meal_price" type="field"> <value>$25 to $50</value> </data> <data name="meals_in_garden" type="criterion"> <value>0</value> </data> <data name="sake" type="criterion"> <value>0</value> </data> <data name="private_room" type="criterion"> <value>1</value> </data> <data name="main_desc" type="field"> <value language="eng">A reprieve from the neighborhood's many pubs and quick-serve joints, this popular restaurant occupies three floors of a historic building across from the Rockwell-designed Imagination Playground. Stylish and eclectic with a maritime theme, the massive space boasts a rollicking bar and whiskey cellar plus an upscale second floor with water views and an elegant library. The menu is just as wonderful and wide-ranging, with everything from flatbreads to skirt steak to lobster fried rice. Highlights include a healthy and delicious quinoa salad, studded with butternut squash, morsels of creamy feta, dried cranberries, and a drizzle of reduced balsamic vinegar. Jumbo shrimp plated with wilted kale, plump butter beans, and braised tomato is an impressive entrée.</value> </data> <data name="cooking_lib" type="multi"> <item> <value language="eng">American</value> </item> </data> <data name="cooking_id" type="multi"> <item> <value>40</value> </item> </data> <data name="restaurant_lib" type="multi"> <item> <value language="eng">restaurant</value> </item> </data> <data name="restaurant_id" type="multi"> <item> <value>1</value> </item> </data> <data name="valet" type="criterion"> <value>0</value> </data> <data name="facilities_details" type="complex"> <data name="disabled_access" type="criterion"> <value>1</value> </data> <data name="private_room" type="criterion"> <value>1</value> </data> </data> <data name="meals_details" type="complex"> <data name="brunch" type="criterion"> <value>0</value> </data> <data name="bring_your_own_bottle" type="criterion"> <value>0</value> </data> <data name="dim_sum" type="criterion"> <value>0</value> </data> <data name="breakfast" type="criterion"> <value>0</value> </data> <data name="sake" type="criterion"> <value>0</value> </data> <data name="cooking_lib" type="multi"> <item> <value language="eng">American</value> </item> </data> <data name="cooking_id" type="multi"> <item> <value>40</value> </item> </data> <data name="restaurant_lib" type="multi"> <item> <value language="eng">restaurant</value> </item> </data> <data name="restaurant_id" type="multi"> <item> <value>1</value> </item> </data> </data> <data name="selections_details" type="complex"> <data name="interesting_beer_list" type="criterion"> <value>1</value> </data> <data name="interesting_wine_list" type="criterion"> <value>0</value> </data> <data name="cocktail" type="criterion"> <value>0</value> </data> <data name="pleasant" type="criterion"> <value>0</value> </data> </data> <data name="credit_cards_details" type="complex"> <data name="cash_only" type="criterion"> <value>0</value> </data> </data> <data name="prices_details" type="complex"> <data name="currency" type="field"> <value>USD</value> </data> <data name="price_class" type="criterion"> <value>5</value> </data> <data name="price_max_gm21" type="field"> <value>49.99</value> </data> <data name="price_min_gm21" type="field"> <value>25</value> </data> </data> <data name="services_details" type="complex"> <data name="no_smoke" type="criterion"> <value>1</value> </data> <data name="meals_in_garden" type="criterion"> <value>0</value> </data> <data name="valet" type="criterion"> <value>0</value> </data> </data> <data name="desc_details" type="complex"> <data name="main_desc" type="field"> <value language="eng">A reprieve from the neighborhood's many pubs and quick-serve joints, this popular restaurant occupies three floors of a historic building across from the Rockwell-designed Imagination Playground. Stylish and eclectic with a maritime theme, the massive space boasts a rollicking bar and whiskey cellar plus an upscale second floor with water views and an elegant library. The menu is just as wonderful and wide-ranging, with everything from flatbreads to skirt steak to lobster fried rice. Highlights include a healthy and delicious quinoa salad, studded with butternut squash, morsels of creamy feta, dried cranberries, and a drizzle of reduced balsamic vinegar. Jumbo shrimp plated with wilted kale, plump butter beans, and braised tomato is an impressive entrée.</value> </data> </data> </added_values> <relationship> <media_relationship/> <xoi_relationship> <xoi identifier="NX70897" type="CITY" role="parent"/> </xoi_relationship> </relationship> </xoi>
```

## Conversion to JSON

XML is painful to manipulate, particularly compared to JSON when using NodeJS. As a first task we built a converter that takes the XML and converts it to JSON.

While there is the useful `xml2js` library, the output from that library is itself not optimal. The structure of the XML leads to repeated data, and the attribute vs content nature of XML leads to a complex JSON data structure. To simplify it down, we wrote a simple node.js script to convert to a flattened JSON format. 

```var fs = require('fs'),
    xml2js = require('xml2js');

var parser = new xml2js.Parser();
var jsonfile = require('jsonfile')

fs.readFile(__dirname + '/data.xml', function(err, data) {
    parser.parseString(data, function (err, result) {
        var restaurants  = result.mtpxoi.xoi;
        var newRests = [];

        for (var index in restaurants) {
            //console.log(`Restaurant ${index}`);
            var newRest = processMetadata(restaurants[index]);
            
            processMainInformation(newRest, restaurants[index]);
            processGeolocationField(newRest, restaurants[index]);
            processAddedValues(newRest, restaurants[index]);
            processRelationship(newRest, restaurants[index]);

            newRests.push(newRest);
        }

        writeOutput(newRests);
        writeRemainingInput(restaurants);
    });
});

function writeOutput(restaurants) {
    var file = 'output.json';

    jsonfile.writeFile(file, restaurants, {spaces: 2}, function(err) {
        if (err) console.error(err);
    })
}

function writeRemainingInput(restaurants) {
    var file = 'remaining-input.json';

    jsonfile.writeFile(file, restaurants, {spaces: 2}, function(err) {
        if (err) console.error(err);
    })
}

function processMetadata(origObj) {
    var newRest = {
        id: origObj["$"]["identifier"],
        year: origObj["$"]["millesime"],
        type: origObj["$"]["type"]
    };

    delete origObj["$"];
    return newRest;
};

function processMainInformation(obj, origObj) {
    obj.name = origObj["main_information"][0]["name"][0]["label"][0]["_"];
    delete origObj["main_information"][0]["name"];

    addMainInformationField(obj, origObj, "local_name", null, null, true);
    addMainInformationField(obj, origObj, "main_city", null, null, true);
    addMainInformationField(obj, origObj, "street", null, null, true);
    addMainInformationField(obj, origObj, "postcode", null, null, true);
    addMainInformationField(obj, origObj, "address_complement");
    addMainInformationField(obj, origObj, "city", null, null, true);
    addMainInformationField(obj, origObj, "state", null, null, true);
    addMainInformationField(obj, origObj, "country", null, null, true);
    addMainInformationField(obj, origObj, "ref_lieu", "ref_lieu", null, true);
    addMainInformationField(obj, origObj, "ref_main", "ref_main", null, true);
    addMainInformationField(obj, origObj, "local_phone1", "localPhone", null, true);
    addMainInformationField(obj, origObj, "e164_phone1", "globalPhone", null, false);
    addMainInformationField(obj, origObj, "web", "web", null, false);
    addAccessField(obj, origObj);
    ignoreMainInformationFields(origObj, ["int_phone1"]);
    delete origObj.main_information;

    //origObj.main_information = obj.name;
};

function addMainInformationField(obj, origObj, fieldName, newFieldName, defaultValue, required) {
    if (newFieldName == null) newFieldName = fieldName;
    if (origObj["main_information"][0][fieldName]) {
        obj[newFieldName] = origObj["main_information"][0][fieldName][0]
        delete origObj["main_information"][0][fieldName];
    } else {
        if (defaultValue) obj[newFieldName] = defaultValue;
        if (required) console.error('Missing ' + fieldName + ' for ' + obj.id + ' (' + obj.name + ' in ' + obj.main_city + ')');
    }
};

function ignoreMainInformationFields(origObj, fieldNames) {
    for (index in fieldNames) {
        var fieldName = fieldNames[index];
        delete origObj["main_information"][0][fieldName];
    }
};

function addAccessField(obj, origObj) {
    if (origObj["main_information"][0].access) {
        obj.access_mode = origObj["main_information"][0].access[0]["$"]["mode"];
        obj.access_description = origObj["main_information"][0].access[0]["description"][0];
        delete origObj["main_information"][0].access;
    } else {
        //console.log('Missing access for ' + obj.id + ' (' + obj.name + ' in ' + obj.main_city + ')')
    }
};

function processGeolocationField(obj, origObj) {
    var geo = origObj["geoposition"];
    if (geo) {
        obj.location_lat = geo[0]["lat"][0];
        obj.location_lon = geo[0]["lon"][0];
        delete origObj["geoposition"];
    } else {
        console.error('Missing location for ' + obj.id + ' (' + obj.name + ' in ' + obj.main_city + ')');
    }
};

function processAddedValues(obj, origObj) {
    var remaining = [];
    obj.attributes = [];
    for (var i = 0; i < origObj.added_values[0].data.length; i++) {
        if (!processAddedValue(obj, origObj.added_values[0].data[i])) {
            remaining.push(origObj.added_values[0].data[i]);
        }
    }

    if (remaining.length > 0) origObj.added_values = remaining;
    else delete origObj.added_values;
};

function processAddedValue(obj, addedValue) {
    var valueName = addedValue.$.name;
    var valueType = addedValue.$.type;
    if (testCoreAddedValue(obj, valueName, valueType, addedValue)) return true;
    if (testAttributeAddedValue(obj, valueName, valueType, addedValue)) return true;
    if (processCookingLib(obj, valueName, valueType, addedValue)) return true;
    if (processCookingId(obj, valueName, valueType, addedValue)) return true;
    if (testIgnoredAddedValue(valueName, addedValue)) return true;
    if (processDetailedLists(obj, valueName, valueType, addedValue)) return true;
    return false;
};

var CORE_ADDED_VALUE_CRITERION = ["michelin_stars", "bib_gourmand", "main_desc", "opening_times", "facilities", "currency", "rating", "classification", "michelin_guide_selection", "price_class", "price_max_gm21", "price_min_gm21", "meal_price", "district"];
function testCoreAddedValue(obj, valueName, valueType, attribute) {
    if (CORE_ADDED_VALUE_CRITERION.indexOf(valueName) != -1) {
        if (attribute.value[0]._) {
            obj[valueName] = attribute.value[0]._;
        } else {
            obj[valueName] = attribute.value[0];
        }
        return true;
    }
}

var ADDED_VALUE_ATTRIBUTES = ["brunch","bring_your_own_bottle","sake","valet","private_room","interesting_beer_list","interesting_wine_list","cash_only","cocktail","dim_sum","pleasant","meals_in_garden","breakfast","no_smoke","disabled_access", "small_plates", "air_conditioning"];
function testAttributeAddedValue(obj, valueName, valueType, attribute) {
    if (ADDED_VALUE_ATTRIBUTES.indexOf(valueName) != -1) {
        if (attribute.value[0] == "0") return true;
        if (attribute.value[0] == "1") {
            if (obj.attributes.indexOf(valueName) == -1) {
                obj.attributes.push(valueName);
            }
            return true;
        }
    }
};

function processCookingLib(obj, valueName, valueType, attribute) {
    try {
        if (valueName == "cooking_lib") {
            if (attribute.item) {
                if (attribute.item.length != 1 || attribute.item[0].value.length != 1) {
                    console.error("Multiple cooking_id for Restaurant " + obj.name);
                } else {
                    obj[valueName] = attribute.item[0].value[0]._;
                    return true;
                }
            } else {
                console.error('Missing cooking_lib in ' + obj.id + ' (' + obj.name + ' in ' + obj.main_city + ')');
            }
        }

    } catch (err) {
        console.error("Failed during " + obj.name);
        throw err;
    }
};

function processCookingId(obj, valueName, valueType, attribute) {
    try {
        if (valueName == "cooking_id") {
            if (attribute.item && 
                attribute.item.length == 1 && 
                attribute.item[0].value && 
                attribute.item[0].value.length == 1) {
                obj[valueName] = attribute.item[0].value[0];
                return true;
            } else {
                console.error('Missing cooking_id in ' + obj.id + ' (' + obj.name + ' in ' + obj.main_city + ')');
                return true;
            }
        }

    } catch (err) {
        console.error("Failed during " + obj.name);
        throw err;
    }
};

var ADDED_VALUE_IGNORED_IF_ZERO = ["ascr", "open_park", "amex", "din", "visa", "mc", "cartesi"];
function testIgnoredAddedValue(valueName, attribute) {
    if (valueName == "restaurant_id") {
        if (attribute.item[0].value[0] == 1) return true;
    }
    if (valueName == "restaurant_lib") {
        if (attribute.item[0].value[0]._ == "restaurant") return true;
    }

    if (ADDED_VALUE_IGNORED_IF_ZERO.indexOf(valueName) != -1) {
        if (attribute.value[0] == 0) return true;
    }
};

var ADDED_VALUE_DETAIL_LISTS = ["facilities_details", "meals_details", "selections_details", "credit_cards_details", "prices_details", "services_details", "desc_details"];
function processDetailedLists(obj, valueName, valueType, attribute) {
    if (ADDED_VALUE_DETAIL_LISTS.indexOf(valueName) != -1) {
        var remaining = [];
        for (var i = 0; i < attribute.data.length; i++) {
            if (!processAddedValue(obj, attribute.data[i])) {
                remaining.push(attribute.data[i]);
            }
        }
        if (remaining.length > 0) {
            attribute.data = remaining;
        } else {
            return true;
        }
    }
};

function processRelationship(obj, origObj) {
    if (origObj.relationship.length != 1) {
        console.error("Too many relationships for " + obj.name);
    } else {
        processMediaRelationships(obj, origObj.relationship[0].media_relationship);
        processXOIRelationships(obj, origObj.relationship[0].xoi_relationship);
        if (origObj.relationship[0].media_relationship.length == 0) delete origObj.relationship[0].media_relationship;
        if (origObj.relationship[0].xoi_relationship.length == 0) delete origObj.relationship[0].xoi_relationship;
        if (!origObj.relationship[0].media_relationship && !origObj.relationship[0].xoi_relationship) delete origObj.relationship;
    }
};

function processMediaRelationships(obj, mediaRelationshipArray) {
    if (mediaRelationshipArray.length == 1) {
        if (mediaRelationshipArray[0] == "") mediaRelationshipArray.pop();
        else if (mediaRelationshipArray[0].photo && mediaRelationshipArray[0].photo.length == 1) {
            obj.photo = {
                identifier: mediaRelationshipArray[0].photo[0].identifier[0],
                author: mediaRelationshipArray[0].photo[0].author[0],
                copyright: mediaRelationshipArray[0].photo[0].copyright[0],
                orientation: mediaRelationshipArray[0].photo[0].orientation[0],
                representative: mediaRelationshipArray[0].photo[0].representative[0]
            };
            mediaRelationshipArray.pop();
        }
    } else {
        console.error('Too many photos relationships in ' + obj.id + ' (' + obj.name + ' in ' + obj.main_city + ')');
    }
};

function processXOIRelationships(obj, xoiRelationshipArray) {
    if (xoiRelationshipArray.length != 1 || !xoiRelationshipArray[0].xoi || !xoiRelationshipArray[0].xoi.length == 1) {
        // console.error('Too many xoi relationships in ' + obj.id + ' (' + obj.name + ' in ' + obj.main_city + ')');
        if (xoiRelationshipArray.length == 1 && xoiRelationshipArray[0] == "") xoiRelationshipArray.pop();
    } else {
        var identifier = xoiRelationshipArray[0].xoi[0].$.identifier;
        var type =  xoiRelationshipArray[0].xoi[0].$.type;
        var role =  xoiRelationshipArray[0].xoi[0].$.role;
        if (type == "CITY" && role == "parent") {
            obj.parent_city = identifier;
        } else {
            console.error("Bad xoi for " + obj.id + ' (' + obj.name + ' in ' + obj.main_city + ')');
        }
        xoiRelationshipArray.pop();
    }
};

function isEmptyObject(obj) {
  return !Object.keys(obj).length;
}
```


Analysis of data quality

