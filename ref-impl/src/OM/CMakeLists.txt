###############################################################################
#
# $Id$ $Name$
#
# The contents of this file are subject to the AAF SDK Public Source
# License Agreement Version 2.0 (the "License"); You may not use this
# file except in compliance with the License.  The License is available
# in AAFSDKPSL.TXT, or you may obtain a copy of the License from the
# Advanced Media Workflow Association, Inc., or its successor.
#
# Software distributed under the License is distributed on an "AS IS"
# basis, WITHOUT WARRANTY OF ANY KIND, either express or implied.  See
# the License for the specific language governing rights and limitations
# under the License.  Refer to Section 3.3 of the License for proper use
# of this Exhibit.
#
# WARNING:  Please contact the Advanced Media Workflow Association,
# Inc., for more information about any additional licenses to
# intellectual property covering the AAF Standard that may be required
# to create and distribute AAF compliant products.
# (http://www.amwa.tv/policies).
#
# Copyright Notices:
# The Original Code of this file is Copyright 1998-2012, licensor of the
# Advanced Media Workflow Association.  All rights reserved.
#
# The Initial Developer of the Original Code of this file and the
# licensor of the Advanced Media Workflow Association is
# Avid Technology.
# All rights reserved.
#
###############################################################################

cmake_minimum_required(VERSION 3.0.2)

if(NOT DEFINED AAFSDK_ROOT)
    message(FATAL_ERROR "'AAFSDK_ROOT' must be set. Run a build from the top-level CMakeLists.txt script.")
endif()

# MSVC: ./AAFWinSDK/<vsXX>/ref-impl/Om/<Win32|x64>/<Debug|Release>/
# Makefile: ./AAFx86_64LinuxSDK/g++/OM/<debug|>
set(TARGET_DIR "${AAFSDK_TARGET_DIR}")

