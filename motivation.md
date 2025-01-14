# Motivation

Developers frequently encounter the need to model units of measure, because objects in the real world are subject to these measures. Working with units require to understand the mathematics behind, how to convert between systems, and how to format and parse string representations of units. Most of this work can be consolidated into a library to avoid common problems and mistakes of conversion and approximation. 

Units give us a way to measure the physical world. There are many different units, partly because the world has different types of properties, such as length and mass, which are not interchangeable in normal physics. This type of property is sometimes called a "quantity" or a "dimension".
The word "dimension" fits because of the orthogonality of these properties. For example "mass" and "length" cannot be exchanged. Further, when we multiply physical measures the dimensions add up as exponents. For example, length times length becomes length².

A large body of work exists that specifies the dimensions, meanings, and names of various physical quantities.
In particular, the 11th General Conference on Weights and Measures in 1960 recommended a practical system of units of measurement, and gave it the name Systeme International d'Units (SI).
SI defines units for the base dimensions of length, mass, time, electric current, thermodynamic temperature, amount of substance, and luminous intensity.
SI also recognizes names and meaning of derived dimensions, such as area, volume, and force.
For some (but not all) of these derived dimensions SI defines units, such as "liter" for a unit of volume and "newton" for a unit of force. SI does not have a special name for area, although other systems of measurement do (as in "acre").

Despite the rising prominence of the metric system (the SI system), many developers have to work with non-SI units, such as feet, miles, acres, and gallons. A measurement can be expressed as a number of any unit, so long as the unit has the same dimension as the measured quantity. For example, any measure of volume can be expressed as a number of liters or gallons, because liters and gallons are units of volume, and all volumes have the dimension of length^3.
Therefore, a measure expressed as a number of liters can be 'converted' to a number of gallons.
Converting measures from one system of units to another is a common problem, but is subject to mathematics that can help to eliminate errors.