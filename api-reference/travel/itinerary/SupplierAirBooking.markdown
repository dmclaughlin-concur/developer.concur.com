# Travel Supplier Air Samples
This page outlines the use cases for a travel supplier to successfully post bookings to the Itinerary API.  

POSTMAN Collection Link

### What you will need to get started?
1. Create App LINK
2. JWT token LINK

# Use Case 1 - Air Booking (no ticket)

### Endpoint - https://www.concursolutions.com/api/travel/booking/v1.1?

### Params
TripID

userid_type

userid_value

### Request

```XML
    <Booking xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
		<DateBookedLocal>2015-12-06T23:59:00</DateBookedLocal>
    <!-- Record Locator is required & should be unique-->
		<RecordLocator>DJM9876</RecordLocator>
    <!-- Must be a valid booking source -->
		<BookingSource>Ethiad</BookingSource>
		<FareExpiresEmailDatetimeUtc>2015-12-08T20:00:00</FareExpiresEmailDatetimeUtc>
    <!-- FOPTypes (CC - Credit Card, CA - Corportae Account, CH- Cash) -->
		<FormOfPaymentType>CC</FormOfPaymentType>
		<Segments>
			<Air>
				<Status>HK</Status>
				<StartDateUtc>2015-12-28T19:03:00</StartDateUtc>
				<EndDateUtc>2015-12-29T00:50:00</EndDateUtc>
				<ConfirmationNumber>123DJM</ConfirmationNumber>
				<Vendor>Ethiad</Vendor>
				<OperatedByVendor/>
				<OperatedByVendorName/>
				<FlightNumber>357</FlightNumber>
				<AircraftCode>320</AircraftCode>
				<Cabin>Y</Cabin>
				<ClassOfService>S</ClassOfService>
				<Miles>2298</Miles>
				<Duration>347</Duration>
				<NumStops>0</NumStops>
				<StartCityCode>IAD</StartCityCode>
				<EndCityCode>SEA</EndCityCode>
				<StartTerminal/>
				<EndTerminal/>
				<Meals>F</Meals>
				<Bags/>
				<LegId>1</LegId>
				<ETicket>Y</ETicket>
				<CarbonEmissionLbs>889.325989</CarbonEmissionLbs>
				<CarbonModel>1</CarbonModel>
				<Seats>
					<AirSeat>
						<PassengerRph>1</PassengerRph>
						<SeatNumber>12C</SeatNumber>
					</AirSeat>
				</Seats>
			</Air>
			<Air>
				<Status>HK</Status>
				<StartDateUtc>2015-12-30T14:30:00</StartDateUtc>
				<EndDateUtc>2015-12-30T19:33:00</EndDateUtc>
				<ConfirmationNumber>123DJM</ConfirmationNumber>
				<Vendor>Ethiad</Vendor>
				<OperatedByVendor/>
				<OperatedByVendorName/>
				<FlightNumber>1444</FlightNumber>
				<AircraftCode>739</AircraftCode>
				<Cabin>Y</Cabin>
				<ClassOfService>L</ClassOfService>
				<Miles>2298</Miles>
				<Duration>303</Duration>
				<NumStops>0</NumStops>
				<StartCityCode>SEA</StartCityCode>
				<EndCityCode>IAD</EndCityCode>
				<StartTerminal/>
				<EndTerminal/>
				<Meals>F</Meals>
				<Bags/>
				<LegId>2</LegId>
				<ETicket>Y</ETicket>
				<CarbonEmissionLbs>889.325989</CarbonEmissionLbs>
				<CarbonModel>1</CarbonModel>
				<Seats>
					<AirSeat>
						<PassengerRph>1</PassengerRph>
						<SeatNumber>12D</SeatNumber>
					</AirSeat>
				</Seats>
			</Air>
		</Segments>
		<Passengers>
			<Passenger>
				<FrequentTravelerPrograms>
					<FrequentFlyer>
						<AirlineVendor>UA</AirlineVendor>
						<Description>MileagePlus</Description>
						<FrequentFlyerNumber>PU126160</FrequentFlyerNumber>
						<ProgramVendor>UA</ProgramVendor>
						<Status>1P</Status>
						<StatusExpirationDate>2015-12-31T23:59:00</StatusExpirationDate>
					</FrequentFlyer>
				</FrequentTravelerPrograms>
				<NameFirst>John</NameFirst>
				<NameLast>Smith</NameLast>
				<NameMiddle/>
				<NameTitle/>
			</Passenger>
		</Passengers>
    <!-- Delivery country is used to identify point of sale for PRISM reporting -->
	  <Delivery>
		  <Country>US</Country>
		  <Type>mail</Type>
	  </Delivery>
	</Booking>

```

### RESPONSE

### Concur Travel Display

### Concur Expense Display


# Use Case 2 - Air Booking (with ticket)