add_library(OM STATIC
    OMArrayType.cpp
    OMAssertions.cpp
    OMBufferedIStream.cpp
    OMBufferedStream.cpp
    OMByteArray.cpp
    OMCachedDiskRawStorage.cpp
    OMCachedRawStorage.cpp
    OMCachePageAllocator.cpp
    OMCharacterType.cpp
    OMClassDefinition.cpp
    OMContainerElement.cpp
    OMContainerProperty.cpp
    OMDataSet.cpp
    OMDataStream.cpp
    OMDataStreamAccess.cpp
    OMDataStreamProperty.cpp
    OMDataStreamPropertyFilter.cpp
    OMDataTypes.cpp
    OMDataVector.cpp
    OMDefinition.cpp
    OMDictionary.cpp
    OMDiskRawStorage.cpp
    OMDynamicLibrary.cpp
    OMEnumeratedType.cpp
    OMExceptions.cpp
    OMExtendibleEnumeratedType.cpp
    OMFile.cpp
    OMGSF_SSStoredObjectFactory.cpp
    OMGSFStructuredStorage.cpp
    OMIndirectType.cpp
    OMIntegerType.cpp
    OMIOStream.cpp
    OMKLVStoredObject.cpp
    OMKLVStoredObjectFactory.cpp
    OMKLVStoredStream.cpp
    OMKLVStoredStreamFilter.cpp
    OMMappedFileRawStorage.cpp
    OMMemoryRawStorage.cpp
    OMMS_SSStoredObjectFactory.cpp
    OMMSStructuredStorage.cpp
    OMMXFStorage.cpp
    OMMXFStorageBase.cpp
    OMObjectManager.cpp
    OMObjectReference.cpp
    OMObjectReferenceType.cpp
    OMOpaqueType.cpp
    OMOStream.cpp
    OMPageCache.cpp
    OMProperty.cpp
    OMPropertyDefinition.cpp
    OMPropertySet.cpp
    OMPropertySetIterator.cpp
    OMPropertyTable.cpp
    OMRawStorageLockBytes.cpp
    OMRecordType.cpp
    OMRefProperty.cpp
    OMRefSetProperty.cpp
    OMRefVectorProperty.cpp
    OMRenamedType.cpp
    OMRootStorable.cpp
    OMSetType.cpp
    OMSS_SSStoredObjectFactory.cpp
    OMSSSStorageRWInputSource.cpp
    OMSSStoredObject.cpp
    OMSSStoredObjectFactory.cpp
    OMSSStoredStream.cpp
    OMSSStructuredStorage.cpp
    OMStackTrace.cpp
    OMStorable.cpp
    OMStoredObject.cpp
    OMStoredObjectFactory.cpp
    OMStoredPropertySetIndex.cpp
    OMStoredSetIndex.cpp
    OMStoredVectorIndex.cpp
    OMStream.cpp
    OMStreamType.cpp
    OMStringProperty.cpp
    OMStringType.cpp
    OMStrongReference.cpp
    OMStrongReferenceSet.cpp
    OMStrongReferenceVector.cpp
    OMSymbolspace.cpp
    OMType.cpp
    OMTypeDefinition.cpp
    OMTypeVisitor.cpp
    OMUniqueObjectIdentType.cpp
    OMUtilities.cpp
    OMWeakReference.cpp
    OMWeakReferenceSet.cpp
    OMWeakReferenceVector.cpp
    OMWideStringProperty.cpp
    OMWrappedRawStorage.cpp
    OMWString.cpp
    OMXMLReader.cpp
    OMXMLStorage.cpp
    OMXMLStoredObject.cpp
    OMXMLStoredObjectFactory.cpp
    OMXMLStoredStream.cpp
    OMXMLUtilities.cpp
    OMXMLWriter.cpp
    utf8.cpp
    OMArrayPropertyIteratorT.h
    OMArrayPropertyT.h
    OMAssertions.h
    OMAVLTreeT.h
    OMByteArray.h
    OMCharacterStringPropertyT.h
    OMClassFactory.h
    OMContainerElementT.h
    OMFile.h
    OMFixedSizePropertyT.h
    OMGSFStructuredStorage.h
    OMIdentitySetIterT.h
    OMIdentitySetT.h
    OMListIteratorT.h
    OMListT.h
    OMMSStructuredStorage.h
    OMObjectReferenceT.h
    OMPortability.h
    OMRedBlackTreeIteratorT.h
    OMRedBlackTreeT.h
    OMReferenceSetIterT.h
    OMReferenceSetT.h
    OMReferenceVectorIterT.h
    OMReferenceVectorT.h
    OMRootStorable.h
    OMSetIteratorT.h
    OMSetPropertyIteratorT.h
    OMSetPropertyT.h
    OMSetT.h
    OMSingletonT.h
    OMSSSStorageRWInputSource.h
    OMSSStructuredStorage.h
    OMStorable.h
    OMStoredObject.h
    OMStoredObjectFactory.h
    OMStoredPropertySetIndex.h
    OMStoredSetIndex.h
    OMStoredVectorIndex.h
    OMStreamPropertyT.h
    OMStrongReferenceSetIterT.h
    OMStrongReferenceVectorIterT.h
    OMStrongRefPropertyT.h
    OMStrongRefSetPropertyT.h
    OMStrongRefVectorPropertyT.h
    OMStructuredStorage.h
    OMSymbolspace.h
    OMUtilities.h
    OMVariableSizePropertyT.h
    OMVectorIteratorT.h
    OMVectorT.h
    OMWeakReferenceSetIterT.h
    OMWeakReferenceVectorIterT.h
    OMWeakRefPropertyT.h
    OMWeakRefSetPropertyT.h
    OMWeakRefVectorPropertyT.h
    OMWString.h
    OMXMLReader.h
    OMXMLStorage.h
    OMXMLUtilities.h
    OMXMLWriter.h
)

