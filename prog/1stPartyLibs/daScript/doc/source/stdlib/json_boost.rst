
.. _stdlib_json_boost:

======================
Boost package for JSON
======================

.. include:: detail/json_boost.rst

The JSON boost module implements collection of helper macros and functions to accompany :ref:`JSON <stdlib_json>`.

All functions and symbols are in "json_boost" module, use require to get access to it. ::

    require daslib/json_boost


+++++++++++++
Reader macros
+++++++++++++

.. _call-macro-json_boost-json:

.. das:attribute:: json

This macro implements embedding of the JSON object into the program::
  var jsv = %json~
  {
    "name": "main_window",
    "value": 500,
    "size": [1,2,3]
  } %%

++++++++++++++
Variant macros
++++++++++++++

.. _call-macro-json_boost-better_json:

.. das:attribute:: better_json

This macro is used to implement `is json_value` and `as json_value` runtime checks.
It essencially substitutes `value as name` with `value.value as name` and `value is name` with `value.value is name`.

++++++++++++++++
Value conversion
++++++++++++++++

  *  :ref:`JV (v:float const) : json::JsonValue? <function-_at_json_boost_c__c_JV_Cf>` 
  *  :ref:`JV (v:int const) : json::JsonValue? <function-_at_json_boost_c__c_JV_Ci>` 
  *  :ref:`JV (v:bitfield const) : json::JsonValue? <function-_at_json_boost_c__c_JV_Ct>` 
  *  :ref:`JV (val:int8 const) : json::JsonValue? <function-_at_json_boost_c__c_JV_Ci8>` 
  *  :ref:`JV (val:uint8 const) : json::JsonValue? <function-_at_json_boost_c__c_JV_Cu8>` 
  *  :ref:`JV (val:int16 const) : json::JsonValue? <function-_at_json_boost_c__c_JV_Ci16>` 
  *  :ref:`JV (val:uint16 const) : json::JsonValue? <function-_at_json_boost_c__c_JV_Cu16>` 
  *  :ref:`JV (val:uint const) : json::JsonValue? <function-_at_json_boost_c__c_JV_Cu>` 
  *  :ref:`JV (val:int64 const) : json::JsonValue? <function-_at_json_boost_c__c_JV_Ci64>` 
  *  :ref:`JV (val:uint64 const) : json::JsonValue? <function-_at_json_boost_c__c_JV_Cu64>` 
  *  :ref:`from_JV (v:json::JsonValue explicit? const;ent:auto(EnumT) const;defV:EnumT const) : EnumT <function-_at_json_boost_c__c_from_JV_C1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__CY_ls_EnumT_gr_._CY_ls_EnumT_gr_L_%_ls_IsAnyEnumMacro_c_expect_any_enum(ent_eq_true)_gr_>` 
  *  :ref:`from_JV (v:json::JsonValue explicit? -const;ent:string const;defV:string const) : auto <function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Cs_Cs>` 
  *  :ref:`from_JV (v:json::JsonValue explicit? -const;ent:bool const;defV:bool const) : auto <function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Cb_Cb>` 
  *  :ref:`from_JV (v:json::JsonValue explicit? -const;ent:float const;defV:float const) : auto <function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Cf_Cf>` 
  *  :ref:`from_JV (v:json::JsonValue explicit? -const;ent:double const;defV:double const) : auto <function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Cd_Cd>` 
  *  :ref:`from_JV (v:json::JsonValue explicit? -const;ent:int const;defV:int const) : auto <function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Ci_Ci>` 
  *  :ref:`from_JV (v:json::JsonValue explicit? -const;ent:uint const;defV:uint const) : auto <function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Cu_Cu>` 
  *  :ref:`from_JV (v:json::JsonValue explicit? -const;ent:int64 const;defV:int64 const) : auto <function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Ci64_Ci64>` 
  *  :ref:`from_JV (v:json::JsonValue explicit? -const;ent:uint64 const;defV:uint64 const) : auto <function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Cu64_Cu64>` 
  *  :ref:`from_JV (v:json::JsonValue explicit? -const;ent:int8 const;defV:int8 const) : auto <function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Ci8_Ci8>` 
  *  :ref:`from_JV (v:json::JsonValue explicit? -const;ent:uint8 const;defV:uint8 const) : auto <function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Cu8_Cu8>` 
  *  :ref:`from_JV (v:json::JsonValue explicit? -const;ent:int16 const;defV:int16 const) : auto <function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Ci16_Ci16>` 
  *  :ref:`from_JV (v:json::JsonValue explicit? -const;ent:uint16 const;defV:uint16 const) : auto <function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Cu16_Cu16>` 
  *  :ref:`from_JV (v:json::JsonValue explicit? -const;ent:bitfield const;defV:bitfield const) : auto <function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Ct_Ct>` 
  *  :ref:`JV (v:auto(VecT) const) : auto <function-_at_json_boost_c__c_JV_CY_ls_VecT_gr_._%_ls_IsAnyVectorType_c_expect_any_vector_type(v_eq_true)_gr_>` 
  *  :ref:`from_JV (v:json::JsonValue explicit? -const;ent:auto(VecT) const;defV:VecT const) : auto <function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__CY_ls_VecT_gr_._CY_ls_VecT_gr_L_%_ls_IsAnyVectorType_c_expect_any_vector_type(ent_eq_true)_gr_>` 
  *  :ref:`from_JV (v:json::JsonValue explicit? -const;anything:table\<auto(KT);auto(VT)\> const) : auto <function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__C1_ls_Y_ls_KT_gr_._gr_2_ls_Y_ls_VT_gr_._gr_T>` 
  *  :ref:`from_JV (v:json::JsonValue explicit? -const;anything:auto(TT) const) : auto <function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__CY_ls_TT_gr_.>` 
  *  :ref:`JV (value:auto const) : json::JsonValue? <function-_at_json_boost_c__c_JV_C.>` 
  *  :ref:`JV (val1:auto const;val2:auto const) : json::JsonValue? <function-_at_json_boost_c__c_JV_C._C.>` 
  *  :ref:`JV (val1:auto const;val2:auto const;val3:auto const) : json::JsonValue? <function-_at_json_boost_c__c_JV_C._C._C.>` 
  *  :ref:`JV (val1:auto const;val2:auto const;val3:auto const;val4:auto const) : json::JsonValue? <function-_at_json_boost_c__c_JV_C._C._C._C.>` 
  *  :ref:`JV (val1:auto const;val2:auto const;val3:auto const;val4:auto const;val5:auto const) : json::JsonValue? <function-_at_json_boost_c__c_JV_C._C._C._C._C.>` 
  *  :ref:`JV (val1:auto const;val2:auto const;val3:auto const;val4:auto const;val5:auto const;val6:auto const) : json::JsonValue? <function-_at_json_boost_c__c_JV_C._C._C._C._C._C.>` 
  *  :ref:`JV (val1:auto const;val2:auto const;val3:auto const;val4:auto const;val5:auto const;val6:auto const;val7:auto const) : json::JsonValue? <function-_at_json_boost_c__c_JV_C._C._C._C._C._C._C.>` 
  *  :ref:`JV (val1:auto const;val2:auto const;val3:auto const;val4:auto const;val5:auto const;val6:auto const;val7:auto const;val8:auto const) : json::JsonValue? <function-_at_json_boost_c__c_JV_C._C._C._C._C._C._C._C.>` 
  *  :ref:`JV (val1:auto const;val2:auto const;val3:auto const;val4:auto const;val5:auto const;val6:auto const;val7:auto const;val8:auto const;val9:auto const) : json::JsonValue? <function-_at_json_boost_c__c_JV_C._C._C._C._C._C._C._C._C.>` 
  *  :ref:`JV (val1:auto const;val2:auto const;val3:auto const;val4:auto const;val5:auto const;val6:auto const;val7:auto const;val8:auto const;val9:auto const;val10:auto const) : json::JsonValue? <function-_at_json_boost_c__c_JV_C._C._C._C._C._C._C._C._C._C.>` 