### Endpoint - https://www.concursolutions.com/api/travel/booking/v1.1?

### Params
TripID

userid_type

userid_value

### REQUEST

```XML

    <Booking xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
		<DateBookedLocal>2015-12-06T23:59:00</DateBookedLocal>
    <!-- Record Locator is required & should be unique-->
		<RecordLocator>DJM9876</RecordLocator>
    <!-- Must be a valid booking source -->
		<BookingSource>Ethiad</BookingSource>
		<FareExpiresEmailDatetimeUtc>2015-12-08T20:00:00</FareExpiresEmailDatetimeUtc>
    <!-- FOPTypes (CC - Credit Card, CA - Corportae Account, CH- Cash) -->
		<FormOfPaymentType>CC</FormOfPaymentType>
		<Segments>
			<Air>
				<Status>HK</Status>
				<StartDateUtc>2015-12-28T19:03:00</StartDateUtc>
				<EndDateUtc>2015-12-29T00:50:00</EndDateUtc>
				<ConfirmationNumber>123DJM</ConfirmationNumber>
				<Vendor>Ethiad</Vendor>
				<OperatedByVendor/>
				<OperatedByVendorName/>
				<FlightNumber>357</FlightNumber>
				<AircraftCode>320</AircraftCode>
				<Cabin>Y</Cabin>
				<ClassOfService>S</ClassOfService>
				<Miles>2298</Miles>
				<Duration>347</Duration>
				<NumStops>0</NumStops>
				<StartCityCode>IAD</StartCityCode>
				<EndCityCode>SEA</EndCityCode>
				<StartTerminal/>
				<EndTerminal/>
				<Meals>F</Meals>
				<Bags/>
				<LegId>1</LegId>
				<ETicket>Y</ETicket>
				<CarbonEmissionLbs>889.325989</CarbonEmissionLbs>
				<CarbonModel>1</CarbonModel>
				<Seats>
					<AirSeat>
						<PassengerRph>1</PassengerRph>
						<SeatNumber>12C</SeatNumber>
					</AirSeat>
				</Seats>
			</Air>
			<Air>
				<Status>HK</Status>
				<StartDateUtc>2015-12-30T14:30:00</StartDateUtc>
				<EndDateUtc>2015-12-30T19:33:00</EndDateUtc>
				<ConfirmationNumber>123DJM</ConfirmationNumber>
				<Vendor>Ethiad</Vendor>
				<OperatedByVendor/>
				<OperatedByVendorName/>
				<FlightNumber>1444</FlightNumber>
				<AircraftCode>739</AircraftCode>
				<Cabin>Y</Cabin>
				<ClassOfService>L</ClassOfService>
				<Miles>2298</Miles>
				<Duration>303</Duration>
				<NumStops>0</NumStops>
				<StartCityCode>SEA</StartCityCode>
				<EndCityCode>IAD</EndCityCode>
				<StartTerminal/>
				<EndTerminal/>
				<Meals>F</Meals>
				<Bags/>
				<LegId>2</LegId>
				<ETicket>Y</ETicket>
				<CarbonEmissionLbs>889.325989</CarbonEmissionLbs>
				<CarbonModel>1</CarbonModel>
				<Seats>
					<AirSeat>
						<PassengerRph>1</PassengerRph>
						<SeatNumber>12D</SeatNumber>
					</AirSeat>
				</Seats>
			</Air>
		</Segments>
    <AirlineTickets>
    		<AirlineTicket>
    			<AirlineTicketCoupons>
    				<AirlineTicketCoupon>
              <!-- CouponNumber is sequential order of Coupons for ticket-->
    					<CouponNumber>1</CouponNumber>
              <!-- Vendor code -->
    					<Vendor>UA</Vendor>
    					<FlightNumber>357</FlightNumber>
    					<ClassOfService>S</ClassOfService>
    					<RateCode>SE143KS/8N02</RateCode>
    					<StartDateLocal>2014-11-28T15:03:00</StartDateLocal>
    					<StartCityCode>IAD</StartCityCode>
    					<EndCityCode>SEA</EndCityCode>
              <!-- Valid Coupon Statuses (OPEN, EXCHANGED, REFUNDED, USED, VOID, etc.. ) -->
    					<CouponStatus>OPEN</CouponStatus>
    					<NotValidBeforeDate>2015-12-28T00:00:00</NotValidBeforeDate>
    					<NotValidAfterDate>2015-12-28T00:00:00</NotValidAfterDate>
    				</AirlineTicketCoupon>
    				<AirlineTicketCoupon>
    					<CouponNumber>2</CouponNumber>
    					<Vendor>UA</Vendor>
    					<FlightNumber>1444</FlightNumber>
    					<ClassOfService>L</ClassOfService>
    					<RateCode>LE73KS/8N02</RateCode>
    					<StartDateLocal>2014-11-30T07:30:00</StartDateLocal>
    					<StartCityCode>SEA</StartCityCode>
    					<EndCityCode>IAD</EndCityCode>
    					<CouponStatus>OPEN</CouponStatus>
    					<NotValidBeforeDate>2015-12-30T00:00:00</NotValidBeforeDate>
    					<NotValidAfterDate>2015-12-30T00:00:00</NotValidAfterDate>
    				</AirlineTicketCoupon>
    			</AirlineTicketCoupons>
    			<Taxes>
    				<Tax>
    					<TaxType>US</TaxType>
    					<TaxAmount>27.6900</TaxAmount>
    				</Tax>
    				<Tax>
    					<TaxType>ZP</TaxType>
    					<TaxAmount>7.8000</TaxAmount>
    				</Tax>
    				<Tax>
    					<TaxType>XT</TaxType>
    					<TaxAmount>14.0000</TaxAmount>
    				</Tax>
    			</Taxes>
    			<AirlineTicketExchanges/>
    			<AirlineCharges/>
    			<InvoiceNumber/>
          <!--3 character carrier code from ticket-->
    			<PlatingCarrierNumericCode>016</PlatingCarrierNumericCode>
          <!-- Rest of ticket number 10 characters -->
    			<PlatingControlNumber>7249117982</PlatingControlNumber>
    			<IssueDateTime>2015-09-07T23:59:00</IssueDateTime>
    			<IssueDateTimeUTC xsi:nil="true"/>
    			<PassengerName>Smith/John</PassengerName>
    			<BaseFare>369.2100</BaseFare>
    			<BaseFareCurrency>USD</BaseFareCurrency>
    			<BaseFareNuc xsi:nil="true"/>
    			<TotalFare>418.7000</TotalFare>
    			<TotalFareCurrency>USD</TotalFareCurrency>
          <!--Need to add details here for each use case -->
    			<AddCollectAmount>0</AddCollectAmount>
    			<LinearFareConstructor>WAS UA SEA214.24UA WAS154.97 USD369.21END UA ZPIADSEA XT5.00AY9.00XFIAD4.5SEA4.5</LinearFareConstructor>
    			<TicketType>E</TicketType>
    		</AirlineTicket>
    </AirlineTickets>
		<Passengers>
			<Passenger>
				<FrequentTravelerPrograms>
					<FrequentFlyer>
						<AirlineVendor>UA</AirlineVendor>
						<Description>MileagePlus</Description>
						<FrequentFlyerNumber>PU126160</FrequentFlyerNumber>
						<ProgramVendor>UA</ProgramVendor>
						<Status>1P</Status>
						<StatusExpirationDate>2015-12-31T23:59:00</StatusExpirationDate>
					</FrequentFlyer>
				</FrequentTravelerPrograms>
				<NameFirst>John</NameFirst>
				<NameLast>Smith</NameLast>
				<NameMiddle/>
				<NameTitle/>
			</Passenger>
		</Passengers>
    <!-- Delivery country is used to identify point of sale for PRISM reporting -->
	  <Delivery>
		  <Country>US</Country>
		  <Type>mail</Type>
	  </Delivery>
	</Booking>



      
```
# Use Case 3 - Update Coupon Status