target_sources(OM PUBLIC
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMArrayProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMArrayPropertyIterator.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMArrayType.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMAVLTree.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMBufferedIStream.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMBufferedStream.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMCachedDiskRawStorage.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMCachedRawStorage.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMCachePageAllocator.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMCharacterStringProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMCharacterType.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMClassDefinition.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMContainer.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMContainerElement.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMContainerIterator.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMContainerProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMDataContainer.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMDataContainerIterator.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMDataSet.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMDataStream.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMDataStreamAccess.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMDataStreamProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMDataStreamPropertyFilter.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMDataTypes.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMDataVector.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMDefinition.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMDictionary.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMDiskRawStorage.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMDynamicLibrary.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMEnumeratedType.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMExceptions.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMExtendibleEnumeratedType.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMFixedSizeProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMGSF_SSStoredObjectFactory.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMIdentitySet.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMIdentitySetIter.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMIndirectType.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMIntegerType.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMIOStream.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMKLVStoredObject.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMKLVStoredObjectFactory.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMKLVStoredStream.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMKLVStoredStreamFilter.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMList.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMListIterator.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMMappedFileRawStorage.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMMemoryRawStorage.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMMS_SSStoredObjectFactory.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMMXFStorage.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMMXFStorageBase.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMObject.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMObjectManager.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMObjectReference.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMObjectReferenceType.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMObjectSet.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMObjectVector.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMOpaqueType.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMOStream.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMPageCache.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMPropertyDefinition.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMPropertySet.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMPropertySetIterator.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMPropertyTable.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMRawStorage.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMRawStorageLockBytes.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMRecordType.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMRedBlackTree.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMRedBlackTreeIterator.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMReferenceContainer.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMReferenceContainerIter.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMReferenceSet.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMReferenceSetIter.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMReferenceVector.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMReferenceVectorIter.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMRefProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMRefSetProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMRefVectorProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMRenamedType.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMSet.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMSetIterator.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMSetProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMSetPropertyIterator.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMSetType.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMSingleton.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMSSStoredObject.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMSSStoredObjectFactory.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMSSStoredStream.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMSS_SSStoredObjectFactory.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMStackTrace.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMStoredStream.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMStoredStreamFilter.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMStream.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMStreamProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMStreamType.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMStringProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMStringType.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMStrongReference.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMStrongReferenceSet.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMStrongReferenceSetIter.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMStrongReferenceVector.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMStrongReferenceVectorIter.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMStrongRefProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMStrongRefSetProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMStrongRefVectorProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMTransparentStoredStreamFilter.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMType.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMTypeDefinition.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMTypeVisitor.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMUniqueObjectIdentType.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMVariableSizeProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMVector.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMVectorIterator.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMWeakReference.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMWeakReferenceSet.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMWeakReferenceSetIter.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMWeakReferenceVector.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMWeakReferenceVectorIter.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMWeakRefProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMWeakRefSetProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMWeakRefVectorProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMWideStringProperty.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMWrappedRawStorage.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMXMLStoredObject.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMXMLStoredObjectFactory.h
    ${AAFSDK_ROOT}/ref-impl/include/OM/OMXMLStoredStream.h
)

target_include_directories(OM PUBLIC
    ${AAFSDK_ROOT}/ref-impl/include/OM
    ${AAFSDK_ROOT}/ref-impl/src/OM
)

target_include_directories(OM PRIVATE
    ${AAFSDK_ROOT}/ref-impl/include
    ${AAFSDK_ROOT}/ref-impl/include/ref-api
    # Required with OM_USE_SCHEMASOFT_SS
    ${AAFSDK_ROOT}/sss-impl/include
    # HACK (see OMStructuredStorage.h): Required with OM_USE_SCHEMASOFT_SS and OM_USE_GSF_SS
    ${AAFSDK_ROOT}/ss-impl/ref
    # AAF-XML stored format support requires the expat library which is bundled with the AAF SDK.
    ${AAFSDK_ROOT}/ref-impl/expat
)

target_compile_definitions(OM PUBLIC
    XML_STATIC
    $<$<CONFIG:Debug>:OM_DEBUG>
    $<$<CONFIG:Debug>:OM_STACK_TRACE_ON_ASSERT>
)

if(NOT AAF_NO_STRUCTURED_STORAGE)
    target_compile_definitions(OM PUBLIC OM_STRUCTURED_STORAGE)
    if(WIN32)
        target_compile_definitions(OM PUBLIC OM_USE_SCHEMASOFT_SS OM_USE_WINDOWS_SS OM_USE_STORAGE_EX)
    else()
        target_compile_definitions(OM PUBLIC OM_USE_SCHEMASOFT_SS)
    endif()
else()
    target_compile_definitions(OM PUBLIC OM_NO_STRUCTURED_STORAGE)
endif()

set_target_properties(OM PROPERTIES
    ARCHIVE_OUTPUT_DIRECTORY ${TARGET_DIR}
    ARCHIVE_OUTPUT_DIRECTORY_DEBUG ${TARGET_DIR}
    ARCHIVE_OUTPUT_DIRECTORY_RELEASE ${TARGET_DIR}
)

if(NOT MSVC)
    set_target_properties(OM PROPERTIES
        OUTPUT_NAME "om"
        OUTPUT_NAME_DEBUG "om"
        OUTPUT_NAME_RELEASE "om"
    )
endif()
