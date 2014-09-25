|Logo XML Travelgate|

`api docs </Docs/API-Specification/Main.html>`__

XML Travelgate Hotel API
========================

--------------

Table Of Contents
-----------------

#. `Change Log <#Change%20Log>`__
#. `Intro <#Intro>`__
#. `Audience <#Audience>`__
#. `Document Goals <#Document%20Goals>`__
#. `Service Endpoints <#Service%20Endpoints>`__
#. `Hotel FAQ </Wiki/0/hotel-faq>`__ (**soon**)
#. `Anatomy of a Request <#Anatomy%20of%20a%20Request>`__ Anatomy of a
   Request
#. `General Structure <#General%20Structure>`__

   #. `Data Structure <#Data%20Structure>`__

      #. `Common Elements <#Common%20Elements>`__

         #. `Common Elements RQ
            Example <#Common%20Elements%20RQ%20Example>`__
         #. `Common Elements RQ
            Description <#Common%20Elements%20RQ%20Description>`__
         #. `Common Elements RS
            Example <#Common%20Elements%20RS%20Example>`__
         #. `Common Elements RS
            Description <#Common%20Elements%20RS%20Description>`__

      #. *`Avail <#Avail>`__* (Availability)

         #. `Avail RQ Example <#Avail%20RQ%20Example>`__
         #. `Avail RQ Description <#Avail%20RQ%20Description>`__
         #. `Avail RS Example <#Avail%20RS%20Example>`__
         #. `Avail RS Description <#Avail%20RS%20Description>`__

      #. *`Valuation <#Valuation>`__* (Pre-Booking)

         #. `Valuation RQ Example <#Valuation%20RQ%20Example>`__
         #. `Valuation RQ Description <#Valuation%20RQ%20Description>`__
         #. `Valuation RS Example <#Valuation%20RS%20Example>`__
         #. `Valuation RS Description <#Valuation%20RS%20Description>`__

      #. *`Reservation <#Reservation>`__* (Booking)

         #. `Reservation RQ Example <#Reservation%20RQ%20Example>`__
         #. `Reservation RQ
            Description <#Reservation%20RQ%20Description>`__
         #. `Reservation RS Example <#Reservation%20RS%20Example>`__
         #. `Reservation RS
            Description <#Reservation%20RS%20Description>`__

      #. *`ReservationRead <#ReservationRead>`__* (Booking Details)

         #. `ReservationRead RQ
            Example <#ReservationRead%20RQ%20Example>`__
         #. `ReservationRead RQ
            Description <#ReservationRead%20RQ%20Description>`__
         #. `ReservationRead RS
            Example <#ReservationRead%20RS%20Example>`__
         #. `ReservationRead RS
            Description <#ReservationRead%20RS%20Description>`__

      #. *`ReservationList <#ReservationList>`__* (Booking List)

         #. `ReservationList RQ
            Example <#ReservationList%20RQ%20Example>`__
         #. `ReservationList RQ
            Description <#ReservationList%20RQ%20Description>`__
         #. `ReservationList RS
            Example <#ReservationList%20RS%20Example>`__
         #. `ReservationList RS
            Description <#ReservationList%20RS%20Description>`__

      #. *`Cancel <#Cancel>`__* (Booking Cancellation)

         #. `Cancel RQ Example <#Cancel%20RQ%20Example>`__
         #. `Cancel RQ Description <#Cancel%20RQ%20Description>`__
         #. `Cancel RS Example <#Cancel%20RS%20Example>`__
         #. `Cancel RS Description <#Cancel%20RS%20Description>`__

      #. *`HotelList <#HotelList>`__* (Hotel List)

         #. `HotelList RQ Example <#HotelList%20RQ%20Example>`__
         #. `HotelList RQ Description <#HotelList%20RQ%20Description>`__
         #. `HotelList RS Example <#HotelList%20RS%20Example>`__
         #. `HotelList RS Description <#HotelList%20RS%20Description>`__

      #. *`DescriptiveInfo <#DescriptiveInfo>`__* (Hotel Details)

         #. `DescriptiveInfo RQ
            Example <#DescriptiveInfo%20RQ%20Example>`__
         #. `IDescriptiveInfo RQ
            Description <#IDescriptiveInfo%20RQ%20Description>`__
         #. `DescriptiveInfo RS
            Example <#DescriptiveInfo%20RS%20Example>`__
         #. `DescriptiveInfo RS
            Description <#DescriptiveInfo%20RS%20Description>`__

      #. *`AvailDestinationTree <#AvailDestinationTree>`__*
         (Destinations Tree of Availability)

         #. `AvailDestinationTree RQ
            Example <#AvailDestinationTree%20RQ%20Example>`__
         #. `AvailDestinationTree RQ
            Description <#AvailDestinationTree%20RQ%20Description>`__
         #. `AvailDestinationTree RS
            Example <#AvailDestinationTree%20RS%20Example>`__
         #. `AvailDestinationTree RS
            Description <#AvailDestinationTree%20RS%20Description>`__

      #. *`GeographicDestinationTree <#GeographicDestinationTree>`__*
         (Geographic Destinations Tree)

         #. `GeographicDestinationTree RQ
            Example <#GeographicDestinationTree%20RQ%20Example>`__
         #. `GeographicDestinationTree RQ
            Description <#GeographicDestinationTree%20RQ%20Description>`__
         #. `GeographicDestinationTree RS
            Example <#GeographicDestinationTree%20RS%20Example>`__
         #. `GeographicDestinationTree RS
            Description <#GeographicDestinationTree%20RS%20Description>`__

      #. *`MealPlanList <#MealPlanList>`__* (Mealplan List)

         #. `MealPlanList RQ Example <#MealPlanList%20RQ%20Example>`__
         #. `MealPlanList RQ
            Description <#MealPlanList%20RQ%20Description>`__
         #. `MealPlanList RS Example <#MealPlanList%20RS%20Example>`__
         #. `MealPlanList RS
            Description <#MealPlanList%20RS%20Description>`__

      #. *`CategoryList <#CategoryList>`__* (Hotel Category List)

         #. `CategoryList RQ Example <#CategoryList%20RQ%20Example>`__
         #. `CategoryList RQ
            Description <#CategoryList%20RQ%20Description>`__
         #. `CategoryList RS Example <#CategoryList%20RS%20Example>`__
         #. `CategoryList RS
            Description <#CategoryList%20RS%20Description>`__

      #. *`RoomList <#RoomList>`__* (Room Type List)

         #. `RoomList RQ Example <#RoomList%20RQ%20Example>`__
         #. `RoomList RQ Description <#RoomList%20RQ%20Description>`__
         #. `RoomList RS Example <#RoomList%20RS%20Example>`__
         #. `RoomList RS Description <#RoomList%20RS%20Description>`__

      #. *`StaticConfiguration <#StaticConfiguration>`__* (Static
         Configuration)

         #. `StaticConfiguration RQ
            Example <#StaticConfiguration%20RQ%20Example>`__
         #. `StaticConfiguration RQ
            Description <#StaticConfiguration%20RQ%20Description>`__
         #. `StaticConfiguration RS
            Example <#StaticConfiguration%20RS%20Example>`__
         #. `StaticConfiguration RS
            Description <#StaticConfiguration%20RS%20Description>`__

      #. *`RuntimeConfiguration <#RuntimeConfiguration>`__* (RunTime
         Configuration)

         #. `RuntimeConfiguration RQ
            Example <#RuntimeConfiguration%20RQ%20Example>`__
         #. `RuntimeConfiguration RQ
            Description <#RuntimeConfiguration%20RQ%20Description>`__
         #. `RuntimeConfiguration RS
            Example <#RuntimeConfiguration%20RS%20Example>`__
         #. `RuntimeConfiguration RS
            Description <#RuntimeConfiguration%20RS%20Description>`__

      #. *`ModifyValuation <#ModifyValuation>`__* (Modify Valuation)

         #. `ModifyValuation RQ
            Example <#ModifyValuation%20RQ%20Example>`__
         #. `ModifyValuation RQ
            Description <#ModifyValuation%20RQ%20Description>`__
         #. `ModifyValuation RS
            Example <#ModifyValuation%20RS%20Example>`__
         #. `ModifyValuation RS
            Description <#ModifyValuation%20RS%20Description>`__

      #. *`ModifyReservation <#ModifyReservation>`__*
         (ModifyReservation)

         #. `ModifyReservation RQ
            Example <#ModifyReservation%20RQ%20Example>`__
         #. `ModifyReservation RQ
            Description <#ModifyReservation%20RQ%20Description>`__
         #. `ModifyReservation RS
            Example <#ModifyReservation%20RS%20Example>`__
         #. `ModifyReservation RS
            Description <#ModifyReservation%20RS%20Description>`__

--------------

Change Log
----------

Version 1.0.1

Date 11/01/2012

-  Specified Common Elements
-  Added Appendices

| 

Version 1.0.2

Date 20/02/2012

-  AvailDestinationTree specified destinations only attackable on
   availability
-  Added ISO country code in response Hotel

| 

Version 1.0.3

Date 09/04/2012

-  New type errors in Valuation

| 

Version 1.0.4

Date 13/06/2012

-  Larger PDI structure to charge hotel + ticket
-  Add ProveedorFacturacionExterna in confirmacionRS

| 

Version 1.0.5

Date 30/07/2012

-  Correcting errors in the documentation
-  Add Promotions / Specials Offers in disponibilidadRS option

| 

Version 1.0.6

Date 30/08/2012

-  Implemented three new calls: ReservationList, RuntimeConfigurationand
   StaticConfiguration
-  Added attribute element level NuevaOpcion Offer
-  Appendix of countries and currencies

| 

Version 1.0.7

Date 11/03/2013

-  Product specification download
-  Added element geographical destination in hotel
-  Implemented new call: GeographicDestinationTree

| 

Version 1.0.8

Date 17/03/2014

-  `Bed information in
   AvailRS <http://www.xmltravelgate.com/Wiki/1517#Beds%20information%20in%20AvailRS>`__

| 

Version 1.0.9

Date 27/03/2014

-  `Modify
   booking <http://www.xmltravelgate.com/Wiki/1517#Modify%20Booking>`__

`toc <#toc>`__

--------------

XML Travelgate Hotel API
------------------------

| The XML Travelgate Hotel API allows clients to access content from XL
Travelgate's inventory of partners. Currently there are more than 70
providers sources including switching platforms and hotel chains. Use
this API to query, check for availability and book fares. It can be
accessed by any third-party system such as tour-operator systems, B2C
and B2B web applications or third-party applications. Scaleability is
not an issue. Our systems are used to heavy load and monitored 24x7.
| `toc <#toc>`__

--------------

Audience
--------

| This document is intended to a technical audience. Prior knowledge of
XML is required.
| Although it is recommended to have prior knowledge of XML integrations
with airlines, ferries or railway carriers, it is not necessary.
| `toc <#toc>`__

--------------

Document Goals
--------------

| This document aims to explain all aspects of **XML Travelgate**'s
Hotel API specification. In the next pages you can find detailed
explanation of all Nodes, Elements and Attributes of every aspect of the
API specification.
| It uses a very straight forward nomenclature that tries to define
every aspect of the specification by the name.
| This documentation follows a standard. For every method there is:

#. Method Description

   #. Method Goals: What does it do, how does it do it?
   #. Request Format: General information on how is the request is
      formed.
   #. Response Format: General information on how is the response is
      returned.
   #. Remarks: Any remark / explanation about this method

#. Example Request

   #. Full explanation of all nodes, elements and attributes

#. Example Response

   #. Full explanation of all nodes, elements and attributes

| 
| Every method, element, attribute or node name is in *italic*.
| 
| For any questions or comments please send an email to
hotel@xmltravelgate.com
| `toc <#toc>`__

--------------

Service Endpoints
-----------------

| Service Endpoints, WSDLs and XML schemas describing the request and
response XML structures can be found in:

-  Service Definitions:
   `http://www.xmltravelgate.com/Docs/API-Specification/Hub.html#Service%20Endpoints <http://www.xmltravelgate.com/Docs/API-Specification/Hub.html#Service%20Endpoints>`__

Each request **must** be sent to the service url.
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

`toc <#toc>`__

--------------

Anatomy of a Request
--------------------

| Requests to the Service URL are explained in detail
`here <http://www.xmltravelgate.com/Docs/API-Specification/Hub.html>`__
| `toc <#toc>`__

--------------

General Structure
-----------------

| The structure of the API specification follows a standard. This
document intends to explain every aspect of this structure and their
fields.
| The integration will have the following methods:

+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+
| Method                                                       | Input                         | Output                        | Required   | Description                                  |
+==============================================================+===============================+===============================+============+==============================================+
| `AvailDestinationTree <#AvailDestinationTree>`__             | AvailDestinationTreeRQ        | AvailDestinationTreeRS        | No         | Returns a tree of available destinations     |
+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+
| `GeographicDestinationTree <#GeographicDestinationTree>`__   | GeographicDestinationTreeRQ   | GeographicDestinationTreeRS   | Yes        | Returns a tree of provider destinations      |
+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+
| `HotelList <#HotelList>`__                                   | HotelListRQ                   | HotelListRS                   | Yes        | Returns a list of available hotels           |
+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+
| `DescriptiveInfo <#DescriptiveInfo>`__                       | DescriptiveInfoRQ             | DescriptiveInfoRS             | Yes        | Returns hotel information per hotel          |
+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+
| `RoomList <#RoomList>`__                                     | RoomListRQ                    | RoomListRS                    | No         | Returns available room types                 |
+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+
| `MealPlanList <#MealPlanList>`__                             | MealPlanListRQ                | MealPlanListRS                | Yes        | Returns a list of available boards           |
+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+
| `CategoryList <#CategoryList>`__                             | CategoryListRQ                | CategoryListRS                | Yes        | Returns a list of available categories       |
+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+
| `Avail <#Avail>`__                                           | AvailRQ                       | AvailRS                       | Yes        | Makes an availability call                   |
+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+
| `Valuation <#Valuation>`__                                   | ValuationRQ                   | ValuationRS                   | Yes        | Gets a booking quote (pre-book)              |
+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+
| `Reservation <#Reservation>`__                               | ReservationRQ                 | ReservationRS                 | Yes        | Makes a booking                              |
+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+
| `Cancel <#Cancel>`__                                         | CancelRQ                      | CancelRS                      | No         | Cancels a booking                            |
+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+
| `ReservationRead <#ReservationRead>`__                       | ReservationReadRQ             | ReservationReadRS             | No         | Gets booking details                         |
+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+
| `ReservationList <#ReservationList>`__                       | ReservationListRQ             | ReservationListRS             | No         | Gets a list of bookings                      |
+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+
| `RuntimeConfiguration <#RuntimeConfiguration>`__             | RuntimeConfigurationRQ        | RuntimeConfigurationRS        | Yes        | Gets the provider's run-time configuration   |
+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+
| `StaticConfiguration <#StaticConfiguration>`__               | StaticConfigurationRQ         | StaticConfigurationRS         | Yes        | Gets the provider's static configuration     |
+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+
| `ModifyValuation <#ModifyValuation>`__                       | ModifyValuationRQ             | ModifyValuationRS             | No         | Valuation a possible booking modification    |
+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+
| `ModifyReservation <#ModifyReservation>`__                   | ModifyReservationRQ           | ModifyReservationRS           | No         | Confirm a booking modification               |
+--------------------------------------------------------------+-------------------------------+-------------------------------+------------+----------------------------------------------+

| 
| Each request sent to the **service url** requires a node called
*rqXML*. Inside this node travels the current method's Input object.
| `toc <#toc>`__

--------------

Data Structure
~~~~~~~~~~~~~~

| The data structure will always have common elements in all objects and
the specific objects related to the operation
| `toc <#toc>`__

--------------

Common Elements
^^^^^^^^^^^^^^^

| This node will be in every request and response objects.
| The request objects contains the provider's configuration, urls and
credentials.
| The response object contains the operation status and errors if any.
| `toc <#toc>`__

--------------

| 

Common Elements RQ Example
''''''''''''''''''''''''''

::

    <HotelBaseRQ>
        <echoToken>TEST</echoToken>
        <timeoutMilliseconds>20000</timeoutMilliseconds>
        <source>
            <agencyCode>XXXX</agencyCode>
            <languageCode>es</languageCode>
        </source>
        <filterAuditData>
            <registerTransactions>True</registerTransactions>
        </filterAuditData>
        <Configuration>
            <User>USERXX</User>
            <Password>PWXX</Password>
            <UrlAvail>www.proveedor.es/avail</UrlAvail>
            <UrlReservation>www.proveedor.es/reservation</UrlReservation>
            <UrlValuation>www.proveedor.es/valuation</UrlValuation>
            <UrlGeneric>www.proveedor.es</UrlGeneric>
            <Parameters>
                <Parameter key = "SegundoPW" value = "PWXML"/>
            </Parameters>
        </Configuration>
        …
    </HotelBaseRQ>

| 
| `toc <#toc>`__

--------------

Common Elements RQ Description
''''''''''''''''''''''''''''''

| 

+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| Element                                | Number   | Type      | Description                                                          |
+========================================+==========+===========+======================================================================+
| HotelBaseRQ                            | 1        |           | Root node.                                                           |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| echoToken                              | 0..1     | String    | Echo token to be returned in response (valid for test purposes).     |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| timeoutMillisencods                    | 1        | Integer   | Timeout in milliseconds that client will be waiting that response.   |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| source                                 | 1        |           | Information about source requesting the operation.                   |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| source/agencyCode                      | 0..1     | String    | Agency code that requests the operation.                             |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| source/languageCode                    | 1        | String    | Language code (ISO 3166-1 alpha-2) format.                           |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| filterAuditData                        | 1        |           | Enables or disables information returned in audit data.              |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| filterAuditData/registerTransactions   | 1        | Boolean   | Returns all the transactions (XMLs) exchanged with the provider.     |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| Configuration                          | 1        |           | Information about source requesting the operation.                   |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| Configuration/User                     | 0..1     | String    | User code for connection.                                            |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| Configuration/Password                 | 0..1     | String    | Password for the connection.                                         |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| Configuration/UrlGeneric               | 0..1     | String    | Url generic connection.                                              |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| Configuration/UrlAvail                 | 0..1     | String    | Url for Avail method.                                                |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| Configuration/UrlValuation             | 0..1     | String    | Url for Valuation method.                                            |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| Configuration/UrlReservation           | 0..1     | String    | Url for Reservation method.                                          |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| Configuration/Parameters               | 0..1     |           | Parameters for additional information.                               |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| Configuration/Parameters/Parameter     | 0..n     |           | List of parameter.                                                   |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| *@key*                                 | 1        | String    | Contains the keyword/Id to identify a parameter.                     |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+
| *@value*                               | 1        | String    | Contains the value of the parameter                                  |
+----------------------------------------+----------+-----------+----------------------------------------------------------------------+

| 
| `toc <#toc>`__

--------------

Common Elements RS Example
''''''''''''''''''''''''''

::

    <HotelBaseRS>
        <echoToken>TEST</echoToken>
        <OperationImplemented>true</OperationImplemented>
        <applicationErrors>
            <type>102</type>
            <code>xxx</code>
            <description>xxx</description>
        </applicationErrors>
        …
        <auditData>
            <transactions>
                <timeStamp>2011-10-6T15:19:45.3544495+02:00</timeStamp>
                <RQ/>
                <RS/>
            </transactions>
            …
            <timeStamp>2011-10-26T15:19:43.4014745+02:00</timeStamp>
            <processTimeMilliseconds>19532</processTimeMilliseconds>
        </auditData>
        …
    </HotelBaseRS>

| 
| `toc <#toc>`__

--------------

Common Elements RS Description
''''''''''''''''''''''''''''''

| 

+-------------------------------------+----------+-----------+--------------------------------------------------------------------+
| Element                             | Number   | Type      | Description                                                        |
+=====================================+==========+===========+====================================================================+
| HotelBaseRS                         | 1        |           | Root node.                                                         |
+-------------------------------------+----------+-----------+--------------------------------------------------------------------+
| echoToken                           | 0..1     | String    | Echo token to be returned in response (valid for test purposes).   |
+-------------------------------------+----------+-----------+--------------------------------------------------------------------+
| OperationImplemented                | 1        | Boolean   | If the operation is implemented by this provider or not.           |
+-------------------------------------+----------+-----------+--------------------------------------------------------------------+
| applicationErrors                   | 0..n     |           | Application errors reported by provider.                           |
+-------------------------------------+----------+-----------+--------------------------------------------------------------------+
| applicationErrors/type              | 1        | String    | Error Type as specified by XML Travelgate.                         |
+-------------------------------------+----------+-----------+--------------------------------------------------------------------+
| applicationErrors/code              | 1        | String    | Native error code reported by provider.                            |
+-------------------------------------+----------+-----------+--------------------------------------------------------------------+
| applicationErrors/description       | 1        | String    | Error description.                                                 |
+-------------------------------------+----------+-----------+--------------------------------------------------------------------+
| auditData                           | 1        |           | Information about processing that transaction.                     |
+-------------------------------------+----------+-----------+--------------------------------------------------------------------+
| auditData/transactions              | 0..n     |           | List of transactions communicated with provider.                   |
+-------------------------------------+----------+-----------+--------------------------------------------------------------------+
| auditData/transactions/timeStamp    | 1        | Integer   | TimeStamp in which has been generated that transaction.            |
+-------------------------------------+----------+-----------+--------------------------------------------------------------------+
| auditData/transactions/RQ           | 1        | String    | Transaction Request.                                               |
+-------------------------------------+----------+-----------+--------------------------------------------------------------------+
| auditData/transactions/RS           | 1        | String    | Transaction Response.                                              |
+-------------------------------------+----------+-----------+--------------------------------------------------------------------+
| auditData/timeStamp                 | 1        | Integer   | imeStamp in which response has been generated                      |
+-------------------------------------+----------+-----------+--------------------------------------------------------------------+
| auditData/processTimeMilliseconds   | 1        | Integer   | Time in milliseconds consumed by this method.                      |
+-------------------------------------+----------+-----------+--------------------------------------------------------------------+

| 
| `toc <#toc>`__

--------------

| 

*Avail* (Availability)
^^^^^^^^^^^^^^^^^^^^^^

Method Goals

| 
| This method aims to return all the available options for a given date
and itinerary. It does not filter different classes, times or fares. It
will always return all results returned by the provider.

Request Format

| 
| The availability request is very straight forward. It only requires
the destination, the traveling dates and the paxes of the rooms.

Response Format

| 
| Results are organized in this hierarchy:

-  *Hotel* :

| A list with all the hotels, including the name and code hotel,
*mealplans* list, etc returned by the provider.

-  *Mealplans* :

| A list of all MealPlans returned by the provider, every *mealplan*
including the mealplan's code. Every *mealplan* also contains a list of
the *options* for this availability.

-  *Options* :

| A list with all the *options* returned for each mealplan, every
*option* includes the total price, conditions and description each room.
| The price returned should be "all inclusive". All fares, taxes and
discounts are already included in the total price.

Remarks

| 
| This method **must** be called **before** the *Valuation* method.
| **Price, binding price and commission**:

-  If commission = 0. The price returned is a net price, and the
   provider is informing that the commission **must** be 0.

-  If commission = -1. The provider is not informing if the price is net
   or sale price. This information is informed when signing with the
   provider or with the binding price is true/false)

-  When commission is greater than 0, for example: commission = 12, it
   is a sale price, and this commission is informed for the provider (
   this price is mandatory depends if binding price is true /false).

| 
| `toc <#toc>`__

--------------

*AvailRQ* Example
'''''''''''''''''

::

    <AvailRQ>
        <CancellationPolicies>false</CancellationPolicies>
        <AvailDestinations>
            <Destination type = "CTY" code = "5"/>
        </AvailDestinations>
        <StartDate>28/01/2014</StartDate>
        <EndDate>29/01/2014</EndDate>
        <Currency>EUR</Currency>
        <RoomCandidates>
            <RoomCandidate id = "1">
                <Paxes>
                    <Pax age = "30" id = "1"/>
                    <Pax age = "30" id = "2"/>
                </Paxes>
            </RoomCandidate>
        </RoomCandidates>
    </AvailRQ>

| 
| `toc <#toc>`__

--------------

*AvailRQ* Description
'''''''''''''''''''''

+------------------------------------------+----------+-----------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| Element                                  | Number   | Type      | Description                                                                                                                                         |
+==========================================+==========+===========+=====================================================================================================================================================+
| AvailRQ                                  | 1        |           | Root node.                                                                                                                                          |
+------------------------------------------+----------+-----------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| CancellationPolicies                     | 1        | Boolean   | Indicates if you want to receive the cancellation policies in AvailRS, as long as the provider returns it in this call (see StaticConfiguration).   |
+------------------------------------------+----------+-----------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| AvailDestinations/Destination            | 0..n     |           | Contains the list of destinations filters ( hotels or cities or zones or geocodes).                                                                 |
+------------------------------------------+----------+-----------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| *@type*                                  | 1        | String    | Destination type ( HOT, CTY, ZON, GEO).                                                                                                             |
+------------------------------------------+----------+-----------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| *@code*                                  | 1        | String    | Native destination code as returned by provider in *HotelList* or *AvailDestinationTree*.                                                           |
+------------------------------------------+----------+-----------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| StartDate                                | 1        | String    | Start date to search rates.                                                                                                                         |
+------------------------------------------+----------+-----------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| EndDate                                  | 1        | String    | End date to search rates.                                                                                                                           |
+------------------------------------------+----------+-----------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| Currency                                 | 1        | String    | Currency value.                                                                                                                                     |
+------------------------------------------+----------+-----------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| RoomCandidates/RoomCandidate             | 1..n     |           | Room required.                                                                                                                                      |
+------------------------------------------+----------+-----------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| *@id*                                    | 1        | Integer   | Id of the requested room (starting at 1).                                                                                                           |
+------------------------------------------+----------+-----------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| RoomCandidates/RoomCandidate/Paxes/Pax   | 1..n     |           | Pax required.                                                                                                                                       |
+------------------------------------------+----------+-----------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| *@age*                                   | 1        | Integer   | Passenger age.                                                                                                                                      |
+------------------------------------------+----------+-----------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| *@id*                                    | 1        | Integer   | Passenger id (starting at 1).                                                                                                                       |
+------------------------------------------+----------+-----------+-----------------------------------------------------------------------------------------------------------------------------------------------------+

| 
| `toc <#toc>`__

--------------