### Endpoint - https://www.concursolutions.com/api/travel/booking/v1.1/UpdateCoupon?

### Request

````XML
<Booking xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <RecordLocator>DJM1013</RecordLocator>
    <PlatingCarrierNumericCode>016</PlatingCarrierNumericCode>
    <PlatingControlNumber>7249117982</PlatingControlNumber>
    <AirlineTicketCoupon>
        <ClassOfService>S</ClassOfService>
        <CouponNumber>1</CouponNumber>
        <CouponStatus>OPEN</CouponStatus>
        <EndCityCode>SEA</EndCityCode>
        <FlightNumber>357</FlightNumber>
        <NotValidAfterDate>2016-05-28T00:00:00</NotValidAfterDate>
        <NotValidBeforeDate>2016-05-28T00:00:00</NotValidBeforeDate>
        <RateCode>SE143KS/8N02</RateCode>
        <StartCityCode>IAD</StartCityCode>
        <StartDateLocal>2016-05-28T15:03:00</StartDateLocal>
        <Vendor>UA</Vendor>
    </AirlineTicketCoupon>
</Booking>

```

### Response

# Use Case 4 - Ticket Exchange

# Use Case 5 - Partial Refund

# Use Case 6 - Full Refund

# Use Case 7 - Cancel Booking

### EndPoint - https://www.concursolutions.com/api/travel/booking/v1.0?

### Params

bookingsource

Vendor

confirmationnumber

### Request

https://www.concursolutions.com/api/travel/booking/v1.0?bookingsource=Test Car Vendor&confirmationnumber=F16726AIUS


## Enumerated Fields
Coupon Status

Form Of Payment Type

## FAQ
1. What is the tripID & as a supplier do I need to store it?