.. _function-_at_json_boost_c__c_JV_Cf:

.. das:function:: JV(v: float const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+v       +float const  +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_Ci:

.. das:function:: JV(v: int const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+v       +int const    +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_Ct:

.. das:function:: JV(v: bitfield const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+----------------+
+argument+argument type   +
+========+================+
+v       +bitfield<> const+
+--------+----------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_Ci8:

.. das:function:: JV(val: int8 const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+val     +int8 const   +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_Cu8:

.. das:function:: JV(val: uint8 const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+val     +uint8 const  +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_Ci16:

.. das:function:: JV(val: int16 const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+val     +int16 const  +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_Cu16:

.. das:function:: JV(val: uint16 const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+val     +uint16 const +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_Cu:

.. das:function:: JV(val: uint const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+val     +uint const   +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_Ci64:

.. das:function:: JV(val: int64 const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+val     +int64 const  +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_Cu64:

.. das:function:: JV(val: uint64 const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+val     +uint64 const +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_from_JV_C1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__CY_ls_EnumT_gr_._CY_ls_EnumT_gr_L_%_ls_IsAnyEnumMacro_c_expect_any_enum(ent_eq_true)_gr_:

.. das:function:: from_JV(v: JsonValue? const; ent: auto(EnumT) const; defV: EnumT const)

from_JV returns EnumT

+--------+-------------------------------------------------------+
+argument+argument type                                          +
+========+=======================================================+
+v       + :ref:`json::JsonValue <struct-json-JsonValue>` ? const+
+--------+-------------------------------------------------------+
+ent     +auto(EnumT) const                                      +
+--------+-------------------------------------------------------+
+defV    +EnumT const                                            +
+--------+-------------------------------------------------------+


Parse a JSON value and return the corresponding native value.

.. _function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Cs_Cs:

.. das:function:: from_JV(v: JsonValue?; ent: string const; defV: string const)

from_JV returns auto

+--------+-------------------------------------------------+
+argument+argument type                                    +
+========+=================================================+
+v       + :ref:`json::JsonValue <struct-json-JsonValue>` ?+
+--------+-------------------------------------------------+
+ent     +string const                                     +
+--------+-------------------------------------------------+
+defV    +string const                                     +
+--------+-------------------------------------------------+


Parse a JSON value and return the corresponding native value.

.. _function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Cb_Cb:

.. das:function:: from_JV(v: JsonValue?; ent: bool const; defV: bool const)

from_JV returns auto

+--------+-------------------------------------------------+
+argument+argument type                                    +
+========+=================================================+
+v       + :ref:`json::JsonValue <struct-json-JsonValue>` ?+
+--------+-------------------------------------------------+
+ent     +bool const                                       +
+--------+-------------------------------------------------+
+defV    +bool const                                       +
+--------+-------------------------------------------------+


Parse a JSON value and return the corresponding native value.

.. _function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Cf_Cf:

.. das:function:: from_JV(v: JsonValue?; ent: float const; defV: float const)

from_JV returns auto

+--------+-------------------------------------------------+
+argument+argument type                                    +
+========+=================================================+
+v       + :ref:`json::JsonValue <struct-json-JsonValue>` ?+
+--------+-------------------------------------------------+
+ent     +float const                                      +
+--------+-------------------------------------------------+
+defV    +float const                                      +
+--------+-------------------------------------------------+


Parse a JSON value and return the corresponding native value.

.. _function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Cd_Cd:

.. das:function:: from_JV(v: JsonValue?; ent: double const; defV: double const)

from_JV returns auto

+--------+-------------------------------------------------+
+argument+argument type                                    +
+========+=================================================+
+v       + :ref:`json::JsonValue <struct-json-JsonValue>` ?+
+--------+-------------------------------------------------+
+ent     +double const                                     +
+--------+-------------------------------------------------+
+defV    +double const                                     +
+--------+-------------------------------------------------+


Parse a JSON value and return the corresponding native value.

.. _function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Ci_Ci:

.. das:function:: from_JV(v: JsonValue?; ent: int const; defV: int const)

from_JV returns auto

+--------+-------------------------------------------------+
+argument+argument type                                    +
+========+=================================================+
+v       + :ref:`json::JsonValue <struct-json-JsonValue>` ?+
+--------+-------------------------------------------------+
+ent     +int const                                        +
+--------+-------------------------------------------------+
+defV    +int const                                        +
+--------+-------------------------------------------------+


Parse a JSON value and return the corresponding native value.

.. _function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Cu_Cu:

.. das:function:: from_JV(v: JsonValue?; ent: uint const; defV: uint const)

from_JV returns auto

+--------+-------------------------------------------------+
+argument+argument type                                    +
+========+=================================================+
+v       + :ref:`json::JsonValue <struct-json-JsonValue>` ?+
+--------+-------------------------------------------------+
+ent     +uint const                                       +
+--------+-------------------------------------------------+
+defV    +uint const                                       +
+--------+-------------------------------------------------+


Parse a JSON value and return the corresponding native value.

.. _function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Ci64_Ci64:

.. das:function:: from_JV(v: JsonValue?; ent: int64 const; defV: int64 const)

from_JV returns auto

+--------+-------------------------------------------------+
+argument+argument type                                    +
+========+=================================================+
+v       + :ref:`json::JsonValue <struct-json-JsonValue>` ?+
+--------+-------------------------------------------------+
+ent     +int64 const                                      +
+--------+-------------------------------------------------+
+defV    +int64 const                                      +
+--------+-------------------------------------------------+


Parse a JSON value and return the corresponding native value.

.. _function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Cu64_Cu64:

.. das:function:: from_JV(v: JsonValue?; ent: uint64 const; defV: uint64 const)

from_JV returns auto

+--------+-------------------------------------------------+
+argument+argument type                                    +
+========+=================================================+
+v       + :ref:`json::JsonValue <struct-json-JsonValue>` ?+
+--------+-------------------------------------------------+
+ent     +uint64 const                                     +
+--------+-------------------------------------------------+
+defV    +uint64 const                                     +
+--------+-------------------------------------------------+


Parse a JSON value and return the corresponding native value.

.. _function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Ci8_Ci8:

.. das:function:: from_JV(v: JsonValue?; ent: int8 const; defV: int8 const)

from_JV returns auto

+--------+-------------------------------------------------+
+argument+argument type                                    +
+========+=================================================+
+v       + :ref:`json::JsonValue <struct-json-JsonValue>` ?+
+--------+-------------------------------------------------+
+ent     +int8 const                                       +
+--------+-------------------------------------------------+
+defV    +int8 const                                       +
+--------+-------------------------------------------------+


Parse a JSON value and return the corresponding native value.

.. _function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Cu8_Cu8:

.. das:function:: from_JV(v: JsonValue?; ent: uint8 const; defV: uint8 const)

from_JV returns auto

+--------+-------------------------------------------------+
+argument+argument type                                    +
+========+=================================================+
+v       + :ref:`json::JsonValue <struct-json-JsonValue>` ?+
+--------+-------------------------------------------------+
+ent     +uint8 const                                      +
+--------+-------------------------------------------------+
+defV    +uint8 const                                      +
+--------+-------------------------------------------------+


Parse a JSON value and return the corresponding native value.

.. _function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Ci16_Ci16:

.. das:function:: from_JV(v: JsonValue?; ent: int16 const; defV: int16 const)

from_JV returns auto

+--------+-------------------------------------------------+
+argument+argument type                                    +
+========+=================================================+
+v       + :ref:`json::JsonValue <struct-json-JsonValue>` ?+
+--------+-------------------------------------------------+
+ent     +int16 const                                      +
+--------+-------------------------------------------------+
+defV    +int16 const                                      +
+--------+-------------------------------------------------+


Parse a JSON value and return the corresponding native value.

.. _function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Cu16_Cu16:

.. das:function:: from_JV(v: JsonValue?; ent: uint16 const; defV: uint16 const)

from_JV returns auto

+--------+-------------------------------------------------+
+argument+argument type                                    +
+========+=================================================+
+v       + :ref:`json::JsonValue <struct-json-JsonValue>` ?+
+--------+-------------------------------------------------+
+ent     +uint16 const                                     +
+--------+-------------------------------------------------+
+defV    +uint16 const                                     +
+--------+-------------------------------------------------+


Parse a JSON value and return the corresponding native value.

.. _function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__Ct_Ct:

.. das:function:: from_JV(v: JsonValue?; ent: bitfield const; defV: bitfield const)

from_JV returns auto

+--------+-------------------------------------------------+
+argument+argument type                                    +
+========+=================================================+
+v       + :ref:`json::JsonValue <struct-json-JsonValue>` ?+
+--------+-------------------------------------------------+
+ent     +bitfield<> const                                 +
+--------+-------------------------------------------------+
+defV    +bitfield<> const                                 +
+--------+-------------------------------------------------+


Parse a JSON value and return the corresponding native value.

.. _function-_at_json_boost_c__c_JV_CY_ls_VecT_gr_._%_ls_IsAnyVectorType_c_expect_any_vector_type(v_eq_true)_gr_:

.. das:function:: JV(v: auto(VecT) const)

JV returns auto

+--------+----------------+
+argument+argument type   +
+========+================+
+v       +auto(VecT) const+
+--------+----------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__CY_ls_VecT_gr_._CY_ls_VecT_gr_L_%_ls_IsAnyVectorType_c_expect_any_vector_type(ent_eq_true)_gr_:

.. das:function:: from_JV(v: JsonValue?; ent: auto(VecT) const; defV: VecT const)

from_JV returns auto

+--------+-------------------------------------------------+
+argument+argument type                                    +
+========+=================================================+
+v       + :ref:`json::JsonValue <struct-json-JsonValue>` ?+
+--------+-------------------------------------------------+
+ent     +auto(VecT) const                                 +
+--------+-------------------------------------------------+
+defV    +VecT const                                       +
+--------+-------------------------------------------------+


Parse a JSON value and return the corresponding native value.

.. _function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__C1_ls_Y_ls_KT_gr_._gr_2_ls_Y_ls_VT_gr_._gr_T:

.. das:function:: from_JV(v: JsonValue?; anything: table<auto(KT);auto(VT)> const)

from_JV returns auto

+--------+-------------------------------------------------+
+argument+argument type                                    +
+========+=================================================+
+v       + :ref:`json::JsonValue <struct-json-JsonValue>` ?+
+--------+-------------------------------------------------+
+anything+table<auto(KT);auto(VT)> const                   +
+--------+-------------------------------------------------+


Parse a JSON value and return the corresponding native value.

.. _function-_at_json_boost_c__c_from_JV_1_ls_XS_ls_json_c__c_JsonValue_gr__gr__qm__CY_ls_TT_gr_.:

.. das:function:: from_JV(v: JsonValue?; anything: auto(TT) const)

from_JV returns auto

+--------+-------------------------------------------------+
+argument+argument type                                    +
+========+=================================================+
+v       + :ref:`json::JsonValue <struct-json-JsonValue>` ?+
+--------+-------------------------------------------------+
+anything+auto(TT) const                                   +
+--------+-------------------------------------------------+


Parse a JSON value and return the corresponding native value.

.. _function-_at_json_boost_c__c_JV_C.:

.. das:function:: JV(value: auto const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+value   +auto const   +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_C._C.:

.. das:function:: JV(val1: auto const; val2: auto const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+val1    +auto const   +
+--------+-------------+
+val2    +auto const   +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_C._C._C.:

.. das:function:: JV(val1: auto const; val2: auto const; val3: auto const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+val1    +auto const   +
+--------+-------------+
+val2    +auto const   +
+--------+-------------+
+val3    +auto const   +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_C._C._C._C.:

.. das:function:: JV(val1: auto const; val2: auto const; val3: auto const; val4: auto const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+val1    +auto const   +
+--------+-------------+
+val2    +auto const   +
+--------+-------------+
+val3    +auto const   +
+--------+-------------+
+val4    +auto const   +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_C._C._C._C._C.:

.. das:function:: JV(val1: auto const; val2: auto const; val3: auto const; val4: auto const; val5: auto const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+val1    +auto const   +
+--------+-------------+
+val2    +auto const   +
+--------+-------------+
+val3    +auto const   +
+--------+-------------+
+val4    +auto const   +
+--------+-------------+
+val5    +auto const   +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_C._C._C._C._C._C.:

.. das:function:: JV(val1: auto const; val2: auto const; val3: auto const; val4: auto const; val5: auto const; val6: auto const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+val1    +auto const   +
+--------+-------------+
+val2    +auto const   +
+--------+-------------+
+val3    +auto const   +
+--------+-------------+
+val4    +auto const   +
+--------+-------------+
+val5    +auto const   +
+--------+-------------+
+val6    +auto const   +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_C._C._C._C._C._C._C.:

.. das:function:: JV(val1: auto const; val2: auto const; val3: auto const; val4: auto const; val5: auto const; val6: auto const; val7: auto const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+val1    +auto const   +
+--------+-------------+
+val2    +auto const   +
+--------+-------------+
+val3    +auto const   +
+--------+-------------+
+val4    +auto const   +
+--------+-------------+
+val5    +auto const   +
+--------+-------------+
+val6    +auto const   +
+--------+-------------+
+val7    +auto const   +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_C._C._C._C._C._C._C._C.:

.. das:function:: JV(val1: auto const; val2: auto const; val3: auto const; val4: auto const; val5: auto const; val6: auto const; val7: auto const; val8: auto const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+val1    +auto const   +
+--------+-------------+
+val2    +auto const   +
+--------+-------------+
+val3    +auto const   +
+--------+-------------+
+val4    +auto const   +
+--------+-------------+
+val5    +auto const   +
+--------+-------------+
+val6    +auto const   +
+--------+-------------+
+val7    +auto const   +
+--------+-------------+
+val8    +auto const   +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_C._C._C._C._C._C._C._C._C.:

.. das:function:: JV(val1: auto const; val2: auto const; val3: auto const; val4: auto const; val5: auto const; val6: auto const; val7: auto const; val8: auto const; val9: auto const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+val1    +auto const   +
+--------+-------------+
+val2    +auto const   +
+--------+-------------+
+val3    +auto const   +
+--------+-------------+
+val4    +auto const   +
+--------+-------------+
+val5    +auto const   +
+--------+-------------+
+val6    +auto const   +
+--------+-------------+
+val7    +auto const   +
+--------+-------------+
+val8    +auto const   +
+--------+-------------+
+val9    +auto const   +
+--------+-------------+


skip functions
skip void?

.. _function-_at_json_boost_c__c_JV_C._C._C._C._C._C._C._C._C._C.:

.. das:function:: JV(val1: auto const; val2: auto const; val3: auto const; val4: auto const; val5: auto const; val6: auto const; val7: auto const; val8: auto const; val9: auto const; val10: auto const)

JV returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+-------------+
+argument+argument type+
+========+=============+
+val1    +auto const   +
+--------+-------------+
+val2    +auto const   +
+--------+-------------+
+val3    +auto const   +
+--------+-------------+
+val4    +auto const   +
+--------+-------------+
+val5    +auto const   +
+--------+-------------+
+val6    +auto const   +
+--------+-------------+
+val7    +auto const   +
+--------+-------------+
+val8    +auto const   +
+--------+-------------+
+val9    +auto const   +
+--------+-------------+
+val10   +auto const   +
+--------+-------------+


skip functions
skip void?

+++++++++++++
Uncategorized
+++++++++++++

.. _function-_at_json_boost_c__c__qm__lb__rb__C_eq_1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Cs:

.. das:function:: operator ?[](a: JsonValue? const ==const; key: string const)

?[] returns  :ref:`json::JsonValue <struct-json-JsonValue>` ? const

+--------+--------------------------------------------------------+
+argument+argument type                                           +
+========+========================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ? const!+
+--------+--------------------------------------------------------+
+key     +string const                                            +
+--------+--------------------------------------------------------+


Returns the value of the index in the JSON array, if it exists.

.. _function-_at_json_boost_c__c__qm__lb__rb___eq_1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Cs:

.. das:function:: operator ?[](a: JsonValue? ==const; key: string const)

?[] returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+--------------------------------------------------+
+argument+argument type                                     +
+========+==================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ?!+
+--------+--------------------------------------------------+
+key     +string const                                      +
+--------+--------------------------------------------------+


Returns the value of the index in the JSON array, if it exists.

.. _function-_at_json_boost_c__c__qm_._C_eq_1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Cs:

.. das:function:: operator ?.(a: JsonValue? const ==const; key: string const)

?. returns  :ref:`json::JsonValue <struct-json-JsonValue>` ? const

+--------+--------------------------------------------------------+
+argument+argument type                                           +
+========+========================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ? const!+
+--------+--------------------------------------------------------+
+key     +string const                                            +
+--------+--------------------------------------------------------+


Returns the value of the key in the JSON object, if it exists.

.. _function-_at_json_boost_c__c__qm_.__eq_1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Cs:

.. das:function:: operator ?.(a: JsonValue? ==const; key: string const)

?. returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+--------------------------------------------------+
+argument+argument type                                     +
+========+==================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ?!+
+--------+--------------------------------------------------+
+key     +string const                                      +
+--------+--------------------------------------------------+


Returns the value of the key in the JSON object, if it exists.

.. _function-_at_json_boost_c__c__qm__lb__rb__C_eq_1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Ci:

.. das:function:: operator ?[](a: JsonValue? const ==const; idx: int const)

?[] returns  :ref:`json::JsonValue <struct-json-JsonValue>` ? const

+--------+--------------------------------------------------------+
+argument+argument type                                           +
+========+========================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ? const!+
+--------+--------------------------------------------------------+
+idx     +int const                                               +
+--------+--------------------------------------------------------+


Returns the value of the index in the JSON array, if it exists.

.. _function-_at_json_boost_c__c__qm__lb__rb___eq_1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Ci:

.. das:function:: operator ?[](a: JsonValue? ==const; idx: int const)

?[] returns  :ref:`json::JsonValue <struct-json-JsonValue>` ?

+--------+--------------------------------------------------+
+argument+argument type                                     +
+========+==================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ?!+
+--------+--------------------------------------------------+
+idx     +int const                                         +
+--------+--------------------------------------------------+


Returns the value of the index in the JSON array, if it exists.

.. _function-_at_json_boost_c__c__qm__qm__C1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Cd:

.. das:function:: operator ??(a: JsonValue? const; val: double const)

?? returns double

+--------+-------------------------------------------------------+
+argument+argument type                                          +
+========+=======================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ? const+
+--------+-------------------------------------------------------+
+val     +double const                                           +
+--------+-------------------------------------------------------+


Returns the value of the JSON object, if it exists, otherwise returns the default value.

.. _function-_at_json_boost_c__c__qm__qm__C1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Cf:

.. das:function:: operator ??(a: JsonValue? const; val: float const)

?? returns float

+--------+-------------------------------------------------------+
+argument+argument type                                          +
+========+=======================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ? const+
+--------+-------------------------------------------------------+
+val     +float const                                            +
+--------+-------------------------------------------------------+


Returns the value of the JSON object, if it exists, otherwise returns the default value.

.. _function-_at_json_boost_c__c__qm__qm__C1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Ci8:

.. das:function:: operator ??(a: JsonValue? const; val: int8 const)

?? returns int8

+--------+-------------------------------------------------------+
+argument+argument type                                          +
+========+=======================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ? const+
+--------+-------------------------------------------------------+
+val     +int8 const                                             +
+--------+-------------------------------------------------------+


Returns the value of the JSON object, if it exists, otherwise returns the default value.

.. _function-_at_json_boost_c__c__qm__qm__C1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Ci16:

.. das:function:: operator ??(a: JsonValue? const; val: int16 const)

?? returns int16

+--------+-------------------------------------------------------+
+argument+argument type                                          +
+========+=======================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ? const+
+--------+-------------------------------------------------------+
+val     +int16 const                                            +
+--------+-------------------------------------------------------+


Returns the value of the JSON object, if it exists, otherwise returns the default value.

.. _function-_at_json_boost_c__c__qm__qm__C1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Ci:

.. das:function:: operator ??(a: JsonValue? const; val: int const)

?? returns int

+--------+-------------------------------------------------------+
+argument+argument type                                          +
+========+=======================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ? const+
+--------+-------------------------------------------------------+
+val     +int const                                              +
+--------+-------------------------------------------------------+


Returns the value of the JSON object, if it exists, otherwise returns the default value.

.. _function-_at_json_boost_c__c__qm__qm__C1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Ci64:

.. das:function:: operator ??(a: JsonValue? const; val: int64 const)

?? returns int64

+--------+-------------------------------------------------------+
+argument+argument type                                          +
+========+=======================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ? const+
+--------+-------------------------------------------------------+
+val     +int64 const                                            +
+--------+-------------------------------------------------------+


Returns the value of the JSON object, if it exists, otherwise returns the default value.

.. _function-_at_json_boost_c__c__qm__qm__C1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Cu8:

.. das:function:: operator ??(a: JsonValue? const; val: uint8 const)

?? returns uint8

+--------+-------------------------------------------------------+
+argument+argument type                                          +
+========+=======================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ? const+
+--------+-------------------------------------------------------+
+val     +uint8 const                                            +
+--------+-------------------------------------------------------+


Returns the value of the JSON object, if it exists, otherwise returns the default value.

.. _function-_at_json_boost_c__c__qm__qm__C1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Cu16:

.. das:function:: operator ??(a: JsonValue? const; val: uint16 const)

?? returns uint16

+--------+-------------------------------------------------------+
+argument+argument type                                          +
+========+=======================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ? const+
+--------+-------------------------------------------------------+
+val     +uint16 const                                           +
+--------+-------------------------------------------------------+


Returns the value of the JSON object, if it exists, otherwise returns the default value.

.. _function-_at_json_boost_c__c__qm__qm__C1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Cu:

.. das:function:: operator ??(a: JsonValue? const; val: uint const)

?? returns uint

+--------+-------------------------------------------------------+
+argument+argument type                                          +
+========+=======================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ? const+
+--------+-------------------------------------------------------+
+val     +uint const                                             +
+--------+-------------------------------------------------------+


Returns the value of the JSON object, if it exists, otherwise returns the default value.

.. _function-_at_json_boost_c__c__qm__qm__C1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Cu64:

.. das:function:: operator ??(a: JsonValue? const; val: uint64 const)

?? returns uint64

+--------+-------------------------------------------------------+
+argument+argument type                                          +
+========+=======================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ? const+
+--------+-------------------------------------------------------+
+val     +uint64 const                                           +
+--------+-------------------------------------------------------+


Returns the value of the JSON object, if it exists, otherwise returns the default value.

.. _function-_at_json_boost_c__c__qm__qm__C1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Cb:

.. das:function:: operator ??(a: JsonValue? const; val: bool const)

?? returns bool

+--------+-------------------------------------------------------+
+argument+argument type                                          +
+========+=======================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ? const+
+--------+-------------------------------------------------------+
+val     +bool const                                             +
+--------+-------------------------------------------------------+


Returns the value of the JSON object, if it exists, otherwise returns the default value.

.. _function-_at_json_boost_c__c__qm__qm__C1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm__Cs:

.. das:function:: operator ??(a: JsonValue? const; val: string const)

?? returns string

+--------+-------------------------------------------------------+
+argument+argument type                                          +
+========+=======================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ? const+
+--------+-------------------------------------------------------+
+val     +string const                                           +
+--------+-------------------------------------------------------+


Returns the value of the JSON object, if it exists, otherwise returns the default value.

.. _function-_at_json_boost_c__c__qm_._rq_value_C_eq_1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm_:

.. das:function:: operator ?.`value(a: JsonValue? const ==const)

?.`value returns  :ref:`JsValue <alias-JsValue>` ?

+--------+--------------------------------------------------------+
+argument+argument type                                           +
+========+========================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ? const!+
+--------+--------------------------------------------------------+


Returns the value of the JSON object, if it exists.

.. _function-_at_json_boost_c__c__qm_._rq_value__eq_1_ls_S_ls_json_c__c_JsonValue_gr__gr__qm_:

.. das:function:: operator ?.`value(a: JsonValue? ==const)

?.`value returns  :ref:`JsValue <alias-JsValue>` ?

+--------+--------------------------------------------------+
+argument+argument type                                     +
+========+==================================================+
+a       + :ref:`json::JsonValue <struct-json-JsonValue>` ?!+
+--------+--------------------------------------------------+


Returns the value of the JSON object, if it exists.


