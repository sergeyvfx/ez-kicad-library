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
  (version 7)
  (lib (name "Amplifier_Operational")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Amplifier_Operational.kicad_sym")(options "")(descr ""))
  (lib (name "Capacitor_Ceramic")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Capacitor_Ceramic.kicad_sym")(options "")(descr ""))
  (lib (name "Capacitor_Electrolytic")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Capacitor_Electrolytic.kicad_sym")(options "")(descr ""))
  (lib (name "Circuit_Protection")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Circuit_Protection.kicad_sym")(options "")(descr ""))
  (lib (name "Connector_Audio")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Connector_Audio.kicad_sym")(options "")(descr ""))
  (lib (name "Connector_Battery")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Connector_Battery.kicad_sym")(options "")(descr ""))
  (lib (name "Connector_CardEdge")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Connector_CardEdge.kicad_sym")(options "")(descr ""))
  (lib (name "Connector_Data")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Connector_Data.kicad_sym")(options "")(descr ""))
  (lib (name "Connector_Generic")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Connector_Generic.kicad_sym")(options "")(descr ""))
  (lib (name "Connector_RF")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Connector_RF.kicad_sym")(options "")(descr ""))
  (lib (name "Crystal")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Crystal.kicad_sym")(options "")(descr ""))
  (lib (name "Diode")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Diode.kicad_sym")(options "")(descr ""))
  (lib (name "Inductor")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Inductor.kicad_sym")(options "")(descr ""))
  (lib (name "Interface_Optical")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Interface_Optical.kicad_sym")(options "")(descr ""))
  (lib (name "Interface_USB")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Interface_USB.kicad_sym")(options "")(descr ""))
  (lib (name "LED")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/LED.kicad_sym")(options "")(descr ""))
  (lib (name "Logic")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Logic.kicad_sym")(options "")(descr ""))
  (lib (name "Mechanical")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Mechanical.kicad_sym")(options "")(descr ""))
  (lib (name "Microcontroller")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Microcontroller.kicad_sym")(options "")(descr ""))
  (lib (name "Potentiometer_Digital")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Potentiometer_Digital.kicad_sym")(options "")(descr ""))
  (lib (name "Power")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Power.kicad_sym")(options "")(descr ""))
  (lib (name "Power_Management")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Power_Management.kicad_sym")(options "")(descr ""))
  (lib (name "Power_Supervisor")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Power_Supervisor.kicad_sym")(options "")(descr ""))
  (lib (name "Resistor")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Resistor.kicad_sym")(options "")(descr ""))
  (lib (name "Switches")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Switches.kicad_sym")(options "")(descr ""))
  (lib (name "Transistor_BJT")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Transistor_BJT.kicad_sym")(options "")(descr ""))
  (lib (name "Transistor_FET")(type "KiCad")(uri "${KIPRJMOD}/../../library/symbol/Transistor_FET.kicad_sym")(options "")(descr ""))
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
  (lib (name Connector_CardEdge)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Connector_CardEdge.pretty)(options "")(descr ""))
  (lib (name Connector_Data)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Connector_Data.pretty)(options "")(descr ""))
  (lib (name Connector_Generic)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Connector_Generic.pretty)(options "")(descr ""))
  (lib (name Connector_RF)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Connector_RF.pretty)(options "")(descr ""))
  (lib (name Crystal)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Crystal.pretty)(options "")(descr ""))
  (lib (name Diode)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Diode.pretty)(options "")(descr ""))
  (lib (name Inductor)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Inductor.pretty)(options "")(descr ""))
  (lib (name LED)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/LED.pretty)(options "")(descr ""))
  (lib (name Mechanical)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Mechanical.pretty)(options "")(descr ""))
  (lib (name Package_DFN_QFN)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Package_DFN_QFN.pretty)(options "")(descr ""))
  (lib (name Package_SO)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Package_SO.pretty)(options "")(descr ""))
  (lib (name Package_SON)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Package_SON.pretty)(options "")(descr ""))
  (lib (name Package_TO_SOT)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Package_TO_SOT.pretty)(options "")(descr ""))
  (lib (name Resistor)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Resistor.pretty)(options "")(descr ""))
  (lib (name Switches)(type KiCad)(uri ${KIPRJMOD}/../../library/footprint/Switches.pretty)(options "")(descr ""))
)
</pre>
