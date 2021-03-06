* Please follow the template we introduced in NOVEMBER.md file.
* Every parser need to be added under the corresponding feature.

| Module                  | Version       |
| ------------------------|:-------------:|
| ``genie.libs.parser``   |               |

--------------------------------------------------------------------------------
                                New
--------------------------------------------------------------------------------
* JUNOS
    * Created ShowMPLSLSPNameDetail
        * show mpls lsp name {name} detail
    * Show Ospf3 Route Network Extensive
        * Created ShowOspf3RouteNetworkExtensive
    * Added ShowBFDSesssion
        * show bfd session
    * Added ShowBFDSesssionDetail
        * show bfd session {ipaddress} detail
    * Added ShowLDPSession
        * show ldp session
    * Added ShowClassOfService
        * show class-of-service interface {interface}
    * Added ShowRouteForwardingTableLabel
        * show route forwarding-table label {label}
    * Added ShowRSVPSession
        * show rsvp session
    * Added ShowRSVPNeighbor
        * show rsvp neighbor
    * Added ShowRSVPNeighborDetail
        * show rsvp neighbor detail


--------------------------------------------------------------------------------
                                Fix
--------------------------------------------------------------------------------
* JUNOS
    * Updated ShowOspfDatabaseAdvertisingRouterSelfDetail
        * Added more keys to the schema, in order to support output of ShowOspfDatabaseLsaidDetail
    * Updated ShowSystemUsers
        * Regex issues resolved
    * Updated ShowOspfOverview
        * Optional key issue resolved
    * Updated ShowInterfaceExtensive
        * No longer breaks on use and previously unused data is now used
    * Updated ShowOspfDatabaseExtensiveSchema
        * Optional key issue resolved
    * Updated ShowOspf3DatabaseExtensiveSchema
        * Optional key issue resolved
    * Updated ShowOspfVrfAllInclusive
        * key error resolved
    * Updated ShowOspfDatabaseLsaidDetail
        * Resolved issue where empty output would cause error
    * Updated ShowOspf3DatabaseExtensive
        * Missing key issue resolved
    * Updated ShowOspf3Database
        * List ospf-area
    * Updated ShowOspfDatabaseExtensiveSchema
        * Modified ShowOspfDatabaseExtensiveSchema to have optional keys
        * Missing key added
    * Updated ShowOspf3Overview
        * Missing key added
    * Updated ShowSystemUptime
        * Fixed optional key error, improved regex, and fixed return results
    * Updated ShowInterfaces
        * Optional key issue resolved
        * Regex modified to support more output
        * 'show interfaces extensive {interface}' changed to 'show interfaces {interface} extensive'
* IOSXE
    * Updated ShowCdpNeighbors
        * Modified regex to support different output
    * Updated ShowCdpNeighborsDetail
        * Modified regex to support different output
    * Updated ShowIpInterface
        * Enhanced parser and added optional values
    * Updated ShowPlatformIntegrity
        * to pretty print the rpc reply for netconf

* NXOS
    * Updated ShowIpRoute
        * Enhanced parser

* IOSXR
    * Updated ShowOspfVrfAllInclusiveDatabaseOpaqueArea
        * Enhanced parser
    * Updated ShowIsisSpfLogDetail:
        * Added more regex patterns to support various outputs.
    * Updated ShowIsisInterface:
        * Modified to support default as instance name
    * Updated ShowInterfaces:
        * Added more regex patterns to support various outputs.