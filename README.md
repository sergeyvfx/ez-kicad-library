# Ez KiCAD Library

This is a personal library for KiCAD EDA.

There are few points to reason maintaining own library over using a standard one
or using someone's else library:

- Allow to be used as a Git submodule in projects, allowing to lock project to
  a specific version of the library.
- Is limited to components which are either already in the personal component
  library, or which are planned for being acquired for an on-going project.
- Parts are usually linked to DigiKey, which makes it easier to build BOM and
  actually acquire parts for projects.
- Footprints are more friendly for dense population.
- All components are attempted to be standardized to personal taste of silk
  screen.

This library is supposed to be used as a drop-in with minimal configuration in
project which uses it, without modifying global settings like KiCAD's global
search paths.

## Licensing

All the work done and implemented for this project is licensed under the
terms of MIT license.

## Configuration

Due to limitations of KiCAD EDA in topics related on making library portable
with zero configuration, there is some expection on the directory layout of
project:

<pre>
  MyProject.git
    Receiver
      hardware
        Receiver.pro
        Receiver.kicad_pcb
        Receiver.sch
    Transmitter
      hardware
        Receiver.pro
        Receiver.kicad_pcb
        Receiver.sch
    library
      footprint
      package3d
      symbol
</pre>

The library folder is supposed to be a git module to this repository.

Content of `sym-lib-table` file:
<pre>
(sym_lib_table
  (lib (name Amplifier_Operational)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Amplifier_Operational.lib)(options "")(descr ""))
  (lib (name Capacitor_Ceramic)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Capacitor_Ceramic.kicad_sym)(options "")(descr ""))
  (lib (name Capacitor_Electrolytic)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Capacitor_Electrolytic.lib)(options "")(descr ""))
  (lib (name Connector_Audio)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Connector_Audio.lib)(options "")(descr ""))
  (lib (name Connector_Battery)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Connector_Battery.lib)(options "")(descr ""))
  (lib (name Connector_Data)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Connector_Data.lib)(options "")(descr ""))
  (lib (name Connector_Generic)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Connector_Generic.lib)(options "")(descr ""))
  (lib (name Connector_RF)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Connector_RF.lib)(options "")(descr ""))
  (lib (name Crystal)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Crystal.lib)(options "")(descr ""))
  (lib (name Diode)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Diode.kicad_sym)(options "")(descr ""))
  (lib (name Inductor)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Inductor.lib)(options "")(descr ""))
  (lib (name Interface_Optical)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Interface_Optical.lib)(options "")(descr ""))
  (lib (name Interface_USB)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Interface_USB.lib)(options "")(descr ""))
  (lib (name LED)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/LED.lib)(options "")(descr ""))
  (lib (name Microcontroller)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Microcontroller.lib)(options "")(descr ""))
  (lib (name Potentiometer_Digital)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Potentiometer_Digital.lib)(options "")(descr ""))
  (lib (name Power)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Power.lib)(options "")(descr ""))
  (lib (name Power_Management)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Power_Management.lib)(options "")(descr ""))
  (lib (name Power_Supervisor)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Power_Supervisor.lib)(options "")(descr ""))
  (lib (name Resistor)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Resistor.kicad_sym)(options "")(descr ""))
  (lib (name Switches)(type Legacy)(uri D:/Projects/Electronics/IR-Volume-Control/library/symbol/Switches.lib)(options "")(descr ""))
  (lib (name Transistor_BJT)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Transistor_BJT.lib)(options "")(descr ""))
  (lib (name Transistor_FET)(type Legacy)(uri ${KIPRJMOD}/../../library/symbol/Transistor_FET.lib)(options "")(descr ""))
)
</pre>

Content of `fp-lib-table` file:
<pre>
(fp_lib_table
  (lib (name Interface_Optical)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Interface_Optical.pretty)(options "")(descr ""))
  (lib (name Capacitor_Ceramic)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Capacitor_Ceramic.pretty)(options "")(descr ""))
  (lib (name Capacitor_Electrolytic)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Capacitor_Electrolytic.pretty)(options "")(descr ""))
  (lib (name Connector_Audio)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Connector_Audio.pretty)(options "")(descr ""))
  (lib (name Connector_Battery)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Connector_Battery.pretty)(options "")(descr ""))
  (lib (name Connector_Data)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Connector_Data.pretty)(options "")(descr ""))
  (lib (name Connector_Generic)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Connector_Generic.pretty)(options "")(descr ""))
  (lib (name Connector_RF)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Connector_RF.pretty)(options "")(descr ""))
  (lib (name Crystal)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Crystal.pretty)(options "")(descr ""))
  (lib (name Diode)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Diode.pretty)(options "")(descr ""))
  (lib (name Inductor)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Inductor.pretty)(options "")(descr ""))
  (lib (name LED)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/LED.pretty)(options "")(descr ""))
  (lib (name Package_DFN_QFN)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Package_DFN_QFN.pretty)(options "")(descr ""))
  (lib (name Package_SO)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Package_SO.pretty)(options "")(descr ""))
  (lib (name Package_SON)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Package_SON.pretty)(options "")(descr ""))
  (lib (name Package_TO_SOT)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Package_TO_SOT.pretty)(options "")(descr ""))
  (lib (name Resistor)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Resistor.pretty)(options "")(descr ""))
  (lib (name Switches)(type KiCad)(uri D:/Projects/Electronics/IR-Volume-Control/library/footprint/Switches.pretty)(options "")(descr ""))
)
</pre>
