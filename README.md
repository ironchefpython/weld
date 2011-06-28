This is my fork of weld, to add a few enhancements to support my personal projects.

Utimately, I'd like to be have a version of weld that is able to perform the following actions.

var $ = require('jquery');

require('weld').plugin($);                  // import weld and register it with jquery as a plugin


var weldInstance = $('.myDiv').weldable();  // created a "weldable" element

weldInstance.weld(data)                     // welds new data to the element

weldInstance.clear();                       // removes the element and all siblings

weldInstance.weld(data)                     // creates the element again, and welds data
                                            // to it

weldInstance.append(otherData)              // adds a sibling to the element, and welds 
                                            // otherData to it

weldInstance.update(dataArray)              // updates the element and all siblings, matching 
                                            // elements with data based on a key



data = weldInstance.unweld()                // The is the key activity I'm trying to support
                                            // My goal is to be able to reverse the weld function
                                            // and extract an object, or an array of objects 
                                            // from the same block of HTML that would be a target 
                                            // of a weld