*AvailRS* Example
'''''''''''''''''

::

    <AvailRS xmlns:xsd = "http://www.w3.org/2001/XMLSchema" xmlns:xsi = "http://www.w3.org/2001/XMLSchema-instance">
        <Hotels>
            <Hotel code = "10" name = "LEO">
                <MealPlans>
                    <MealPlan code = "D">
                        <Options>
                            <Option type = "Hotel" paymentType = "MerchantPay" status = "OK">
                                <Rooms>
                                    <Room id = "4582" roomCandidateRefId = "1" code = "506" description = "Doble Standard..">
                                        <Price currency = "EUR" amount = "36.20" binding = "false" commission = "-1"/>
                                    </Room>
                                </Rooms>
                                <Price currency = "EUR" amount = "36.20" binding = "false" commission = "-1" />
                            </Option>
                        </Options>
                    </MealPlan>
                    <MealPlan code = "M">
                        <Options>
                            <Option type = "Hotel" paymentType = "MerchantPay" status = "OK">
                                <Rooms>
                                    <Room id = "4582" roomCandidateRefId = "1" code = "506" description = "Doble Standard..">
                                        <Price currency = "EUR" amount = "42.90" binding = "false" commission = "-1"/>
                                    </Room>
                                </Rooms>
                                <Price currency = "EUR" amount = "42.90" binding = "false" commission = "-1"/>
                            </Option>
                        </Options>
                           ...
                    </MealPlan>
                    <MealPlan code = "MP">
                        <Options>
                            <Option type = "HotelSkiPass" paymentType = "MerchantPay" status = "OK">
                                <Rooms>
                                    <Room id = "4145" roomCandidateRefId = "1" code = "DBL#STAND" description = "Doble Standard">
                                        <Price currency = "EUR" amount = "636.80" binding = "false" commission = "-1"/>
                                    </Room>
                                </Rooms>
                                <Detail>
                                    <POIs>
                                        <POI code = "8A" Description = "Andorra">
                                            <Services>
                                                <Service type = "SkiPass" code = "F1" description = "Forfait" durationType = "Range" quantity = "0" unit = "Day">
                                                    <RangeDates startDate = "28/01/2014" endDate = "29/01/2014"/>
                                                </Service>
                                            </Services>
                                        </POI>
                                    </POIs>
                                </Detail>
                                <Price currency = "EUR" amount = "636.80" binding = "false" commission = "-1"/>
                                <Parameters>
                                    <Parameter key = "sesion" value = "888de014"/>
                                </Parameters>
                            </Option>
                        </Options>
                    </MealPlan>
                    ...
                </MealPlans>
            </Hotel>
            ...
        </Hotels>
    </AvailRS>

| 
| `toc <#toc>`__

--------------

*AvailRS* Description
'''''''''''''''''''''

