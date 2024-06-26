# Changelog

## v0.9.0-alpha

- Correctly serializes structure and enums in order they are added. (i.e. using OrderedDictionary)

## v0.8.0-alpha

- \_BIT datatype added
- added 2 memory operations, WriteBitToBoolOperation and WriteBoolToBitOperation
- updated to support mobject-deserialization v0.3.0
- Updated to support mobject-collections v1.3.0
- Updated to support mobject-disposable v1.1.1
- Updated to support mobject-enumerable v1.2.0
- Updated to support mobject-errors v0.3.0
- Updated to support mobject-events v1.1.0
- Updated to support mobject-serialization v0.5.0
- swapped values to reference to, so that they can be used directly in functions

## v0.7.0-alpha

- updated to support mobject-deserialization v0.2.0
- updated to support mobject-collections v1.2.0
- added interface datatype base

## v0.6.0-alpha

- finished / added TryCopyFrom on all datatypes.
- added IsUserDefined property to I_Datatype to assist with conversion
- I_StructuredDatatype now no longer has direct access to TryGetMemberByName (reason, see below)
- I_StructuredDatatype now extends I_HostStructureMembers which gives access to Members
- added 2 memory operations, MemCopyOperation and SafeMemCopyOperation

## v0.5.0-alpha

- bug fix TryDeserialize was always returning false on Enums
- moved primitives back to library, this reduces coupling.

## v0.4.0-alpha

- removed basic datatypes to their own library. mobject-basic-datatyps.
- renamed GetPrimitiveByTypeName in Datatypes and I_Datatypes
- completed support for enums
- added tests for base types

## v0.3.0-alpha

- updated Name to typeName on datatype base and serialization
- LREAL and REAL are now Numeric
- updated to support the new mobject-constants-datatype-limits v1.0.0
- Ubound and Lbound now MinValue and MaxValue in both class and serialization

## v0.2.0-alpha

- mobject-types change name to mobject-datatypes
- SerializeTypeWith refactored the following:
  - baseType -> baseDatatype
  - datatype -> name
  - isFloat added
- DatatypeBase has Datatype renamed to Name
- TryResolveAsAliasType renamed to TryResolveAsAliasDatatype
- TryResolveAsEnumType renamed to TryResolveAsEnumDatatype
- TryResolveAsStructuredType renamed to TryResolveAsStructuredDatatype
- Datatypes now supports adding enums
- Alias and Enums method names changed from Type to Datatype

## v0.1.2-alpha

- Corrected copy paste error, in which ULINT and UWORD were being treated as LINT when their bounds were serialized.

## v0.1.1-alpha

- Added mobject-converters 1.1.0
- Added Accept method to Datatypes to allow visitors
- Added I_EventEmitter to I_Datatypes
- Added event "OnDatatypeAdded" to Datatypes
- Added upper and lower bounds to integer datatypes
- Added new IntegerDatatypeBase
- Added IsSigned to integer datatypes
- Added enum datatype and tests

## v0.1.0-alpha

- Initial