+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Element                                                                         | Number   | Type      | Description                                                                                                                                                                                                       |
+=================================================================================+==========+===========+===================================================================================================================================================================================================================+
| AvailRS/Hotels/Hotel                                                            | 0..n     |           | Root node.                                                                                                                                                                                                        |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@code*                                                                         | 1        | String    | Hotel code.                                                                                                                                                                                                       |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@name*                                                                         | 0..1     | String    | Hotel name.                                                                                                                                                                                                       |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans                                                                       | 1        |           | Meal plans of this hotel.                                                                                                                                                                                         |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan                                                              | 1..n     |           | List of meal type classification.                                                                                                                                                                                 |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@code*                                                                         | 1        | String    | MealPlan code.                                                                                                                                                                                                    |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options                                                      | 1        |           | Options ( list option).                                                                                                                                                                                           |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option                                               | 1..n     |           | Detail of option.                                                                                                                                                                                                 |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@type*                                                                         | 1        | String    | Indicates the type of option (only hotel, hotel with ski pass, hotel with entrance...).                                                                                                                           |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@paymentType*                                                                  | 1        | String    | Indicates the typology of payment (Merchant, Direct ...) .                                                                                                                                                        |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@status*                                                                       | 1        | String    | Status option (OK = available, RQ = on request).                                                                                                                                                                  |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option/Parameters                                    | 0..1     |           | Additional parameters that must be reported on the ValuationRQ.Parameters, if this option is required                                                                                                             |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option/Parameters/Parameter                          | 0..n     |           | Additional parameter that requires the integration                                                                                                                                                                |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@key*                                                                          | 1        | String    | Contains the keyword/Id to identify a parameter.                                                                                                                                                                  |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@value*                                                                        | 1        | String    | Contains the value of the parameter                                                                                                                                                                               |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option/RateRules                                     | 0..1     |           | Restrictions of this option                                                                                                                                                                                       |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option/RateRules/Rules                               | 0..1     |           | Rules                                                                                                                                                                                                             |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option/RateRules/Rules/Rule                          | 1..n     |           | Rule                                                                                                                                                                                                              |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@type*                                                                         | 1        | String    | Values that can take (NonRefundable, Older55, Package)                                                                                                                                                            |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option/Rooms                                         | 1        |           | Rooms of this option ( room list).                                                                                                                                                                                |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option/Rooms/Room                                    | 1..n     |           | Detail of room.                                                                                                                                                                                                   |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@id*                                                                           | 1        | String    | Identifier of the room.                                                                                                                                                                                           |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@roomCandidateRefId*                                                           | 1        | Integer   | Identifier of room candidate.                                                                                                                                                                                     |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@code*                                                                         | 1        | String    | Room code.                                                                                                                                                                                                        |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@description*                                                                  | 1        | String    | Room description.                                                                                                                                                                                                 |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option/Rooms/Room/Price                              | 1        |           | Room price.                                                                                                                                                                                                       |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@currency*                                                                     | 1        | String    | Currency code.                                                                                                                                                                                                    |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@amount*                                                                       | 1        | Decimal   | Room Amount.                                                                                                                                                                                                      |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@binding*                                                                      | 1        | Boolean   | Identifies if is the price is binding ( When true the sale price returned **must** not be less than the price informed.                                                                                           |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@commission*                                                                   | 1        | Decimal   | Commission ( -1 = not specified (will come indicated with the provider contract ), 0 = net price, X = % of the commission that applies to the amount.                                                             |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option/Price                                         | 1        |           | Option price ( it is the total price of option).                                                                                                                                                                  |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@currency*                                                                     | 1        | String    | Currency code.                                                                                                                                                                                                    |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@amount*                                                                       | 1        | Decimal   | Option Amount.                                                                                                                                                                                                    |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@binding*                                                                      | 1        | Boolean   | Identifies if is the price is binding ( When true the sale price returned **must** not be less than the price informed.                                                                                           |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@commission*                                                                   | 1        | Decimal   | Commission ( -1 = not specified (will come indicated with the provider contract ), 0 = net price, X = % of the commission that applies to the amount.                                                             |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option/Detail                                        | 0..1     |           | Detail of option (it is indicated if the option is different from the type<> Hotel).                                                                                                                              |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option/Detail/POIs                                   | 1        |           | Points of interest.                                                                                                                                                                                               |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option/Detail/POIs/POI                               | 1..n     |           | Point of interest.                                                                                                                                                                                                |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@code*                                                                         | 1        | String    | POI code.                                                                                                                                                                                                         |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@description*                                                                  | 1        | String    | POI description.                                                                                                                                                                                                  |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option/Detail/POIs/POI/Services                      | 1        |           | Services that contains this POI.                                                                                                                                                                                  |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option/Detail/POIs/POI/Services/Service              | 1..n     |           | Service detail.                                                                                                                                                                                                   |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@type*                                                                         | 1        | String    | Service typification (SkiPass, Lessons, Meals, Equipment, Ticket, Transfers or Gala).                                                                                                                             |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@code*                                                                         | 1        | String    | Service code.                                                                                                                                                                                                     |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@description*                                                                  | 1        | String    | Service description.                                                                                                                                                                                              |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@durationType*                                                                 | 1        | String    | Type of duration (Range= date range specified will come "RangeDates" element, Open= indicates a duration not restricted by date, quantity and typology of the elements are indicated in "quantity" and "unit").   |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@quantity*                                                                     | 1        | Integer   | Indicate the quantity of field in the element "unit".                                                                                                                                                             |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@unit*                                                                         | 0..1     | String    | Day or Hour.                                                                                                                                                                                                      |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option/Detail/POIs/POI/Services/Service/RangeDates   | 0..1     |           | Service date range (Only specified if durationType=Range).                                                                                                                                                        |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@startDate*                                                                    | 1        | String    | Start date to service.                                                                                                                                                                                            |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@endDate*                                                                      | 1        | String    | End date to service.                                                                                                                                                                                              |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option/Parameters                                    | 0..1     |           | Parameters for additional information.                                                                                                                                                                            |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlans/MealPlan/Options/Option/Parameters/Parameter                          | 1..n     |           | List of parameter.                                                                                                                                                                                                |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@key*                                                                          | 1        | String    | Contains the keyword/Id to identify a parameter.                                                                                                                                                                  |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@value*                                                                        | 1        | String    | Contains the value of the parameter                                                                                                                                                                               |
+---------------------------------------------------------------------------------+----------+-----------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

| 
| `toc <#toc>`__

--------------

*Valuation* (Pre-Booking)
^^^^^^^^^^^^^^^^^^^^^^^^^

Method Goals

| 
| This method aims to return the total price and cancel policies of the
selected *Option*. This *Option* **must** be selected in the previous
step (*Avail*).

Request Format

| 
| The *Valuation* request is same that availabilityRQ and add rooms and
Mealplan code.

Response Format

| 
| The returned XML contains the total price and list of cancel policies.
Sometimes this method will fail since the selected option at *Avail*
time will not be available in this stage. In this case the integration
returns an error code 301.

Remarks

| 
| Some providers do not support this method. In this case all the info
**must** be returned in *Avail* and this method will do a *Avail* again
filtered by the selected option.
| `toc <#toc>`__

--------------

*ValuationRQ* Example
'''''''''''''''''''''

::

    <ValuationRQ>
        <StartDate>28/01/2014</StartDate>
        <EndDate>29/01/2014</EndDate>
        <MealPlanCode>D</MealPlanCode>
        <HotelCode>10</HotelCode>
        <PaymentType>MerchantPay</PaymentType>
        <OptionType>Hotel</OptionType>
        <Rooms>
            <Room id = "4582" roomCandidateRefId = "1" code = "506" description = "Doble Standard.."/>
        </Rooms>
        <RoomCandidates>
            <RoomCandidate id = "1">
                <Paxes>
                    <Pax age = "30" id = "1"/>
                    <Pax age = "30" id = "2"/>
                </Paxes>
            </RoomCandidate>
        </RoomCandidates>
    </ValuationRQ>

| 
| `toc <#toc>`__

--------------

*ValuationRQ* Description
'''''''''''''''''''''''''

+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| Element                                  | Number   | Type      | Description                                                             |
+==========================================+==========+===========+=========================================================================+
| ValuationRQ                              | 1        |           | Root node.                                                              |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| StartDate                                | 1        | String    | Start date to search rates.                                             |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| EndDate                                  | 1        | String    | End date to search rates.                                               |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| MealPlanCode                             | 1        | String    | MealPlan code.                                                          |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| HotelCode                                | 1        | String    | Hotel code.                                                             |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| PaymentType                              | 1        | String    | Indicates the typology of payment.                                      |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| OptionType                               | 1        | String    | Indicates the type of option.                                           |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| Rooms                                    | 1        |           | Rooms of this option ( room list).                                      |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| Rooms/Room                               | 1..n     |           | Detail of room.                                                         |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| *@id*                                    | 1        | String    | Identifier of the room.                                                 |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| *@roomCandidateRefId*                    | 1        | Integer   | Identifier of room candidate.                                           |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| *@code*                                  | 1        | String    | Room code.                                                              |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| *@description*                           | 1        | String    | Room description.                                                       |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| RoomCandidates                           | 1        |           | Rooms required.                                                         |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| RoomCandidates/RoomCandidate             | 1..n     |           | Room required.                                                          |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| *@id*                                    | 1        | Integer   | Id of the requested room (starting at 1).                               |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| RoomCandidates/RoomCandidate/Paxes/Pax   | 1..n     |           | Pax required.                                                           |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| *@age*                                   | 1        | Integer   | Passenger age.                                                          |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| *@id*                                    | 1        | Integer   | Passenger id (starting at 1).                                           |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| Parameters                               | 0..1     |           | Additional parameters that have been reported in the option (AvailRS)   |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| Parameters/Parameter                     | 0..n     |           | Additional parameter that requires the integration                      |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| *@key*                                   | 1        | String    | Contains the keyword/Id to identify a parameter.                        |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+
| *@value*                                 | 1        | String    | Contains the value of the parameter                                     |
+------------------------------------------+----------+-----------+-------------------------------------------------------------------------+

| 
| `toc <#toc>`__

--------------

*ValuationRS* Example
'''''''''''''''''''''

::

    <ValuationRS >
        <Parameters>
            <Parameter key = "bd1" value = "43"/>
        </Parameters>
        <Price currency = "EUR" amount = "36.20" binding = "false" commission = "-1" importeNoComisionable = "0"/>
        <CancelPenalties nonRefundable = "false">
            <CancelPenalty>
                <HoursBefore>48</HoursBefore>
                <Penalty type = "Importe" paymentType = "MerchantPay" currency = "EUR">72.40</Penalty>
            </CancelPenalty>
        </CancelPenalties>
        <Remarks/>
    </ValuationRS>

| 
| `toc <#toc>`__

--------------

*ValuationRS* Description
'''''''''''''''''''''''''

+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| Element                                     | Number   | Type      | Description                                                                                                                                             |
+=============================================+==========+===========+=========================================================================================================================================================+
| ValuationRS                                 | 1        |           | Root node.                                                                                                                                              |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| Parameters                                  | 0..1     |           | Parameters for additional information.                                                                                                                  |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| Parameters/Parameter                        | 1..n     |           | List of parameter.                                                                                                                                      |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@key*                                      | 1        | String    | Contains the keyword/Id to identify a parameter.                                                                                                        |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@value*                                    | 1        | String    | Contains the value of the parameter.                                                                                                                    |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| Price                                       | 1        |           | Total price of this valuation.                                                                                                                          |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@currency*                                 | 1        | String    | Currency code.                                                                                                                                          |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@amount*                                   | 1        | Decimal   | Option Amount.                                                                                                                                          |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@binding*                                  | 1        | Boolean   | Identifies if is the price is binding ( When true the sale price returned **must** not be less than the price informed.                                 |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@commission*                               | 1        | Decimal   | Commission ( -1 = not specified (will come indicated with the provider contract ), 0 = net price, X = % of the commission that applies to the amount.   |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| CancelPenalties                             | 0..1     |           | Information of cancellation policies.                                                                                                                   |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@nonRefundable*                            | 1        | Boolean   | Indicate if this option is nonRefundable (true or false).                                                                                               |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| CancelPenalties/CancelPenalty               | 0..n     |           | Listing cancellation penalties.                                                                                                                         |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| CancelPenalties/CancelPenalty/HoursBefore   | 1        | String    | Number of hours prior to arrival day in which this Cancellation policy applies .                                                                        |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| CancelPenalties/CancelPenalty/Penalty       | 1        |           | Contains the value to apply.                                                                                                                            |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@type*                                     | 1        | String    | Type of penalty Possible values: "Noches" (nights) , "Porcentaje" (percentage) ,"Importe" (price value).                                                |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@paymentType*                              | 1        | String    | Indicates the typology of payment.                                                                                                                      |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@currency*                                 | 1        | String    | Currency code.                                                                                                                                          |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
| Remarks                                     | 0..1     | String    | Remarks.                                                                                                                                                |
+---------------------------------------------+----------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------+

| 
| `toc <#toc>`__

--------------

*Reservation* (Booking)
^^^^^^^^^^^^^^^^^^^^^^^

Method Goals

| 
| This method aims to book an option.

Request Format

| 
| The request format works the same way as the *Valuation* request but
with the list of passengers.

Response Format

| 
| The result returns the booking locator (booking code). It can be the
provider's or the one sent in the request.
| It also returns all the charges associated to the booking and the
state of booking.

Remarks

| 
| `toc <#toc>`__

--------------

*ReservationRQ* Example
'''''''''''''''''''''''

::

    <ReservationRQ>
        <ClientLocator>2537459</ClientLocator>
        <Parameters>
            <Parameter key = "extra" value = "31"/>
        </Parameters>
        <StartDate>28/01/2014</StartDate>
        <EndDate>29/01/2014</EndDate>
        <MealPlanCode>D</MealPlanCode>
        <HotelCode>10</HotelCode>
        <Price currency = "EUR" amount = "36.20" binding = "false" commission = "-1"/>
        <ResGuests>
            <Guests>
                <Guest roomCandidateId = "1" paxId = "1">
                    <GivenName>Test11</GivenName>
                    <SurName>TestAp11</SurName>
                </Guest>
                <Guest roomCandidateId = "1" paxId = "2">
                    <GivenName>Test12</GivenName>
                    <SurName>TestAp12</SurName>
                </Guest>
            </Guests>
        </ResGuests>
        <PaymentType>MenchardPay</PaymentType>
        <Rooms>
            <Room id = "4582" roomCandidateRefId = "1" code = "506" description = "Doble Standard.."/>
        </Rooms>
        <RoomCandidates>
            <RoomCandidate id = "1">
                <Paxes>
                    <Pax age = "30" id = "1"/>
                    <Pax age = "30" id = "2"/>
                </Paxes>
            </RoomCandidate>
        </RoomCandidates>
    </ReservationRQ>

| 
| `toc <#toc>`__

--------------

*ReservationRQ* Description
'''''''''''''''''''''''''''

+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Element                                  | Number   | Type      | Description                                                                                                                                              |
+==========================================+==========+===========+==========================================================================================================================================================+
| ReservationRQ                            | 1        |           | Root node.                                                                                                                                               |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClientLocator                            | 1        | String    | Client locator.                                                                                                                                          |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Parameters                               | 0..1     |           | Parameters for additional information that have been reported in ValuationRS.                                                                            |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Parameters/Parameter                     | 1..n     |           | List of parameter.                                                                                                                                       |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@key*                                   | 1        | String    | Contains the keyword/Id to identify a parameter.                                                                                                         |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@value*                                 | 1        | String    | Contains the value of the parameter                                                                                                                      |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| StartDate                                | 1        | String    | Start date to search rates.                                                                                                                              |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| EndDate                                  | 1        | String    | End date to search rates.                                                                                                                                |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| MealPlanCode                             | 1        | String    | MealPlan code.                                                                                                                                           |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| HotelCode                                | 1        | String    | Hotel code.                                                                                                                                              |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| PaymentType                              | 1        | String    | Indicates the typology of payment.                                                                                                                       |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Price                                    | 1        |           | Total price of this valuation.                                                                                                                           |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@currency*                              | 1        | String    | Currency code.                                                                                                                                           |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@amount*                                | 1        | Decimal   | Option Amount.                                                                                                                                           |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@binding*                               | 1        | Boolean   | Identifies if is the price is binding ( When true the sale price returned **must** not be less than the price informed.                                  |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@commission*                            | 1        | Decimal   | Commission ( -1 = not specified (will come indicated with the provider contract ), 0 = net price, X = % of the commission that applies to the amount .   |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| ResGuests                                | 1        |           | Structure of the passengers.                                                                                                                             |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| ResGuests/Guests                         | 1        |           | List of passengers.                                                                                                                                      |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| ResGuests/Guests/Guest                   | 1..n     |           | Detail of each passenger.                                                                                                                                |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@roomCandidateId*                       | 1        | Integer   | Identifier of room candidate.                                                                                                                            |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@paxId*                                 | 1        | Integer   | Passenger id (starting at 1).                                                                                                                            |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| ResGuests/Guests/Guest/GivenName         | 1        | String    | Given name.                                                                                                                                              |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| ResGuests/Guests/Guest/SurName           | 1        | String    | Surname.                                                                                                                                                 |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rooms                                    | 1        |           | Rooms of this option ( room list).                                                                                                                       |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rooms/Room                               | 1..n     |           | Detail of room.                                                                                                                                          |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@id*                                    | 1        | String    | Identifier of the room.                                                                                                                                  |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@roomCandidateRefId*                    | 1        | Integer   | Identifier of room candidate.                                                                                                                            |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@code*                                  | 1        | String    | Room code.                                                                                                                                               |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@description*                           | 1        | String    | Room description.                                                                                                                                        |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| RoomCandidates/RoomCandidate             | 1..n     |           | Room required.                                                                                                                                           |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@id*                                    | 1        | Integer   | Id of the requested room (starting at 1).                                                                                                                |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| RoomCandidates/RoomCandidate/Paxes/Pax   | 1..n     |           | Pax required.                                                                                                                                            |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@age*                                   | 1        | Integer   | Passenger age.                                                                                                                                           |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@id*                                    | 1        | Integer   | Passenger id (starting at 1).                                                                                                                            |
+------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+

| 
| `toc <#toc>`__

--------------

*ReservationRS* Example
'''''''''''''''''''''''

::

    <ReservationRS>
        <ProviderLocator>102</ProviderLocator>
        <ResStatus>OK</ResStatus>
        <Price currency = "EUR" amount = "36.20" binding = "false" commission = "-1"/>
    </ReservationRS>

| 
| `toc <#toc>`__

--------------

*ReservationRS* Description
'''''''''''''''''''''''''''

+-------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Element           | Number   | Type      | Description                                                                                                                                              |
+===================+==========+===========+==========================================================================================================================================================+
| ReservationRS     | 1        |           | Root node.                                                                                                                                               |
+-------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| ProviderLocator   | 1        | String    | Provider locator                                                                                                                                         |
+-------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| ResStatus         | 1        | String    | Status of book (OK = confirmed, RQ = on request, CN = canceled, UN = unknown                                                                             |
+-------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Price             | 0..1     |           | Total price of this book.                                                                                                                                |
+-------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@currency*       | 1        | String    | Currency code.                                                                                                                                           |
+-------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@amount*         | 1        | Decimal   | Book Amount.                                                                                                                                             |
+-------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@binding*        | 1        | Boolean   | Identifies if is the price is binding ( When true the sale price returned **must** not be less than the price informed.                                  |
+-------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@commission*     | 1        | Decimal   | Commission ( -1 = not specified (will come indicated with the provider contract ), 0 = net price, X = % of the commission that applies to the amount .   |
+-------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Remarks           | 0..1     | String    | Remarks of this book.                                                                                                                                    |
+-------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+

| 
| `toc <#toc>`__

--------------

*ReservationRead* (Get Booking Details)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Method Goals

| 
| This method aims to retrieve a booking with its full details.

Request Format

| 
| The request requires one of the following data depending on provider:

-  *Locators*: booking codes (this element contains two elements
   *Client* (client's booking code) and *Provider* (provider's booking
   code), one or both will be required depending on the provider)
-  *Currency*: the currency code
-  *CreationDate*: the booking date
-  *StardDate*: the check-in date
-  *EndDate*: the check-out date

| 

Response Format

| 
| The result returns the full details of a booking. It is very similar
to the *Option* in the Availability Response, the cancel policies and
holder of booking.

Remarks

| 
| Some providers do not support this method.
| `toc <#toc>`__

--------------

*ReservationReadRQ* Example
'''''''''''''''''''''''''''

::

    <ReservationReadRQ>
        <Locators>
            <Client>5356342</Client>
            <Provider>MGNZ12345</Provider>
        </Locators>
        <Currency>EUR</Currency>
        <StartDate>28/01/2014</StartDate>
        <EndDate>29/01/2014</EndDate>
        <CreationDate>17/01/2014</CreationDate>
    </ReservationReadRQ>

| 
| `toc <#toc>`__

--------------

*ReservationReadRQ* Description
'''''''''''''''''''''''''''''''

+---------------------+----------+----------+---------------------------------------------------------------------------------------------+
| Element             | Number   | Type     | Description                                                                                 |
+=====================+==========+==========+=============================================================================================+
| ReservationReadRQ   | 1        |          | Root node.                                                                                  |
+---------------------+----------+----------+---------------------------------------------------------------------------------------------+
| Locators            | 1        |          | Information of the locators (it is mandatory indicate one of two, or client or provider).   |
+---------------------+----------+----------+---------------------------------------------------------------------------------------------+
| Locators/Client     | 0..1     | String   | Client locator.                                                                             |
+---------------------+----------+----------+---------------------------------------------------------------------------------------------+
| Locators/Provider   | 0..1     | String   | Provider locator.                                                                           |
+---------------------+----------+----------+---------------------------------------------------------------------------------------------+
| Currency            | 1        | String   | Currency code.                                                                              |
+---------------------+----------+----------+---------------------------------------------------------------------------------------------+
| StartDate           | 1        | String   | Start date of booking.                                                                      |
+---------------------+----------+----------+---------------------------------------------------------------------------------------------+
| EndDate             | 1        | String   | End date of booking.                                                                        |
+---------------------+----------+----------+---------------------------------------------------------------------------------------------+
| CreationDate        | 1        | String   | Creation date of booking.                                                                   |
+---------------------+----------+----------+---------------------------------------------------------------------------------------------+

| 
| `toc <#toc>`__

--------------

*ReservationReadRS* Example
'''''''''''''''''''''''''''

::

    <ReservationReadRS>
          <Locators>
                    <Client>2578478</Client>
                    <Provider>10TTT31</Provider>
                </Locators>
                <Hotel>
                    <Name>LEO</Name>
                    <Code>10</Code>
                    <CreationDate>17/01/2014</CreationDate>
                    <StartDate>28/01/2014</StartDate>
                    <EndDate>29/01/2014</EndDate>
                    <Holder name = "Test11" surname = "TestAp11"/>
                    <Price currency = "EUR" amount = "36.20" binding = "false" commission = "-1"/>
                    <Rooms>
                        <Room id = "4582" roomCandidateRefId = "1" description = "Doble Standard.."/>
                    </Rooms>
                    <CancelPenalties nonRefundable = "false">
                        <CancelPenalty>
                            <HoursBefore>120</HoursBefore>
                            <Penalty type = "Importe" paymentType = "pagoMinorista" currency = "EUR">72.40</Penalty>
                        </CancelPenalty>
                    </CancelPenalties>
                </Hotel>
                <TransactionStatus>
                    <ComunicationStatus>OK</ComunicationStatus>
                    <RSStatus>EXISTE</RSStatus>
                    <ResStatus>OK</ResStatus>
                </TransactionStatus>
    </ReservationReadRS>

| 
| `toc <#toc>`__

--------------

*ReservationReadRS* Description
'''''''''''''''''''''''''''''''

Element

Number

Type

Description

ReservationReadRS

1

Root node.

Locators

1

Information of the locators (it is mandatory indicate one of two, or
client or provider).

Locators/Client

0..1

String

Client locator.

Locators/Provider

0..1

String

Provider locator.

Hotel

0..1

\|Hotel reservation.

Hotel/Name

0..1

String

Hotel name.

Hotel/Code

1

String

Hotel code.

Hotel/City

0..1

String

Hotel city.

Hotel/CreationDate

0..1

String

Creation date of booking.

Hotel/StartDate

1

String

Start date of booking.

Hotel/EndDate

1

String

End date of booking.

Hotel/MealPlanCode

0..1

String

Mealplan code of booking.

Hotel/Holder

0..1

\|Holder reservation.

*@name*

1

String

Holder name.

\_@surname

1

Decimal

Holder surname.

Hotel/Price

0..1

\|Price reservation.

*@currency*

1

String

Currency code.

*@amount*

1

Decimal

Book Amount.

*@binding*

1

Boolean

Identifies if is the price is binding ( When true the sale price
returned **must** not be less than the price informed.

*@commission*

1

Decimal

Commission ( -1 = not specified (will come indicated with the provider
contract ), 0 = net price, X = % of the commission that applies to the
amount .

Hotel/Rooms

0..1

\|Rooms reservation.

Hotel/Rooms/Room

1..n

\|Room reservation.

*@id*

0..1

String

Identifier of the room.

*@roomCandidateRefId*

0..1

Integer

Identifier of room candidate.

*@code*

0..1

String

Room code.

*@description*

0..1

String

Room description.

Hotel/RoomCandidates

0..1

\|Rooms required in the creation of the booking.

Hotel/RoomCandidates/RoomCandidate

1..n

Room required.

*@id*

0..1

Integer

Id of the requested room (starting at 1).

RoomCandidates/RoomCandidate/Paxes/Pax

1..n

Pax required.

*@age*

0..1

Integer

Passenger age.

*@id*

0..1

Integer

Passenger id (starting at 1).

Hotel/CancelPenaltiesCancelPenalties

0..1

Information of cancellation policies.

*@nonRefundable*

1

Boolean

Indicate if this option is nonRefundable (true or false).

Hotel/CancelPenalties/CancelPenalty

0..n

Listing cancellation penalties.

Hotel/CancelPenalties/CancelPenalty/HoursBefore

1

String

Number of hours prior to arrival day in which this Cancellation policy
applies .

Hotel/CancelPenalties/CancelPenalty/Penalty

1

Contains the value to apply.

*@type*

1

String

Type of penalty Possible values: "Noches" (nights) , "Porcentaje"
(percentage) ,"Importe" (price value).

*@paymentType*

1

String

Indicates the typology of payment.

*@currency*

1

String

Currency code.

Hotel/Remarks

0..1

String

Remarks.

TransactionStatus

1

Transaction Status.

TransactionStatus/ComunicationStatus

1

String

Status communication ( OFFLINE, OK and KO) .

TransactionStatus/RSStatus

1

String

Status response (Status response (DESCONOCIDO (Unknown), EXISTE
(Exists), EXISTECANCELADA (Canceled), NO\_EXISTE (Does not exist)).

TransactionStatus/ResStatus

1

String

Status booking (OK = confirmed, RQ = on request, CN = canceled, UN =
unknown).

| 
| `toc <#toc>`__

--------------

*ReservationList* (Get Booking List)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Method Goals

| 
| This method aims to return a list of bookings for a given time period
being that either booking date or the traveling date.

Request Format

| 
| The request requires one of the following data depending on provider:

-  *DateType*: indicates the date type: either booking creation date or
   booking start date
-  *Start*: the date from
-  *End*: the date to

| 

Response Format

| 
| The result returns a list of bookings details, with the same format as
*ReservationReadRS*.

Remarks

| 
| Not implemented by all providers
| `toc <#toc>`__

--------------

*ReservationListRQ* Example
'''''''''''''''''''''''''''

::

    <ReservationListRQ>
        <DateType>E</DateType>
        <Start>01/01/2014</Start>
        <End>22/02/2014</End>
    </ReservationListRQ>

| 
| `toc <#toc>`__

--------------

*ReservationListRQ* Description
'''''''''''''''''''''''''''''''

+---------------------+----------+----------+---------------------------------------------------------+
| Element             | Number   | Type     | Description                                             |
+=====================+==========+==========+=========================================================+
| ReservationListRQ   | 1        |          | Root node.                                              |
+---------------------+----------+----------+---------------------------------------------------------+
| DateType            | 1        | String   | Type search ( A = arrival date, B = booking creation.   |
+---------------------+----------+----------+---------------------------------------------------------+
| Start               | 1        | String   | Start date.                                             |
+---------------------+----------+----------+---------------------------------------------------------+
| End                 | 1        | String   | End date.                                               |
+---------------------+----------+----------+---------------------------------------------------------+
| Currency            | 1        | String   | Currency code.                                          |
+---------------------+----------+----------+---------------------------------------------------------+

| 
| `toc <#toc>`__

--------------

*ReservationListRS* Example
'''''''''''''''''''''''''''

::

    <ReservationListRS>
        <Reservations>
            <Reservation>
                <auditData>
                    <timeStamp>2014-01-21T15:12:12.0558866+00:00</timeStamp>
                    <processTimeMilliseconds>0</processTimeMilliseconds>
                </auditData>
                <operationImplemented>true</operationImplemented>
                <Locators>
                    <Client>2196</Client>
                    <Provider>1AAAA966</Provider>
                </Locators>
                <Hotel>
                    <Name>LAS VEGAS (BENIDORM)</Name>
                    <Code>58475</Code>
                    <CreationDate>30/09/2013</CreationDate>
                    <StartDate>25/01/2014</StartDate>
                    <EndDate>16/02/2014</EndDate>
                    <Holder name = "AAAA" surname = "Test"/>
                    <Price currency = "EUR" amount = "658.94" binding = "false" commission = "-1"/>
                    <Rooms>
                        <Room id = "27441" roomCandidateRefId = "1" description = "Doble Standard"/>
                    </Rooms>
                    <CancelPenalties nonRefundable = "false">
                        <CancelPenalty>
                            <HoursBefore>72</HoursBefore>
                            <Penalty type = "Importe" paymentType = "pagoMinorista" currency = "EUR">29.95</Penalty>
                        </CancelPenalty>
                    </CancelPenalties>
                </Hotel>
                <TransactionStatus>
                    <ComunicationStatus>OK</ComunicationStatus>
                    <RSStatus>EXISTE</RSStatus>
                    <ResStatus>OK</ResStatus>
                </TransactionStatus>
            </Reservation>
            <Reservation>
                <auditData>
                    <timeStamp>2014-01-21T15:12:12.6657414+00:00</timeStamp>
                    <processTimeMilliseconds>0</processTimeMilliseconds>
                </auditData>
                <operationImplemented>true</operationImplemented>
                <Locators>
                    <Client>2578478</Client>
                    <Provider>10TTT31</Provider>
                </Locators>
                <Hotel>
                    <Name>LEO</Name>
                    <Code>10</Code>
                    <CreationDate>17/01/2014</CreationDate>
                    <StartDate>28/01/2014</StartDate>
                    <EndDate>29/01/2014</EndDate>
                    <Holder name = "Test11" surname = "TestAp11"/>
                    <Price currency = "EUR" amount = "36.20" binding = "false" commission = "-1"/>
                    <Rooms>
                        <Room id = "4582" roomCandidateRefId = "1" description = "Doble Standard.."/>
                    </Rooms>
                    <CancelPenalties nonRefundable = "false">
                        <CancelPenalty>
                            <HoursBefore>120</HoursBefore>
                            <Penalty type = "Importe" paymentType = "pagoMinorista" currency = "EUR">72.40</Penalty>
                        </CancelPenalty>
                    </CancelPenalties>
                </Hotel>
                <TransactionStatus>
                    <ComunicationStatus>OK</ComunicationStatus>
                    <RSStatus>EXISTE</RSStatus>
                    <ResStatus>OK</ResStatus>
                </TransactionStatus>
            </Reservation>
    ...
        </Reservations>
    </ReservationListRS>

| 
| `toc <#toc>`__

--------------

*ReservationListRS* Description
'''''''''''''''''''''''''''''''

+----------------------------------------------+----------+--------+----------------------------------------+
| Element                                      | Number   | Type   | Description                            |
+==============================================+==========+========+========================================+
| ReservationListRS                            | 1        |        | Root node.                             |
+----------------------------------------------+----------+--------+----------------------------------------+
| ReservationListRS/Reservations               | 0..1     |        | Reservations.                          |
+----------------------------------------------+----------+--------+----------------------------------------+
| ReservationListRS/Reservations/Reservation   | 1        |        | Same structure as ReservationReadRS.   |
+----------------------------------------------+----------+--------+----------------------------------------+

| 
| `toc <#toc>`__

--------------

*Cancel* (Cancel Booking)
^^^^^^^^^^^^^^^^^^^^^^^^^

Method Goals

| 
| This method aims to cancel a booking

Request Format

| 
| The request requires one of the following data depending on provider:

-  *Locators*: booking codes (this element contains two elements
   *Client* (client's booking code) and *Provider* (provider's booking
   code), one or both will be required depending on the provider)
-  *hotelCode*: the hotel code
-  *StartDate*: the check-in date
-  *EndDate*: the check-out date

| 

Response Format

| 
| The result returns a response with the state of booking, the
cancellation's identification and the fee for that cancellation.

Remarks

| 
| Not supported by all providers
| `toc <#toc>`__

--------------

*CancelRQ* Example
''''''''''''''''''

::

    <CancelRQ  hotelCode="H1548">
        <Locators>
            <Client>AFH123OP567</Client>
            <Provider>YYYYYYYY</Provider>
        </Locators>
        <StartDate>15/10/2012</StartDate>
        <EndDate>20/10/2015</EndDate>
    </CancelRQ>

| 
| `toc <#toc>`__

--------------

*CancelRQ* Description
''''''''''''''''''''''

+---------------------+----------+----------+---------------------------------------------------------------------------------------------+
| Element             | Number   | Type     | Description                                                                                 |
+=====================+==========+==========+=============================================================================================+
| CancelRQ            | 1        |          | Root node.                                                                                  |
+---------------------+----------+----------+---------------------------------------------------------------------------------------------+
| \_@hotelCode        | 1        | String   | Hotel code.                                                                                 |
+---------------------+----------+----------+---------------------------------------------------------------------------------------------+
| Locators            | 1        |          | Information of the locators (it is mandatory indicate one of two, or client or provider).   |
+---------------------+----------+----------+---------------------------------------------------------------------------------------------+
| Locators/Client     | 0..1     | String   | Client locator.                                                                             |
+---------------------+----------+----------+---------------------------------------------------------------------------------------------+
| Locators/Provider   | 0..1     | String   | Provider locator.                                                                           |
+---------------------+----------+----------+---------------------------------------------------------------------------------------------+
| StartDate           | 1        | String   | Start date of booking.                                                                      |
+---------------------+----------+----------+---------------------------------------------------------------------------------------------+
| EndDate             | 1        | String   | End date of booking.                                                                        |
+---------------------+----------+----------+---------------------------------------------------------------------------------------------+

| 
| `toc <#toc>`__

--------------

*CancelRS* Example
''''''''''''''''''

::

    <CancelRS>
        <ProviderLocator>XXXX0000</ProviderLocator> 
        <CancelId>0000000</CancelId>
          <TransactionStatus>
                <ComunicationStatus>OK</ComunicationStatus>
                <RSStatus>EXISTE</RSStatus>
                <ResStatus>OK</ResStatus>
          </TransactionStatus>
         <Price  currency="EUR" amount="120.5" binding="false" commission="-1"/>
    </CancelRS>

| 
| `toc <#toc>`__

--------------

*CancelRS* Description
''''''''''''''''''''''

Element

Number

Type

Description

]

CancelRS

1

\|Root node.

ProviderLocator

1

String

Provider locator.

CancelId

0..1

String

Cancelation id.

Price

0..1

\|Price cancelation.

*@currency*

1

String

Currency code.

*@amount*

1

Decimal

Book Amount.

*@binding*

1

Boolean

Identifies if is the price is binding ( When true the sale price
returned **must** not be less than the price informed.

*@commission*

1

Decimal

Commission ( -1 = not specified (will come indicated with the provider
contract ), 0 = net price, X = % of the commission that applies to the
amount.

TransactionStatus

1

Transaction Status.

TransactionStatus/ComunicationStatus

1

String

Status communication ( OFFLINE, OK and KO) .

TransactionStatus/RSStatus

1

String

Status response (DESCONOCIDO (Unknown), EXISTE (Exists), EXISTECANCELADA
(Canceled), NO\_EXISTE (Does not exist)).

TransactionStatus/ResStatus

1

String

Status booking (OK = confirmed, RQ = on request, CN = canceled, UN =
unknown).

| 
| `toc <#toc>`__

--------------

*HotelList* (Hotels List)
^^^^^^^^^^^^^^^^^^^^^^^^^

Method Goals

| 
| This method returns a list of hotels, where every hotel contains basic
information ( code, name, address, phone...)

Request Format

| 
| The request does not require any elements. Empty request.

Response Format

| 
| The result returns a list of *Hotel* (hotels).

Remarks

| 
| This method may be preloaded in **XML Travelgate**'s system if it
takes more than 5 minutes to download.
| `toc <#toc>`__

--------------

*HotelListRQ* Example
'''''''''''''''''''''

::

    <HotelListRQ>
    </HotelListRQ>

| 
| `toc <#toc>`__

--------------

*HotelListRQ* Description
'''''''''''''''''''''''''

Element

Number

Type

Description

HotelListRQ

1

\|Root node.

| 
| `toc <#toc>`__

--------------

*HotelListRS* Example
'''''''''''''''''''''

::

    <HotelListRS>
        <Hotels>
            <Hotel>
                <Code>5</Code>
                <Name>BADAJOZ</Name>
                <Address>CTRA.NACIONAL V, KM 393</Address>
                <Town>BADAJOZ</Town>
                <ZipCode>06002</ZipCode>
                <CountryISOCode>ES</CountryISOCode>
                <AvailDestination code = "06" name = "BADAJOZ"/>
                <GeographicDestination code = "06" name = "BADAJOZ" avail = "true"/>
                <Latitude>38.893839</Latitude>
                <Longitude>-7.014112</Longitude>
                <Contact>
                    <Email>badajoz@xxx.com</Email>
                    <Telephone>91425891</Telephone>
                    <Fax>910200200</Fax>
                </Contact>
                <CategoryCode>4 Estrellas</CategoryCode>
            </Hotel>
            <Hotel>
                <Code>7</Code>
                <Name>ILLA</Name>
                <Address>AVDA. ILLA S/N</Address>
                <Town>HUELVA</Town>
                <ZipCode>21449</ZipCode>
                <CountryISOCode>ES</CountryISOCode>
                <AvailDestination code = "2" name = "HUELVA"/>
                <GeographicDestination code = "2" name = "HUELVA" avail = "true"/>
                <Latitude>37.207295</Latitude>
                <Longitude>-7.23768</Longitude>
                <Contact>
                    <Email>emailhotel@xxx.es</Email>
                    <Telephone>95124578</Telephone>
                    <Fax>910200200</Fax>
                </Contact>
                <CategoryCode>4 Estrellas</CategoryCode>     
            </Hotel>
            <Hotel>...</Hotel>
        </Hotels>
    </HotelListRS>

| 
| `toc <#toc>`__

--------------

*HotelListRS* Description
'''''''''''''''''''''''''

Element

Number

Type

Description

HotelListRS/Hotels/Hotel

0..n

\|Root node. Hotel sheet.

Code

1

String

Code.

Name

1

String

Name.

Address

1

String

Address.

Town

1

String

Town.

ZipCode

1

String

ZipCode.

CountryISOCode

1

String

CountryISOCode.

AvailDestination

0..1

Avail Destination ( will come only if it is attackable on availability,
and the type is CTY).

*@code*

1

String

Destination code.

*@name*

1

String

Destination name.

GeographicDestination

1

Geographic Destination.

*@code*

1

String

Destination code.

*@name*

1

String

Destination name.

*@avail*

1

Boolean

Indicates if it is attackable on availability.

Latitude

1

String

Latitude.

Longitude

1

String

Longitude.

Contact

1

Contact.

Contact/Email

1

String

Email.

Contact/Telephone

1

String

Telephone.

Contact/Fax

1

String

Fax.

CategoryCode

1

String

CategoryCode.

| 
| `toc <#toc>`__

--------------

*DescriptiveInfo* (Hotel Details)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Method Goals

| 
| This method returns the details of a hotel (pictures, descriptions
...) for a given language.

Request Format

| 
| The request just requires the hotel code and language code (ISO-639-1)
( this is specified within the source-->languageCode).

Response Format

| 
| The result returns the details of that hotel.

Remarks

| 
| The languages codes are limited by each provider.
| `toc <#toc>`__

--------------

*DescriptiveInfoRQ* Example
'''''''''''''''''''''''''''

::

    <DescriptiveInfoRQ>
        <Hotel>
            <Code>524AC</Code>
        </Hotel>
    </DescriptiveInfoRQ>

| 
| `toc <#toc>`__

--------------

*DescriptiveInfoRQ* Description
'''''''''''''''''''''''''''''''

Element

Number

Type

Description

DescriptiveInfoRQ

1

\|Root node.

DescriptiveInfoRQ/Hotel

1

\| Hotel requested.

DescriptiveInfoRQ/Hotel/Code

1

String

Code.

| 
| `toc <#toc>`__

--------------

*DescriptiveInfoRS* Example
'''''''''''''''''''''''''''

::

    <DescriptiveInfoRS>
        <Hotel>
            <Code>70</Code>
            <Name>ILLA</Name>
            <GiataFormatCode>70ES</GiataFormatCode>
            <Address>AVDA. ILLA S/N</Address>
            <Town>HUELVA</Town>
            <ZipCode>21449</ZipCode>
            <CountryISOCode>ES</CountryISOCode>
            <AvailDestination code = "2" name = "HUELVA"/>
            <GeographicDestination code = "2" name = "HUELVA" avail = "true"/>
            <Contact>
                <Email>emailhotel@xxx.com</Email>
                <Telephone>91547892</Telephone>
                <Fax></Fax>
            </Contact>
            <BookingContact>
                <Email>bookinghotel@xxx.com</Email>
                <Telephone>91547880</Telephone>
                <Fax>910200200</Fax>
            </BookingContact>
            <CategoryCode>4 Estrellas</CategoryCode>
            <Type>H</Type>
            <ShortDescription>the hotel.....</ShortDescription>
            <LongDescription>the hotel....</LongDescription>
            <HowToGet></HowToGet>
            <RoomDescription>....</RoomDescription>
            <SituationDescription>....</SituationDescription>
            <Images>
                <Picture>
                    <URL>http://www.images.net/infor/work/imagen/hotel_07/mapa.jpg</URL>
                    <Classification>GRAL</Classification>
                </Picture>
                <Picture>
                    <URL>http://www.images.net/infor/work/imagen/hotel_02/M.jpg</URL>
                    <Classification>GRAL</Classification>
                </Picture>
            </Images>
            <LocationType>City</LocationType>
        </Hotel>
    </DescriptiveInfoRS>

| 
| `toc <#toc>`__

--------------

*DescriptiveInfoRS* Description
'''''''''''''''''''''''''''''''

Element

Number

Type

Description

DescriptiveInfoRS/Hotel

0..n

\|Root node. Hotel sheet.

Code

1

String

Code.

Name

1

String

Name.

Address

1

String

Address.

Town

1

String

Town.

ZipCode

1

String

ZipCode.

CountryISOCode

1

String

CountryISOCode.

AvailDestination

0..1

Avail Destination ( will come only if it is attackable on availability,
and the type is CTY).

*@code*

1

String

Destination code.

*@name*

1

String

Destination name.

GeographicDestination

1

Geographic Destination.

*@code*

1

String

Destination code.

*@name*

1

String

Destination name.

*@avail*

1

Boolean

Indicates if it is attackable on availability.

Latitude

1

String

Latitude.

Longitude

1

String

Longitude.

Contact

0..1

Contact.

Contact/Email

1

String

Email.

Contact/Telephone

1

String

Telephone.

Contact/Fax

1

String

Fax.

CategoryCode

1

String

CategoryCode.

BookingContact

0..1

Booking Contact.

BookingContact/Email

1

String

Email.

BookingContact/Telephone

1

String

Telephone.

BookingContact/Fax

1

String

Fax.

Type

0..1

String

Hotel type: H (hotel) A (apartment) AH (aparthotel) C (club) AT
(agritourism) HS (hostel) CA (house) V (Ville) B (Bungalows).

Chaincode

0..1

String

Chain code.

ShortDescription

0..1

String

Short Description.

LongDescription

0..1

String

Long Description.

HowToGet

0..1

String

How to get description.

RoomDescription

0..1

String

Room description.

SituationDescription

0..1

String

Situation description.

RestaurantsDescription

0..1

String

Restaurants description.

PoolsDescription

0..1

String

Pools description.

ActivitiesDescription

0..1

String

Activities description.

ServicesDescription

0..1

String

Services description.

AdditionalDetails

0..1

String

Additional details.

Attributes

0..1

Attributes.

Attributes/Attribute

1..n

Attribute.

Attributes/Attribute/Code

1

String

Code.

Attributes/Attribute/Value

1

String

Value.

Attributes/Attribute/Classification

1

String

Classification ( HOT=hotel, HAB=room, SER=service and GRAL=generic).

Images

0..1

Images.

Images/Picture

1..n

Picture.

Images/Picture/Url

1

String

Url.

Images/Picture/Classification

1

String

Classification ( HOT=hotel, HAB=room, SER=service and GRAL=generic).

Images/Picture/Ordered

0..1

String

Images should be ordered from 1 onward. 1 is top.

Images/Picture/Description

1

String

Description.

LocationType

0..1

String

CategoryCode.

CategoryCode

1

String

CategoryCode.

| 
| `toc <#toc>`__

--------------

*AvailDestinationTree* (Destinations Tree of Availability)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Method Goals

| 
| This method returns the tree of destinations accessible from the call
*Avail* .

Request Format

| 
| The request does not require any elements empty request.

Response Format

| 
| The result returns a list of *DestinationTree* with their
corresponding sub-destinations.

Remarks

| 
| Only implemented for providers that are more than an affordable level
in availability.
| `toc <#toc>`__

--------------

*AvailDestinationTreeRQ* Example
''''''''''''''''''''''''''''''''

::

    <AvailDestinationTreeRQ>
    </AvailDestinationTreeRQ>

| 
| `toc <#toc>`__

--------------

*AvailDestinationTreeRQ* Description
''''''''''''''''''''''''''''''''''''

Element

Number

Type

Description

| 
| `toc <#toc>`__

--------------

*AvailDestinationTreeRS* Example
''''''''''''''''''''''''''''''''

::

    <AvailDestinationTreeRS>
        <DestinationTree code = "ES" name = "España">
            <DestinationLeaf code = "BAL"/>
            <DestinationLeaf code = "AST"/>
            <DestinationLeaf code = "AND"/>
        </DestinationTree>
        <DestinationTree code = "IT" name = "Italia">
            <DestinationLeaf code = "AA"/>
            <DestinationLeaf code = "BB"/>
            . . .
        </DestinationTree>
        <DestinationTree code = "EN" name = "England">. . .    </DestinationTree>
        <DestinationTree code = "BAL" name = "Baleares">
            <DestinationLeaf code = "PAL0"/>
            <DestinationLeaf code = "ALC0"/>
        </DestinationTree>
        <DestinationTree code = "AST" name = "Asturias"/>
        <DestinationTree code = "AND" name = "Andalucia"/>
        <DestinationTree code = "PAL0" name = "Palma de Mallorca"/>
        <DestinationTree codigo = "ALC0" name = "Alcudia"/>
        . . .
    </AvailDestinationTreeRS>

| 
| `toc <#toc>`__

--------------

*AvailDestinationTreeRS* Description
''''''''''''''''''''''''''''''''''''

Element

Number

Type

Description

| 
| `toc <#toc>`__

--------------

*GeographicDestinationTree* (Geographic Destinations Tree)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Method Goals

| 
| This method returns the provider's geographic tree where each node
indicates whether the call is accessible from availability.

Request Format

| 
| The request not requires any element, it is empty.

Response Format

| 
| The result returns a list of *DestinationTree* with corresponding
sub-destinations.

Remarks

| 
| `toc <#toc>`__

--------------

*GeographicDestinationTreeRQ* Example
'''''''''''''''''''''''''''''''''''''

::

    <GeographicDestinationTreeRQ>
    </GeographicDestinationTreeRQ>

| 
| `toc <#toc>`__

--------------

*GeographicDestinationTreeRQ* Description
'''''''''''''''''''''''''''''''''''''''''

Element

Number

Type

Description

| 
| `toc <#toc>`__

--------------

*GeographicDestinationTreeRS* Example
'''''''''''''''''''''''''''''''''''''

::

    <GeographicDestinationTreeRS>
        <DestinationTree code = "ES" name = "España" avail = "False">
            <DestinationLeaf code = "BAL"/>
            <DestinationLeaf code = "AST"/>
            <DestinationLeaf code = "AND"/>
        </DestinationTree>
        <DestinationTree code= "IT" name = "Italia" avail = "False">
            <DestinationLeaf code = "AA"/>
            <DestinationLeaf code = "BB"/>
            . . .
        </DestinationTree>
        <DestinationTree code = "EN" name = "England" avail = "False">. . .</DestinationTree>
        <DestinationTree code = "BAL" name = "Baleares" avail = "True">
            <DestinationLeaf code = "PAL0"/>
            <DestinationLeaf code = "ALC0"/>
        </DestinationTree>
        <DestinationTree code = "AST" name = "Asturias" avail = "True"/>
        <DestinationTree code = "AND" name = "Andalucia" avail = "True"/>
        . . .
        <DestinationTree code = "PAL0" name = "Palma de Mallorca" avail = " True"/>
        <DestinationTree code = "ALC0" name = "Alcudia" avail = " True"/>
        . . .
    </GeographicDestinationTreeRS>

| 
| `toc <#toc>`__

--------------

*GeographicDestinationTreeRS* Description
'''''''''''''''''''''''''''''''''''''''''

Element

Number

Type

Description

| 
| `toc <#toc>`__

--------------

*MealPlanList* (MealPlan List)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Method Goals

| 
| This method aims to return a list of the available Mealplans, which
will be used in the availability response.

Request Format

| 
| The request does not require any elements empty request.

Response Format

| 
| The result returns a list of *MealPlan*.

Remarks

| 
| If the provider has more than 100 mealplan codes, or more than 20
codes for one single mealplan, this code will be mapped to XML
Travelgate's code. `Link to List of
Codes <#Link%20to%20List%20of%20Codes>`__
| `toc <#toc>`__

--------------

*MealPlanRQ* Example
''''''''''''''''''''

::

    <MealPlanListRQ>
    </MealPlanListRQ>

| 
| `toc <#toc>`__

--------------

*MealPlanListRQ* Description
''''''''''''''''''''''''''''

Element

Number

Type

Description

| 
| `toc <#toc>`__

--------------

*MealPlanListRS* Example
''''''''''''''''''''''''

::

    <MealPlanListRS>
        <MealPlans>
            <MealPlan>
                <Code>AD</Code>
                <Name>Alojamiento y desayuno</Name>
            </MealPlan>
            <MealPlan>
                <Code>MP</Code>
                <Name>Media Pensión</Name>
            </MealPlan>
            …
            <MealPlan/>
        </MealPlans>
    </MealPlanListRS>

| 
| `toc <#toc>`__

--------------

*MealPlanListRS* Description
''''''''''''''''''''''''''''

Element

Number

Type

Description

| 
| `toc <#toc>`__

--------------

*CategoryList* (Hotel Category List)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Method Goals

| 
| This method aims to return a list of the available categories, which
will be used in the list of hotels response.

Request Format

| 
| The request does not require any elements empty request.

Response Format

| 
| The result returns a list of *Category* .

Remarks

| 
| `toc <#toc>`__

--------------

*CategoryListRQ* Example
''''''''''''''''''''''''

::

    <CategoryListRQ>
    </CategoryListRQ>

| 
| `toc <#toc>`__

--------------

*CategoryListRQ* Description
''''''''''''''''''''''''''''

Element

Number

Type

Description

| 
| `toc <#toc>`__

--------------

*CategoryListRS* Example
''''''''''''''''''''''''

::

    <CategoryListRS>
        <Categories>
            <Category>
                <Code>3*</Code>
                <Name>3 Estrellas</Name>
            </Category>
            <Category>
                <Code>3L</Code>
                <Name>3 Llaves</Name>
            </Category>
            ...
            <Category/>
        </Categories>
    </CategoryListRS>

| 
| `toc <#toc>`__

--------------

*CategoryListRS* Description
''''''''''''''''''''''''''''

Element

Number

Type

Description

| 
| `toc <#toc>`__

--------------

*RoomList* (Room Type List)
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Method Goals

| 
| This method aims to return a list of the available rooms code, which
will be used in the availability response.

Request Format

| 
| The request does not require any elements empty request.

Response Format

| 
| The result returns a list of *RoomInfo*.

Remarks

| 
| This message must be implemented solely in case it can not be provided
the description is room in the hotel availability. ( It is indicated in
*StaticConfiguration* )
| `toc <#toc>`__

--------------

*RoomListRQ* Example
''''''''''''''''''''

::

    <RoomListRQ>
    </RoomListRQ>

| 
| `toc <#toc>`__

--------------

*RoomListRQ* Description
''''''''''''''''''''''''

Element

Number

Type

Description

| 
| `toc <#toc>`__

--------------

*RoomListRS* Example
''''''''''''''''''''

::

    <RoomListRS>
        <RoomsInfo>
             <RoomInfo>
                 <Code>DBLSTD</Code>
                  <Name>Doble Estandard</Name>
            </RoomInfo>
            <RoomInfo>
                <Code>DBLSUP</Code>
                <Name>Doble Superior</Name>
            </RoomInfo>
                ...
            <RoomInfo/>
        </RoomsInfo>
    </RoomListRS>

| 
| `toc <#toc>`__

--------------

*RoomListRS* Description
''''''''''''''''''''''''

Element

Number

Type

Description

| 
| `toc <#toc>`__

--------------

*StaticConfiguration* (Static Configuration)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Method Goals

| 
| This message provides information about the static configuration of
the provider, to see and configure the provider in the best way.

Request Format

| 
| The request does not require any elements empty request.

Response Format

| 
| The XML returned contains more elements on the configuration (number
of hotels, the number of cities and the number of areas of availability,
if the provider returns the cancellation policies, maximum number of
distributions, maximum number of paxes in a distribution, release days,
stay minimum, list of languages that allows ....).

Remarks

| 
| `toc <#toc>`__

--------------

*StaticConfigurationRQ* Example
'''''''''''''''''''''''''''''''

::

    <StaticConfigurationRQ>
    </StaticConfigurationRQ>

| 
| `toc <#toc>`__

--------------

*StaticConfigurationRQ* Description
'''''''''''''''''''''''''''''''''''

Element

Number

Type

Description

| 
| `toc <#toc>`__

--------------

*StaticConfigurationRS* Example
'''''''''''''''''''''''''''''''

::

    <StaticConfigurationRS>
        <MaxNumberHotels>2000</MaxNumberHotels>
        <MaxNumberCities>1</MaxNumberCities>
        <MaxNumberZones>1</MaxNumberZones>
        <MaxNumberGeoCodes>0</MaxNumberGeoCodes>
        <RequiredRoomList>false</RequiredRoomList>
        <InformCancelPolicies>true</InformCancelPolicies>
        <InformBindingPriceValuation>true</InformBindingPriceValuation>
        <InformBindingPrice>true</InformBindingPrice>
        <InformNRFValuation>true</InformNRFValuation>
        <InformNRFRate>true</InformNRFRate>
        <Inform55Rate>true</Inform55Rate>
        <InformPackageRate>true</InformPackageRate>
        <InformExtraActivity>false</InformExtraActivity>
        <InformForfait>true</InformForfait>
        <RemarksValuation>true</RemarksValuation>
        <MaxNumberRoomCandidates>9</MaxNumberRoomCandidates>
        <MaxPaxInRoomCandidates>9</MaxPaxInRoomCandidates>
        <Release>0</Release>
        <MinimumStay>0</MinimumStay>
        <InformBillingSupplierReservation>false</InformBillingSupplierReservation>
        <ImplementsProvideLocatorReservationRead>true</ImplementsProvideLocatorReservationRead>
        <ImplementsClientLocatorReservationRead>true</ImplementsClientLocatorReservationRead>
        <ImplementsCancel>true</ImplementsCancel>
        <InformPriceReservation>true</InformPriceReservation>
        <HotelListLanguages>
            <Languages>
                <Language>en</Language>
                <Language>es</Language>
                <Language>de</Language>
                <Language>pt</Language>
                <Language>fr</Language>
                <Language>it</Language>
            </Languages>
        </HotelListLanguages>
        <ReservationListCreationDate>true</ReservationListCreationDate>
        <ReservationListCheckDate>true</ReservationListCheckDate>
        <HotelListType>OffLineCompleted</HotelListType>
        <DescriptiveInfoType>NotImplemented</DescriptiveInfoType>
        <GeographicDestinationTreeType>OffLine</GeographicDestinationTreeType>
        <AvailDestinationTreeType>OffLine</AvailDestinationTreeType>
        <ListadoServicios>OnLine</ListadoServicios>
        <RoomListType>OnLine</RoomListType>
        <DescriptiveInfoParallelism>-1</DescriptiveInfoParallelism>
        <InformCancelPoliciesReservationRead>false</InformCancelPoliciesReservationRead>
        <InformCancelPoliciesReservationList>false</InformCancelPoliciesReservationList>
        <InformCancelPoliciesAvail>false</InformCancelPoliciesAvail>
        <InformChangesPolicies>false</InformChangesPolicies>
        <ImplementsDeltaPrice>false</ImplementsDeltaPrice>
        <RequiredAllPassengers>true</RequiredAllPassengers>
        <InformBedsAvail>false</InformBedsAvail>
        <ModifyTransactions>
            <ModifyTransaction>
                <Modify>ModifyStartDateAddDays</Modify>
                <Modify>ModifyEndDateAddDays</Modify>
            </ModifyTransaction>
            <ModifyTransaction>
                <Modify>ModifyHolder</Modify>
                <Modify>ModifyRoomsAddRooms</Modify>
                <Modify>ModifyRoomsRemoveRooms</Modify>
            </ModifyTransaction>
        </ModifyTransactions>
    </StaticConfigurationRS>

| 
| `toc <#toc>`__

--------------

*StaticConfigurationRS* Description
'''''''''''''''''''''''''''''''''''

Element

Number

Type

Description

| 
| `toc <#toc>`__

--------------

*RuntimeConfiguration* (RunTime Configuration)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Method Goals

| 
| This message lets you know the provider configuration template.

Request Format

| 
| The request does not require any elements empty request.

Response Format

| 
| The returned XML contains a template of all fields used by the
provider.

Remarks

| 
| `toc <#toc>`__

--------------

*RuntimeConfigurationRQ* Example
''''''''''''''''''''''''''''''''

::

    <RuntimeConfigurationRQ>
    </RuntimeConfigurationRQ>

| 
| `toc <#toc>`__

--------------

*RuntimeConfigurationRQ* Description
''''''''''''''''''''''''''''''''''''

Element

Number

Type

Description

| 
| `toc <#toc>`__

--------------

*RuntimeConfigurationRS* Example
''''''''''''''''''''''''''''''''

::

    <RuntimeConfigurationRS>
        <Configuration>
            <User/>
            <Password/>
            <UrlGeneric/>
            <Parameters>
                <Parameter key = "agencia" value = ""/>
            </Parameters>
        </Configuration>
    </RuntimeConfigurationRS>

| 
| `toc <#toc>`__

--------------

*ConfiguracionRunTimeRS* Description
''''''''''''''''''''''''''''''''''''

Element

Number

Type

Description

| 
| `toc <#toc>`__

--------------

*ModifyValuation* (Modify Valuation)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Method Goals

| 
| This message lets you know if it is possible a modify, and new price
of that.

Request Format

| 
| The request require the reservation and all modifications will be
apply ( these will depend on what is specified in the
*StaticConfiguration* )

Response Format

| 
| The XML returned contains a simulation of the new booking.

Remarks

| 
| `toc <#toc>`__

--------------

*ModifyValuationRQ* Example
'''''''''''''''''''''''''''

::

    <ModifyValuationRQ>
        <Reservation>
            <Locators>
                <Client>5356342</Client>
                <Provider>MGNZ12345</Provider>
            </Locators>
            <Currency>EUR</Currency>
            <StartDate>28/01/2014</StartDate>
            <EndDate>29/01/2014</EndDate>
            <CreationDate>17/01/2014</CreationDate>
        </Reservation>
        <Modifications>
            <ModifyStartDateAddDays>
                <StartDate>29/01/2014</StartDate>
            </ModifyStartDateAddDays>
            <ModifyEndDateAddDays>
                <EndDate>30/01/2014</EndDate>
            </ModifyEndDateAddDays>
             <ModifyHolder>
                <Holder name = "Test11Modify" surname = "TestSur11Modify"/>
            </ModifyHolder>
            <ModifyRoomsAddRooms>
                <Rooms>
                    <Room code = "506">
                        <PaxGuests>
                            <PaxGuest age = "30">
                                <GivenName>name1</GivenName>
                                <SurName>surname1</SurName>
                            </PaxGuest>
                            <PaxGuest age = "30">
                                <GivenName>name2</GivenName>
                                <SurName>surname2</SurName>
                            </PaxGuest>
                        </PaxGuests>
                    </Room>
                </Rooms>
            </ModifyRoomsAddRooms>
            <ModifyRoomsRemoveRooms>
                <Rooms>
                    <Room code = "500">
                        <Price currency = "EUR" amount = "36.20" binding = "false" commission = "-1"/>
                    </Room>
                </Rooms>
            </ModifyRoomsRemoveRooms>
        </Modifications>
    </ModifyValuationRQ>

| 
| `toc <#toc>`__

--------------

*ModifyValuationRQ* Description
'''''''''''''''''''''''''''''''

| 

+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Element                                                                     | Number   | Type      | Description                                                                                                                                              |
+=============================================================================+==========+===========+==========================================================================================================================================================+
| ModifyValuationRQ                                                           | 1        |           | Root node.                                                                                                                                               |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Reservation                                                                 | 1        |           | Reservaton data.                                                                                                                                         |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Reservation/Locators                                                        | 1        |           | Information of the locators (it is mandatory indicate one of two, or client or provider).                                                                |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Reservation/Locators/Client                                                 | 0..1     | String    | Client locator.                                                                                                                                          |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Reservation/Locators/Provider                                               | 0..1     | String    | Provider locator.                                                                                                                                        |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Reservation/Currency                                                        | 1        | String    | Currency code.                                                                                                                                           |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Reservation/StartDate                                                       | 1        | String    | Start date of booking.                                                                                                                                   |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Reservation/EndDate                                                         | 1        | String    | End date of booking.                                                                                                                                     |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Reservation/CreationDate                                                    | 1        | String    | Creation date of booking.                                                                                                                                |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications                                                               | 1        |           | Modifications.                                                                                                                                           |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyStartDateAddDays                                        | 0..1     |           | Add days of check-in.                                                                                                                                    |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyStartDateAddDays/StartDate                              | 1        | String    | New check-in.                                                                                                                                            |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyStartDateSubtractDays                                   | 0..1     |           | Substract days of check-in.                                                                                                                              |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyStartDateSubtractDays/StartDate                         | 1        | String    | New chekc-in.                                                                                                                                            |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyEndDateAddDays                                          | 0..1     |           | Add days of check-out.                                                                                                                                   |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyEndDateAddDays/EndDate                                  | 1        | String    | New check-out.                                                                                                                                           |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyEndtDateSubtractDays                                    | 0..1     |           | Substract days of check-out.                                                                                                                             |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyEndtDateSubtractDays/EndDate                            | 1        | String    | New check-out.                                                                                                                                           |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyHolder                                                  | 0..1     |           | Modify holder.                                                                                                                                           |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyHolder/Holder                                           | 1        |           | New holder.                                                                                                                                              |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@name*                                                                     | 1        | String    | Holder name.                                                                                                                                             |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@surname*                                                                  | 1        | String    | Holder surname.                                                                                                                                          |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsAddRooms                                           | 0..1     |           | Add Rooms structure.                                                                                                                                     |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsAddRooms/Rooms                                     | 1        |           | Rooms Add.                                                                                                                                               |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsAddRooms/Rooms/Room                                | 1..n     |           | Room Add.                                                                                                                                                |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@code*                                                                     | 1        | String    | Room code.                                                                                                                                               |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsAddRooms/Rooms/Room/PaxGuests                      | 1        |           | List of passenger.                                                                                                                                       |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsAddRooms/Rooms/Room/PaxGuests/PaxGuest             | 1..n     |           | Detail of each passenger.                                                                                                                                |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@age*                                                                      | 1        | String    | Age pax.                                                                                                                                                 |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsAddRooms/Rooms/Room/PaxGuests/PaxGuest/GivenName   | 1        | String    | Given Name.                                                                                                                                              |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsAddRooms/Rooms/Room/PaxGuests/PaxGuest/SurName     | 1        | String    | Surname.                                                                                                                                                 |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsRemoveRooms                                        | 0..1     |           | Remove Rooms structure.                                                                                                                                  |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsRemoveRooms/Rooms                                  | 1        |           | Rooms Remove.                                                                                                                                            |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsRemoveRooms/Rooms/Room                             | 1..n     |           | Room Remove.                                                                                                                                             |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@code*                                                                     | 1        | String    | Room code.                                                                                                                                               |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsRemoveRooms/Rooms/Room/Price                       | 1        |           | Price Room.                                                                                                                                              |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@currency*                                                                 | 1        | String    | Currency code.                                                                                                                                           |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@amount*                                                                   | 1        | Decimal   | Room Amount.                                                                                                                                             |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@binding*                                                                  | 1        | Boolean   | Identifies if is the price is binding ( When true the sale price returned **must** not be less than the price informed.                                  |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@commission*                                                               | 1        | Decimal   | Commission ( -1 = not specified (will come indicated with the provider contract ), 0 = net price, X = % of the commission that applies to the amount).   |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+

| 
| `toc <#toc>`__

--------------

*ModifyValuationRS* Example
'''''''''''''''''''''''''''

::

    <ModifyValuationRS>
        <ModifyPenalty currency = "EUR" amount = "0" binding = "false" commission = "-1"/>
        <HotelReservation>
           <Price currency = "EUR" amount = "86.20" binding = "false" commission = "-1"/>
        </HotelReservation>
        <Parameters>
            <Parameter key = "bd1" value = "43"/>
        </Parameters>
    </ModifyValuationRS>

| 
| `toc <#toc>`__

--------------

*ModifyValuationRS* Description
'''''''''''''''''''''''''''''''

| 

+--------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Element                  | Number   | Type      | Description                                                                                                                                              |
+==========================+==========+===========+==========================================================================================================================================================+
| ModifyValuationRS        | 1        |           | Root node.                                                                                                                                               |
+--------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| ModifyPenalty            | 1        |           | Price of penalty modification.                                                                                                                           |
+--------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@currency*              | 1        | String    | Currency code.                                                                                                                                           |
+--------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@amount*                | 1        | Decimal   | Penalty Amount.                                                                                                                                          |
+--------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@binding*               | 1        | Boolean   | Identifies if is the price is binding ( When true the sale price returned **must** not be less than the price informed.                                  |
+--------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@commission*            | 1        | Decimal   | Commission ( -1 = not specified (will come indicated with the provider contract ), 0 = net price, X = % of the commission that applies to the amount).   |
+--------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| HotelReservation         | 1        |           | HotelReservation.                                                                                                                                        |
+--------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| HotelReservation/Price   | 1        |           | New total reservation price.                                                                                                                             |
+--------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@currency*              | 1        | String    | Currency code.                                                                                                                                           |
+--------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@amount*                | 1        | Decimal   | Reservation Amount.                                                                                                                                      |
+--------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@binding*               | 1        | Boolean   | Identifies if is the price is binding ( When true the sale price returned **must** not be less than the price informed.                                  |
+--------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@commission*            | 1        | Decimal   | Commission ( -1 = not specified (will come indicated with the provider contract ), 0 = net price, X = % of the commission that applies to the amount).   |
+--------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Parameters               | 0..1     |           | Parameters for additional information.                                                                                                                   |
+--------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Parameters/Parameter     | 1..n     |           | List of parameter.                                                                                                                                       |
+--------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@key*                   | 1        | String    | Contains the keyword/Id to identify a parameter.                                                                                                         |
+--------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@value*                 | 1        | String    | Contains the value of the parameter.                                                                                                                     |
+--------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+

| 
| `toc <#toc>`__

--------------

| 

*ModifyReservation* (Modify Reservation)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Method Goals

| 
| This message confirm a modification

Request Format

| 
| The request require the valuation returned for ModifyValuationRS

Response Format

| 
| The XML returned contains a confirmation booking

Remarks

| 
| `toc <#toc>`__

--------------

*ModifyReservationRQ* Example
'''''''''''''''''''''''''''''

::

    <ModifyReservationRQ>
        <Reservation>
            <Locators>
                <Client>5356342</Client>
                <Provider>MGNZ12345</Provider>
            </Locators>
            <Currency>EUR</Currency>
            <StartDate>28/01/2014</StartDate>
            <EndDate>29/01/2014</EndDate>
            <CreationDate>17/01/2014</CreationDate>
        </Reservation>
        <Modifications>
            <ModifyStartDateAddDays>
                <StartDate>29/01/2014</StartDate>
            </ModifyStartDateAddDays>
            <ModifyEndDateAddDays>
                <EndDate>30/01/2014</EndDate>
            </ModifyEndDateAddDays>
             <ModifyHolder>
                <Holder name = "Test11Modify" surname = "TestSur11Modify"/>
            </ModifyHolder>
            <ModifyRoomsAddRooms>
                <Rooms>
                    <Room code = "506">
                        <PaxGuests>
                            <PaxGuest age = "30">
                                <GivenName>name1</GivenName>
                                <SurName>surname1</SurName>
                            </PaxGuest>
                            <PaxGuest age = "30">
                                <GivenName>name2</GivenName>
                                <SurName>surname2</SurName>
                            </PaxGuest>
                        </PaxGuests>
                    </Room>
                </Rooms>
            </ModifyRoomsAddRooms>
            <ModifyRoomsRemoveRooms>
                <Rooms>
                    <Room code = "500">
                        <Price currency = "EUR" amount = "36.20" binding = "false" commission = "-1"/>
                    </Room>
                </Rooms>
            </ModifyRoomsRemoveRooms>
        </Modifications>
        <ModifyPenalty currency = "EUR" amount = "0" binding = "false" commission = "-1"/>
        <HotelReservation>
           <Price currency = "EUR" amount = "86.20" binding = "false" commission = "-1"/>
        </HotelReservation>
        <Parameters>
            <Parameter key = "bd1" value = "43"/>
        </Parameters>
    </ModifyReservationRQ>

| 
| `toc <#toc>`__

--------------

*ModifyReservationRQ* Description
'''''''''''''''''''''''''''''''''

| 

+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Element                                                                     | Number   | Type      | Description                                                                                                                                              |
+=============================================================================+==========+===========+==========================================================================================================================================================+
| ModifyReservationRQ                                                         | 1        |           | Root node.                                                                                                                                               |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Reservation                                                                 | 1        |           | Reservaton data.                                                                                                                                         |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Reservation/Locators                                                        | 1        |           | Information of the locators (it is mandatory indicate one of two, or client or provider).                                                                |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Reservation/Locators/Client                                                 | 0..1     | String    | Client locator.                                                                                                                                          |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Reservation/Locators/Provider                                               | 0..1     | String    | Provider locator.                                                                                                                                        |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Reservation/Currency                                                        | 1        | String    | Currency code.                                                                                                                                           |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Reservation/StartDate                                                       | 1        | String    | Start date of booking.                                                                                                                                   |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Reservation/EndDate                                                         | 1        | String    | End date of booking.                                                                                                                                     |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Reservation/CreationDate                                                    | 1        | String    | Creation date of booking.                                                                                                                                |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications                                                               | 1        |           | Modifications.                                                                                                                                           |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyStartDateAddDays                                        | 0..1     |           | Add days of check-in.                                                                                                                                    |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyStartDateAddDays/StartDate                              | 1        | String    | New check-in.                                                                                                                                            |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyStartDateSubtractDays                                   | 0..1     |           | Substract days of check-in.                                                                                                                              |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyStartDateSubtractDays/StartDate                         | 1        | String    | New chekc-in.                                                                                                                                            |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyEndDateAddDays                                          | 0..1     |           | Add days of check-out.                                                                                                                                   |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyEndDateAddDays/EndDate                                  | 1        | String    | New check-out.                                                                                                                                           |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyEndtDateSubtractDays                                    | 0..1     |           | Substract days of check-out.                                                                                                                             |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyEndtDateSubtractDays/EndDate                            | 1        | String    | New check-out.                                                                                                                                           |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyHolder                                                  | 0..1     |           | Modify holder.                                                                                                                                           |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyHolder/Holder                                           | 1        |           | New holder.                                                                                                                                              |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@name*                                                                     | 1        | String    | Holder name .                                                                                                                                            |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@surname*                                                                  | 1        | String    | Holder surname .                                                                                                                                         |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsAddRooms                                           | 0..1     |           | Add Rooms structure .                                                                                                                                    |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsAddRooms/Rooms                                     | 1        |           | Rooms Add.                                                                                                                                               |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsAddRooms/Rooms/Room                                | 1..n     |           | Room Add.                                                                                                                                                |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@code*                                                                     | 1        | String    | Room code.                                                                                                                                               |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsAddRooms/Rooms/Room/PaxGuests                      | 1        |           | List of passenger.                                                                                                                                       |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsAddRooms/Rooms/Room/PaxGuests/PaxGuest             | 1..n     |           | Detail of each passenger.                                                                                                                                |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@age*                                                                      | 1        | String    | Age pax.                                                                                                                                                 |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsAddRooms/Rooms/Room/PaxGuests/PaxGuest/GivenName   | 1        | String    | Given Name.                                                                                                                                              |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsAddRooms/Rooms/Room/PaxGuests/PaxGuest/SurName     | 1        | String    | Surname.                                                                                                                                                 |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsRemoveRooms                                        | 0..1     |           | Remove Rooms structure.                                                                                                                                  |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsRemoveRooms/Rooms                                  | 1        |           | Rooms Remove.                                                                                                                                            |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsRemoveRooms/Rooms/Room                             | 1..n     |           | Room Remove.                                                                                                                                             |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@code*                                                                     | 1        | String    | Room code.                                                                                                                                               |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Modifications/ModifyRoomsRemoveRooms/Rooms/Room/Price                       | 1        |           | Price Room                                                                                                                                               |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@currency*                                                                 | 1        | String    | Currency code.                                                                                                                                           |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@amount*                                                                   | 1        | Decimal   | Room Amount.                                                                                                                                             |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@binding*                                                                  | 1        | Boolean   | Identifies if is the price is binding ( When true the sale price returned **must** not be less than the price informed.                                  |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@commission*                                                               | 1        | Decimal   | Commission ( -1 = not specified (will come indicated with the provider contract ), 0 = net price, X = % of the commission that applies to the amount).   |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| ModifyPenalty                                                               | 1        |           | Price of penalty modification. (element returned in ModifyValuationRS)                                                                                   |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@currency*                                                                 | 1        | String    | Currency code.                                                                                                                                           |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@amount*                                                                   | 1        | Decimal   | Penalty Amount.                                                                                                                                          |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@binding*                                                                  | 1        | Boolean   | Identifies if is the price is binding ( When true the sale price returned **must** not be less than the price informed.                                  |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@commission*                                                               | 1        | Decimal   | Commission ( -1 = not specified (will come indicated with the provider contract ), 0 = net price, X = % of the commission that applies to the amount).   |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| HotelReservation                                                            | 1        |           | HotelReservation. (element returned in ModifyValuationRS)                                                                                                |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| HotelReservation/Price                                                      | 1        |           | New total reservation price.                                                                                                                             |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@currency*                                                                 | 1        | String    | Currency code.                                                                                                                                           |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@amount*                                                                   | 1        | Decimal   | Reservation Amount.                                                                                                                                      |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@binding*                                                                  | 1        | Boolean   | Identifies if is the price is binding ( When true the sale price returned **must** not be less than the price informed.                                  |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@commission*                                                               | 1        | Decimal   | Commission ( -1 = not specified (will come indicated with the provider contract ), 0 = net price, X = % of the commission that applies to the amount).   |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Parameters                                                                  | 0..1     |           | Parameters for additional information. (element returned in ModifyValuationRS)                                                                           |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Parameters/Parameter                                                        | 1..n     |           | List of parameter.                                                                                                                                       |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@key*                                                                      | 1        | String    | Contains the keyword/Id to identify a parameter.                                                                                                         |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@value*                                                                    | 1        | String    | Contains the value of the parameter.                                                                                                                     |
+-----------------------------------------------------------------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+

| 
| `toc <#toc>`__

--------------

*ModifyReservationRS* Example
'''''''''''''''''''''''''''''

::

    <ModifyReservationRS>
        <ProviderLocator>2323232</ProviderLocator>
        <Price currency = "EUR" amount = "86.20" binding = "false" commission = "-1"/>
        <ResStatus>OK</ResStatus>
    </ModifyReservationRS>

| 
| `toc <#toc>`__

--------------

*ModifyReservationRS* Description
'''''''''''''''''''''''''''''''''

| 

+---------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Element             | Number   | Type      | Description                                                                                                                                              |
+=====================+==========+===========+==========================================================================================================================================================+
| ModifyValuationRS   | 1        |           | Root node.                                                                                                                                               |
+---------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| ProviderLocator     | 1        | String    | Provider locator.                                                                                                                                        |
+---------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| ResStatus           | 1        | String    | Status of book (OK = confirmed, RQ = on request, CN = canceled, UN = unknown ).                                                                          |
+---------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Price               | 0..1     |           | Total price of this book.                                                                                                                                |
+---------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@currency*         | 1        | String    | Currency code.                                                                                                                                           |
+---------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@amount*           | 1        | Decimal   | Book Amount.                                                                                                                                             |
+---------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@binding*          | 1        | Boolean   | Identifies if is the price is binding ( When true the sale price returned **must** not be less than the price informed.                                  |
+---------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| *@commission*       | 1        | Decimal   | Commission ( -1 = not specified (will come indicated with the provider contract ), 0 = net price, X = % of the commission that applies to the amount).   |
+---------------------+----------+-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------+

| 
| `toc <#toc>`__

--------------

XML Travelgate - Edificio Europa, Local 1, bajos - ParcBIT, Palma de
Mallorca, Baleares +34 871 968 181 \|
`http://www.xmltravelgate.com <http://www.xmltravelgate.com/>`__ \| Free
`URL shortener <http://xml.tg>`__ by XML Travelgate \| Copyright 2014

.. |Logo XML Travelgate| image:: /Images/logo_small.png
