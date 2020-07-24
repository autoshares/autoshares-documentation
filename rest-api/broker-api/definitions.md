# Terms and Definitions

## Definitions

### AccountEditableModel

| Name | Description | Schema |
| :--- | :--- | :--- |
| **BaseCash**   _optional_ |  | number \(double\) |
| **Cash**   _optional_ |  | number \(double\) |
| **CashInterestRate**   _optional_ | **Minimum value** : `0` | number \(double\) |
| **Cip**   _optional_ |  | number \(double\) |
| **ClearingAccount**   _required_ |  | string |
| **ClearingFirm**   _optional_ |  | string |
| **CloseEquity**   _optional_ |  | number \(double\) |
| **CommissionPlan**   _optional_ |  | string |
| **CreatedDate**   _optional_ |  | string \(date-time\) |
| **Currency**   _required_ |  | string |
| **DayTradeCall**   _optional_ |  | number \(double\) |
| **DayTrades**   _optional_ | **Minimum value** : `0`   **Maximum value** : `2147483647` | integer \(int32\) |
| **DayTradingBuyingPower**   _optional_ |  | number \(double\) |
| **Enabled**   _optional_ |  | boolean |
| **EquityCall**   _optional_ |  | number \(double\) |
| **ExcessEquity**   _optional_ |  | number \(double\) |
| **HouseCall**   _optional_ |  | number \(double\) |
| **InitialCall**   _optional_ |  | number \(double\) |
| **IsAverageAccount**   _optional_ |  | boolean |
| **IsChanged**   _optional_ |  | boolean |
| **MaintenanceCall**   _optional_ |  | number \(double\) |
| **MarginEquity**   _optional_ |  | number \(double\) |
| **MarginInterestRate**   _optional_ | **Minimum value** : `0` | number \(double\) |
| **MarginType**   _optional_ |  | enum \(Empty, Cash, Margin, DayTrader, MarginIra\) |
| **ModifiedDate**   _optional_ |  | string \(date-time\) |
| **MoneyMarket**   _optional_ |  | number \(double\) |
| **OpenExcess**   _optional_ |  | number \(double\) |
| **OptionLevel**   _optional_ | **Minimum value** : `0`   **Maximum value** : `2147483647` | integer \(int32\) |
| **OwnerType**   _optional_ |  | enum \(IndividualCustomer, InstitutionalCustomer, Combined, EmployeeAccount, MarketMaking, OtherProprietary, Unknown, ErrorAccount\) |
| **Permissions**   _optional_ |  | enum \(Empty, LongStock, ShortStock, LongOption, ShortOption, AllowTrade, AllowMargin, AllowOpen\) |
| **RepCode**   _optional_ |  | string |
| **SmaBalance**   _optional_ |  | number \(double\) |
| **Status**   _optional_ |  | enum \(UnSpecified, New, SentToClearing, Approved, Rejected\) |
| **SubscriptionPlanId**   _optional_ | **Minimum value** : `1`   **Maximum value** : `2147483647` | integer \(int32\) |
| **Sweep**   _optional_ |  | number \(double\) |
| **TradeDayBalance**   _optional_ |  | number \(double\) |

### AccountModel

| Name | Schema |
| :--- | :--- |
| **BaseCash**   _optional_ | number \(double\) |
| **Cash**   _optional_ | number \(double\) |
| **CashInterestRate**   _optional_ | number \(double\) |
| **Cip**   _optional_ | number \(double\) |
| **ClearingAccount**   _optional_ | string |
| **ClearingFirm**   _optional_ | string |
| **CloseEquity**   _optional_ | number \(double\) |
| **CommissionPlan**   _optional_ | string |
| **CreatedDate**   _optional_ | string \(date-time\) |
| **Currency**   _optional_ | string |
| **DayTradeCall**   _optional_ | number \(double\) |
| **DayTrades**   _optional_ | integer \(int32\) |
| **DayTradingBuyingPower**   _optional_ | number \(double\) |
| **Enabled**   _optional_ | boolean |
| **EquityCall**   _optional_ | number \(double\) |
| **ExcessEquity**   _optional_ | number \(double\) |
| **HouseCall**   _optional_ | number \(double\) |
| **Id**   _optional_ | integer \(int32\) |
| **InitialCall**   _optional_ | number \(double\) |
| **IsAverageAccount**   _optional_ | boolean |
| **IsChanged**   _optional_ | boolean |
| **MaintenanceCall**   _optional_ | number \(double\) |
| **MarginEquity**   _optional_ | number \(double\) |
| **MarginInterestRate**   _optional_ | number \(double\) |
| **MarginType**   _optional_ | enum \(Empty, Cash, Margin, DayTrader, MarginIra\) |
| **ModifiedDate**   _optional_ | string \(date-time\) |
| **MoneyMarket**   _optional_ | number \(double\) |
| **OpenExcess**   _optional_ | number \(double\) |
| **OptionLevel**   _optional_ | integer \(int32\) |
| **OwnerType**   _optional_ | enum \(IndividualCustomer, InstitutionalCustomer, Combined, EmployeeAccount, MarketMaking, OtherProprietary, Unknown, ErrorAccount\) |
| **Permissions**   _optional_ | enum \(Empty, LongStock, ShortStock, LongOption, ShortOption, AllowTrade, AllowMargin, AllowOpen\) |
| **RepCode**   _optional_ | string |
| **SmaBalance**   _optional_ | number \(double\) |
| **Status**   _optional_ | enum \(UnSpecified, New, SentToClearing, Approved, Rejected\) |
| **SubscriptionPlanId**   _optional_ | integer \(int32\) |
| **Sweep**   _optional_ | number \(double\) |
| **TradeDayBalance**   _optional_ | number \(double\) |

### AccountValueItem

| Name | Schema |
| :--- | :--- |
| **Date**   _optional_ | string \(date-time\) |
| **Value**   _optional_ | number \(double\) |

### AllocationLegInfo

| Name | Schema |
| :--- | :--- |
| **Action**   _optional_ | enum \(Buy, Sell, SellShort, BuyToCover, SellToClose, BuyToClose, SellToOpen, BuyToOpen\) |
| **Price**   _optional_ | number \(double\) |
| **Quantity**   _optional_ | number \(double\) |
| **Symbol**   _optional_ | string |

### AllocationResultInfo\[MultilegAllocationRequest\]

Allocation request result

| Name | Description | Schema |
| :--- | :--- | :--- |
| **Description**   _optional_ | Error description | string |
| **IsSucceed**   _optional_ | Is allocation request was successfully processed | boolean |
| **Request**   _optional_ |  | [MultilegAllocationRequest](definitions.md#multilegallocationrequest) |

### AllocationResultInfo\[SimpleAllocationRequest\]

Allocation request result

| Name | Description | Schema |
| :--- | :--- | :--- |
| **Description**   _optional_ | Error description | string |
| **IsSucceed**   _optional_ | Is allocation request was successfully processed | boolean |
| **Request**   _optional_ |  | [SimpleAllocationRequest](definitions.md#simpleallocationrequest) |

### AppKey

| Name | Schema |
| :--- | :--- |
| **CompanyId**   _optional_   _read-only_ | integer \(int32\) |
| **Description**   _optional_   _read-only_ | string |
| **Enabled**   _optional_   _read-only_ | boolean |
| **Id**   _optional_   _read-only_ | integer \(int32\) |
| **Key**   _optional_   _read-only_ | string |
| **Type**   _optional_   _read-only_ | enum \(FrontOffice, Mobile, Custom\) |

### ChartCompareRequestModel

| Name | Schema |
| :--- | :--- |
| **Securities**   _optional_ | &lt; [SecuritySignature](definitions.md#securitysignature) &gt; array |
| **SecuritiesHistorySettings**   _optional_ | [SecurityHistoryRequestSettings](definitions.md#securityhistoryrequestsettings) |

### ChartHistoryModel

| Name | Schema |
| :--- | :--- |
| **IndicatorsHistory**   _optional_ | &lt; &lt; [IndicatorHistoryMapModel](definitions.md#indicatorhistorymapmodel) &gt; array &gt; array |
| **SecurityHistory**   _optional_ | &lt; &lt; [TimeSeriesValueCandleMapModel](definitions.md#timeseriesvaluecandlemapmodel) &gt; array &gt; array |
| **SupportResistanceHistory**   _optional_ | [SupportResistanceMapModel](definitions.md#supportresistancemapmodel) |

### ChartHistoryRequestModel

| Name | Schema |
| :--- | :--- |
| **IndicatorsHistorySettings**   _optional_ | &lt; [IndicatorHistoryRequestSettings](definitions.md#indicatorhistoryrequestsettings) &gt; array |
| **Security**   _optional_ | [SecuritySignature](definitions.md#securitysignature) |
| **SecurityHistorySettings**   _optional_ | [SecurityHistoryRequestSettings](definitions.md#securityhistoryrequestsettings) |

### ClearingAction

System action

| Name | Description | Schema |
| :--- | :--- | :--- |
| **Disabled**   _optional_ | Is action disabled | boolean |
| **Handlers**   _optional_ | List of actions handlers | &lt; [ClearingActionHandler](definitions.md#clearingactionhandler) &gt; array |
| **Name**   _optional_ | System action name | string |

### ClearingActionHandler

System action handler

| Name | Description | Schema |
| :--- | :--- | :--- |
| **Name**   _optional_ | Action handler name | string |
| **Parameters**   _optional_ | Set of handler parameters | &lt; string, string &gt; map |

### CreateAppKey

| Name | Schema |
| :--- | :--- |
| **Description**   _optional_ | string |
| **KeyType**   _optional_ | enum \(FrontOffice, Mobile, Custom\) |

### CreateOrderResource

| Name | Description | Schema |
| :--- | :--- | :--- |
| **ClientId**   _optional_ | Client order id. | string |
| **Exchange**   _optional_ | Desired exchange. | string |
| **ExecInst**   _optional_ | Execution instruction. | enum \(DoNotIncrease, DoNotReduce, AllOrNone\) |
| **ExecutionInstructions**   _optional_ | Algo order execution instructions. | &lt; string, string &gt; map |
| **ExpireDate**   _optional_ | Expire date. Assigned by client. | string \(date-time\) |
| **ExtendedHours**   _optional_ | indicates the extended trading session for GTX order execution \(pre-market session, post-market session\) if empty - than there is no specific requirement for extended session | string |
| **Legs**   _optional_ | Order legs | &lt; [CreateOrderResource](definitions.md#createorderresource) &gt; array |
| **Price**   _optional_ | Price \(not used for some order types\). | number \(double\) |
| **Quantity**   _optional_ | Quantity. Assigned by client.   **Minimum value** : `0` | number \(double\) |
| **Side**   _optional_ | Client side comments. | enum \(Buy, Sell, SellShort, BuyToCover\) |
| **StopPrice**   _optional_ | Stop price \(used for stop orders\). | number \(double\) |
| **Symbol**   _optional_ | Security symbol. | string |
| **TimeInforce**   _optional_ | Time in force. | enum \(Day, GoodTillCancel, AtTheOpening, ImmediateOrCancel, FillOrKill, GoodTillCrossing, GoodTillDate, GoodTillTime\) |
| **Token**   _optional_ | Additional identity key \(usid in market scanner\). | string |
| **TrailingLimitAmount**   _optional_ |  | number \(double\) |
| **TrailingLimitAmountType**   _optional_ |  | enum \(Absolute, Persentage\) |
| **TrailingStopAmount**   _optional_ |  | number \(double\) |
| **TrailingStopAmountType**   _optional_ |  | enum \(Absolute, Persentage\) |
| **Type**   _optional_ | Type. Assigned by client. | enum \(Market, Limit, Stop, StopLimit, Pegged, TrailingStop, TrailingStopLimit, OneCancelOther, OneTriggerOther, OneTriggerOneCancelOther, External\) |
| **ValidationsToBypass**   _optional_ | Flag property indicating validation rules to bypass | integer \(int32\) |

### CreateUserModel

| Name | Schema |
| :--- | :--- |
| **EmailAddress**   _optional_ | string |
| **Enabled**   _optional_ | boolean |
| **EntitlementsPhoneNumber**   _optional_ | string |
| **ExpirationDate**   _optional_ | string \(date-time\) |
| **FirstName**   _optional_ | string |
| **LastName**   _optional_ | string |
| **Login**   _optional_ | string |
| **Middle**   _optional_ | string |
| **PhoneNumber**   _optional_ | string |
| **Salutation**   _optional_ | enum \(NoSalutation, Mr, Mrs, Ms, Dr, Sir, Madam\) |
| **Suffix**   _optional_ | enum \(NoSuffix, Jr, Sr, Second, Third, Fourth\) |
| **TimeZoneInfoId**   _optional_ | string |

### CreateWatchlistModel

| Name | Schema |
| :--- | :--- |
| **Name**   _optional_ | string |
| **Securities**   _optional_ | &lt; integer \(int32\) &gt; array |

### EditableHotkeyModel

| Name | Schema |
| :--- | :--- |
| **ActionId**   _optional_ | integer \(int32\) |
| **Description**   _optional_ | string |
| **KeyboardShortcut**   _optional_ | string |
| **Parameters**   _optional_ | &lt; [HotkeyParameterMapModel](definitions.md#hotkeyparametermapmodel) &gt; array |

### EquityResource

| Name | Schema |
| :--- | :--- |
| **AddedDate**   _optional_ | string \(date-time\) |
| **AllowMargin**   _optional_ | boolean |
| **AllowShort**   _optional_ | boolean |
| **AllowTrade**   _optional_ | boolean |
| **Currency**   _optional_ | string |
| **Description**   _optional_ | string |
| **Enabled**   _optional_ | boolean |
| **Exchange**   _optional_ | string |
| **Id**   _optional_ | integer \(int32\) |
| **ModifyDate**   _optional_ | string \(date-time\) |
| **Precision**   _optional_ | integer \(int32\) |
| **Symbol**   _optional_ | string |
| **TickSize**   _optional_ | number \(double\) |
| **Type**   _optional_ | enum \(BankersAcceptance, CertificateOfDeposit, CollateralizeMortgageObligation, CorporateBond, CommercialPaper, CorporatePrivatePlacement, CommonStock, FederalHousingAuthority, FederalHomeLoan, FederalNationalMortgageAssociation, ForeignExchangeContract, Future, GovernmentNationalMortgageAssociation, TreasuriesPlusAgencyDebenture, MutualFund, MortgageInterestOnly, MortgagePrincipleOnly, MortgagePrivatePlacement, MiscellaneousPassThru, MunicipalBond, NoIsitcSecurityType, Option, PreferredStock, RepurchaseAgreement, ReverseRepurchaseAgreement, StudentLoanMarketingAssociation, TimeDeposit, UsTreasuryBill, Warrant, CatsTigersLions, WildcardEntry, ConvertibleBond, MortgageIoette, Index, FakeStockForNonStandartOption, Right, Cryptocurrency, ETF, DepositoryReceipt, CoveredWarrant, Unit\) |
| **VolumePrecision**   _optional_ | integer \(int32\) |

### Expecting

| Name | Schema |
| :--- | :--- |
| **Reason**   _optional_ | string |
| **State**   _optional_   _read-only_ | string |
| **Step**   _optional_ | string |
| **Token**   _optional_ | string |

### Failed

| Name | Schema |
| :--- | :--- |
| **Reason**   _optional_ | string |
| **State**   _optional_   _read-only_ | string |
| **Step**   _optional_ | string |

### FeeModel

| Name | Schema |
| :--- | :--- |
| **CommissionId**   _optional_ | string |
| **Id**   _optional_ | integer \(int32\) |
| **Leverage**   _optional_ | number \(double\) |
| **Seizure**   _optional_ | enum \(Placement, Execution, Fill, Proportional, Order\) |
| **Value**   _optional_ | number \(double\) |
| **ValueType**   _optional_ | enum \(Absolute, Coefficient\) |

### FeedbackModel

| Name | Schema |
| :--- | :--- |
| **BuildVersion**   _optional_ | string |
| **Comment**   _optional_ | string |
| **Contacts**   _optional_ | string |
| **Files**   _optional_ | &lt; [IAttachItem](definitions.md#iattachitem) &gt; array |
| **Id**   _optional_ | integer \(int32\) |
| **Login**   _optional_ | string |
| **Subject**   _optional_ | string |
| **SupportTicket**   _optional_ | string |
| **Timestamp**   _optional_ | integer \(int32\) |
| **UserAgent**   _optional_ | string |

### Formula

Formula model

| Name | Schema |
| :--- | :--- |
| **Expression**   _optional_ | string |
| **Id**   _optional_ | integer \(int32\) |
| **Name**   _optional_ | string |

### HistoricalTradeDataExportDataModel

| Name | Schema |
| :--- | :--- |
| **DefaultFileName**   _optional_ | string |
| **Indicators**   _optional_ | &lt; [HistoricalTradeDataExportIndicatorModel](definitions.md#historicaltradedataexportindicatormodel) &gt; array |
| **Securities**   _optional_ | &lt; integer \(int32\) &gt; array |
| **TimeFrame**   _optional_ | [TimeFrameModel](definitions.md#timeframemodel) |

### HistoricalTradeDataExportIndicatorModel

| Name | Schema |
| :--- | :--- |
| **Args**   _optional_ | &lt; object &gt; array |
| **Name**   _optional_ | string |
| **Text**   _optional_ | string |
| **Type**   _optional_ | string |

### HotkeyMapModel

| Name | Schema |
| :--- | :--- |
| **ActionId**   _optional_ | integer \(int32\) |
| **ActionName**   _optional_ | string |
| **ActionResource**   _optional_ | [WebActionMapModel](definitions.md#webactionmapmodel) |
| **Description**   _optional_ | string |
| **Id**   _optional_ | integer \(int32\) |
| **KeyboardShortcut**   _optional_ | string |
| **Parameters**   _optional_ | &lt; [HotkeyParameterMapModel](definitions.md#hotkeyparametermapmodel) &gt; array |

### HotkeyParameterMapModel

| Name | Schema |
| :--- | :--- |
| **HotkeyId**   _optional_ | integer \(int32\) |
| **Id**   _optional_ | integer \(int32\) |
| **ParameterId**   _optional_ | integer \(int32\) |
| **ParameterName**   _optional_ | string |
| **ParameterType**   _optional_ | integer \(int32\) |
| **Value**   _optional_ | string |

### IAttachItem

| Name | Schema |
| :--- | :--- |
| **FileName**   _optional_ | string |
| **IsImage**   _optional_ | boolean |
| **Type**   _optional_ | string |
| **Url**   _optional_ | string |

### IndicatorHistoryMapModel

| Name | Schema |
| :--- | :--- |
| **Date**   _optional_ | integer \(int32\) |
| **Values**   _optional_ | &lt; number \(double\) &gt; array |

### IndicatorHistoryRequestSettings

| Name | Schema |
| :--- | :--- |
| **CandlesCount**   _optional_ | integer \(int32\) |
| **EndDate**   _optional_ | integer \(int32\) |
| **IncludeNonMarketData**   _optional_ | boolean |
| **Interval**   _optional_ | integer \(int32\) |
| **Offset**   _optional_ | integer \(int32\) |
| **Period**   _optional_ | string |
| **Signature**   _optional_ | string |
| **StartDate**   _optional_ | integer \(int32\) |

### InternalPositionModel

| Name | Schema |
| :--- | :--- |
| **AccountId**   _optional_ | integer \(int32\) |
| **AverageClosePrice**   _optional_ | number \(double\) |
| **AverageOpenPrice**   _optional_ | number \(double\) |
| **CostBasis**   _optional_ | number \(double\) |
| **CreateDate**   _optional_ | string \(date-time\) |
| **DailyCloseProfitLoss**   _optional_ | number \(double\) |
| **DailyCostBasis**   _optional_ | number \(double\) |
| **DayQuantity**   _optional_ | number \(double\) |
| **ExcessChanges**   _optional_ | number \(double\) |
| **Id**   _optional_ | integer \(int32\) |
| **LastLot**   _optional_ | number \(double\) |
| **Locked**   _optional_ | boolean |
| **MarginType**   _optional_ | enum \(Empty, Cash, Margin, Short\) |
| **ModifyDate**   _optional_ | string \(date-time\) |
| **OpenQuantity**   _optional_ | number \(double\) |
| **Quantity**   _optional_ | number \(double\) |
| **RealizedProfitLoss**   _optional_ | number \(double\) |
| **SecurityId**   _optional_ | integer \(int32\) |
| **SpreadQuantity**   _optional_ | number \(double\) |
| **StopLossPrice**   _optional_ | number \(double\) |
| **TakeProfitPrice**   _optional_ | number \(double\) |
| **Unsettled**   _optional_ | number \(double\) |
| **UnsettledDate**   _optional_ | string \(date-time\) |

### InternalSecurityResource

| Name | Schema |
| :--- | :--- |
| **AddedDate**   _optional_ | string \(date-time\) |
| **AllowMargin**   _optional_ | boolean |
| **AllowShort**   _optional_ | boolean |
| **AllowTrade**   _optional_ | boolean |
| **BaseCurrency**   _optional_ | string |
| **ContractSize**   _optional_ | number \(double\) |
| **Currency**   _optional_ | string |
| **Cusip**   _optional_ | string |
| **Description**   _optional_ | string |
| **Enabled**   _optional_ | boolean |
| **Exchange**   _optional_ | string |
| **ExpirationDate**   _optional_ | string \(date-time\) |
| **ExpirationName**   _optional_ | string |
| **ExpirationType**   _optional_ | enum \(Regular, Quarterly, Weekly, Flex, Undefined, Mini, NonStandard\) |
| **Id**   _optional_ | integer \(int32\) |
| **Industry**   _optional_ | string |
| **Isin**   _optional_ | string |
| **Leverage**   _optional_ | number \(double\) |
| **MarginRate**   _optional_ | number \(double\) |
| **ModifyDate**   _optional_ | string \(date-time\) |
| **Name**   _optional_ | string |
| **OptionType**   _optional_ | enum \(Call, Put, Undefined\) |
| **ParentId**   _optional_ | integer \(int32\) |
| **Precision**   _optional_ | integer \(int32\) |
| **Price**   _optional_ | number \(double\) |
| **QuoteSubscriptionKey**   _optional_ | string |
| **Sector**   _optional_ | string |
| **Sedol**   _optional_ | string |
| **SeriesId**   _optional_ | integer \(int32\) |
| **Source**   _optional_ | integer \(int32\) |
| **SourceId**   _optional_ | string |
| **StrikePrice**   _optional_ | number \(double\) |
| **Suffix**   _optional_ | string |
| **Symbol**   _optional_ | string |
| **TickSize**   _optional_ | number \(double\) |
| **Type**   _optional_ | enum \(BankersAcceptance, CertificateOfDeposit, CollateralizeMortgageObligation, CorporateBond, CommercialPaper, CorporatePrivatePlacement, CommonStock, FederalHousingAuthority, FederalHomeLoan, FederalNationalMortgageAssociation, ForeignExchangeContract, Future, GovernmentNationalMortgageAssociation, TreasuriesPlusAgencyDebenture, MutualFund, MortgageInterestOnly, MortgagePrincipleOnly, MortgagePrivatePlacement, MiscellaneousPassThru, MunicipalBond, NoIsitcSecurityType, Option, PreferredStock, RepurchaseAgreement, ReverseRepurchaseAgreement, StudentLoanMarketingAssociation, TimeDeposit, UsTreasuryBill, Warrant, CatsTigersLions, WildcardEntry, ConvertibleBond, MortgageIoette, Index, FakeStockForNonStandartOption, Right, Cryptocurrency, ETF, DepositoryReceipt, CoveredWarrant, Unit\) |
| **UnderlyingSecuritySymbol**   _optional_ | string |
| **Unit**   _optional_ | string |
| **VolumePrecision**   _optional_ | integer \(int32\) |

### InternalUpdatePosition

| Name | Schema |
| :--- | :--- |
| **AccountId**   _optional_ | integer \(int32\) |
| **AverageClosePrice**   _optional_ | number \(double\) |
| **AverageOpenPrice**   _optional_ | number \(double\) |
| **CostBasis**   _optional_ | number \(double\) |
| **CreateDate**   _optional_ | string \(date-time\) |
| **DailyCloseProfitLoss**   _optional_ | number \(double\) |
| **DailyCostBasis**   _optional_ | number \(double\) |
| **DayQuantity**   _optional_ | number \(double\) |
| **ExcessChanges**   _optional_ | number \(double\) |
| **LastLot**   _optional_ | number \(double\) |
| **Locked**   _optional_ | boolean |
| **MarginType**   _optional_ | enum \(Empty, Cash, Margin, Short\) |
| **ModifyDate**   _optional_ | string \(date-time\) |
| **OpenQuantity**   _optional_ | number \(double\) |
| **Quantity**   _optional_ | number \(double\) |
| **RealizedProfitLoss**   _optional_ | number \(double\) |
| **SecurityId**   _optional_ | integer \(int32\) |
| **SpreadQuantity**   _optional_ | number \(double\) |
| **StopLossPrice**   _optional_ | number \(double\) |
| **TakeProfitPrice**   _optional_ | number \(double\) |
| **Unsettled**   _optional_ | number \(double\) |
| **UnsettledDate**   _optional_ | string \(date-time\) |

### LevelInfoMapModel

| Name | Schema |
| :--- | :--- |
| **BottomPrice**   _optional_ | number \(double\) |
| **GreenCandles**   _optional_ | &lt; integer \(int32\) &gt; array |
| **RedCandles**   _optional_ | &lt; integer \(int32\) &gt; array |
| **TopPrice**   _optional_ | number \(double\) |

### LocalizationResourceMapModel

| Name | Schema |
| :--- | :--- |
| **Culture**   _optional_ | string |
| **Key**   _optional_ | string |
| **Set**   _optional_ | string |
| **Value**   _optional_ | string |

### ModifyOrderResource

Modify order parameters

| Name | Description | Schema |
| :--- | :--- | :--- |
| **ClientId**   _optional_ | Client order id. | string |
| **ExecutionInstructions**   _optional_ | Algo order execution instructions. | &lt; string, string &gt; map |
| **ExpireDate**   _optional_ | Expire date. Assigned by client. | string \(date-time\) |
| **Id**   _required_ | Internal order id.   **Minimum value** : `1`   **Maximum value** : `2147483647` | integer \(int32\) |
| **Legs**   _optional_ | Order legs | &lt; [ModifyOrderResource](definitions.md#modifyorderresource) &gt; array |
| **Price**   _optional_ | Price \(not used for some order types\). | number \(double\) |
| **Quantity**   _optional_ | Quantity. Assigned by client.   **Minimum value** : `0` | number \(double\) |
| **StopPrice**   _optional_ | Stop price \(used for stop orders\). | number \(double\) |
| **TrailingLimitAmount**   _optional_ |  | number \(double\) |
| **TrailingLimitAmountType**   _optional_ |  | enum \(Absolute, Persentage\) |
| **TrailingStopAmount**   _optional_ |  | number \(double\) |
| **TrailingStopAmountType**   _optional_ |  | enum \(Absolute, Persentage\) |
| **ValidationsToBypass**   _optional_ | Flag property indicating validation rules to bypass | integer \(int32\) |

### ModifyUserModel

| Name | Schema |
| :--- | :--- |
| **EmailAddress**   _optional_ | string |
| **Enabled**   _optional_ | boolean |
| **EntitlementsPhoneNumber**   _optional_ | string |
| **ExpirationDate**   _optional_ | string \(date-time\) |
| **FirstName**   _optional_ | string |
| **LastName**   _optional_ | string |
| **Middle**   _optional_ | string |
| **PhoneNumber**   _optional_ | string |
| **Salutation**   _optional_ | enum \(NoSalutation, Mr, Mrs, Ms, Dr, Sir, Madam\) |
| **Suffix**   _optional_ | enum \(NoSuffix, Jr, Sr, Second, Third, Fourth\) |
| **TimeZoneInfoId**   _optional_ | string |

### MultilegAllocationRequest

| Name | Schema |
| :--- | :--- |
| **AccountType**   _optional_ | enum \(Cash, Margin\) |
| **Comment**   _optional_ | string |
| **Commission**   _optional_ | number \(double\) |
| **FromAccount**   _optional_ | string |
| **Instructions**   _optional_ | &lt; string, string &gt; map |
| **Legs**   _optional_ | &lt; [AllocationLegInfo](definitions.md#allocationleginfo) &gt; array |
| **ToAccount**   _optional_ | string |

### OptionExpirationResource

| Name | Schema |
| :--- | :--- |
| **ExpirationDate**   _optional_ | string \(date-time\) |
| **ExpirationType**   _optional_ | enum \(Regular, Quarterly, Weekly, Flex, Undefined, Mini, NonStandard\) |
| **SeriesId**   _optional_ | integer \(int32\) |
| **SeriesType**   _optional_ | enum \(Standard, NonStandard, Binary, Flex, Undefined\) |

### OptionResource

| Name | Schema |
| :--- | :--- |
| **AddedDate**   _optional_ | string \(date-time\) |
| **AllowMargin**   _optional_ | boolean |
| **AllowShort**   _optional_ | boolean |
| **AllowTrade**   _optional_ | boolean |
| **ContractSize**   _optional_ | number \(double\) |
| **Currency**   _optional_ | string |
| **Description**   _optional_ | string |
| **Enabled**   _optional_ | boolean |
| **Exchange**   _optional_ | string |
| **ExpirationDate**   _optional_ | string \(date-time\) |
| **ExpirationType**   _optional_ | enum \(Regular, Quarterly, Weekly, Flex, Undefined, Mini, NonStandard\) |
| **Id**   _optional_ | integer \(int32\) |
| **ModifyDate**   _optional_ | string \(date-time\) |
| **OptionType**   _optional_ | enum \(Call, Put, Undefined\) |
| **Precision**   _optional_ | integer \(int32\) |
| **SeriesId**   _optional_ | integer \(int32\) |
| **StrikePrice**   _optional_ | number \(double\) |
| **Symbol**   _optional_ | string |
| **TickSize**   _optional_ | number \(double\) |
| **Type**   _optional_ | enum \(BankersAcceptance, CertificateOfDeposit, CollateralizeMortgageObligation, CorporateBond, CommercialPaper, CorporatePrivatePlacement, CommonStock, FederalHousingAuthority, FederalHomeLoan, FederalNationalMortgageAssociation, ForeignExchangeContract, Future, GovernmentNationalMortgageAssociation, TreasuriesPlusAgencyDebenture, MutualFund, MortgageInterestOnly, MortgagePrincipleOnly, MortgagePrivatePlacement, MiscellaneousPassThru, MunicipalBond, NoIsitcSecurityType, Option, PreferredStock, RepurchaseAgreement, ReverseRepurchaseAgreement, StudentLoanMarketingAssociation, TimeDeposit, UsTreasuryBill, Warrant, CatsTigersLions, WildcardEntry, ConvertibleBond, MortgageIoette, Index, FakeStockForNonStandartOption, Right, Cryptocurrency, ETF, DepositoryReceipt, CoveredWarrant, Unit\) |
| **UnderlyingAssetSymbol**   _optional_ | string |
| **VolumePrecision**   _optional_ | integer \(int32\) |

### OrderResource

| Name | Description | Schema |
| :--- | :--- | :--- |
| **AccountId**   _optional_ | Account id. Assigned by OMS. | integer \(int32\) |
| **AveragePrice**   _optional_ | Average execution price. Assigned by executor. | number \(double\) |
| **ClientId**   _optional_ | Client order id \(ClOrdID\). Assigned by OMS. | string |
| **Comment**   _optional_ | Client side comments. Assigned by client. | string |
| **CounterPartyOrderId**   _optional_ | Executor order id. Assigned by executor. | string |
| **CreateDate**   _optional_ | Creation date. Assigned by OMS. | string \(date-time\) |
| **Date**   _optional_ | Last modification date. Assigned by OMS. | string \(date-time\) |
| **Description**   _optional_ | Used to indicate reject reason or broker comment. Assigned by executor. | string |
| **Exchange**   _optional_ | Desired exchange. Assigned by client. | string |
| **ExecBrocker**   _optional_ | Order route name. Assigned by executor. | string |
| **ExecId**   _optional_ | Execution id. | string |
| **ExecInst**   _optional_ | Execution instruction. Assigned by client. | enum \(DoNotIncrease, DoNotReduce, AllOrNone\) |
| **ExecutedQuantity**   _optional_ | Executed quantity. Assigned by executor. | number \(double\) |
| **ExecutionInstructions**   _optional_ | Algo order execution instructions. | &lt; string, string &gt; map |
| **ExecutionStatus**   _optional_ | Last modification status. Assigned by OMS or executor. | enum \(New, PartiallyFilled, Filled, DoneForDay, Canceled, Replaced, PendingCancel, Stopped, Rejected, Suspended, PendingNew, Calculated, Expired, AcceptedForBidding, PendingReplace, Error, Held\) |
| **ExecutionVenue**   _optional_ | Executor name, to which the order was routed. Assigned by OMS router. | string |
| **ExpireDate**   _optional_ | Expire date. Assigned by client. | string \(date-time\) |
| **ExtendedHours**   _optional_ | indicates the extended trading session for GTX order execution \(pre-market session, post-market session\) if empty - than there is no specific requirement for extended session | string |
| **Id**   _optional_ | Unique order id. Assigned by OMS. | integer \(int32\) |
| **InitialType**   _optional_ | Initial type. Assigned by OMS. | enum \(Market, Limit, Stop, StopLimit, Pegged, TrailingStop, TrailingStopLimit, OneCancelOther, OneTriggerOther, OneTriggerOneCancelOther, External\) |
| **IsExternal**   _optional_ | This property indicates that order was accepted from external system and fields like ClientOrderId should be persisted. It's a hack for orders from MessageAcceptor. Assigned be client. | boolean |
| **LastMarket**   _optional_ | Exchange where order was filled. Assigned by executor. | string |
| **LastPrice**   _optional_ | Last quote. Assigned by executor. | number \(double\) |
| **LastQuantity**   _optional_ | Last transaction executed quantity. Assigned by executor. | number \(double\) |
| **LeavesQuantity**   _optional_ | Unfilled quantity. Assigned by executor. | number \(double\) |
| **Legs**   _optional_ | Multileg order legs. Assigned by client. | &lt; [OrderResource](definitions.md#orderresource) &gt; array |
| **OrigClientId**   _optional_ | Client order id \(ClOrdID\). Assigned by OMS. | string |
| **ParentClientId**   _optional_ | Client order id \(ClOrdID\) of parent order in a case of mleg order. | string |
| **ParentId**   _optional_ | Parent order id. Assigned by OMS. | integer \(int32\) |
| **ParentRequestId**   _optional_ |  | integer \(int32\) |
| **Price**   _optional_ | Price \(not used for some order types\). Assigned by client. | number \(double\) |
| **Quantity**   _optional_ | Quantity. Assigned by client. | number \(double\) |
| **RequestId**   _optional_ | Request id. Assigned by OMS. | integer \(int32\) |
| **RequestStatus**   _optional_ | Indicate order processing status within OMS. Assigned by OMS. | enum \(RequireValidation, Validated, Rejected, Executing, Complete, Error\) |
| **SecurityId**   _optional_ | Security internal id; | integer \(int32\) |
| **SettDate**   _optional_ | date of settlement. Received from execution venue or calculated by OMS, assigned by OMS or executor. | string \(date-time\) |
| **SettlementDate**   _optional_ | Date of settlement deal | string \(date-time\) |
| **Side**   _optional_ | Side. Assigned by client. | enum \(Buy, Sell, SellShort, BuyToCover\) |
| **StateId**   _optional_ | State id. Assigned by OMS. | integer \(int32\) |
| **Status**   _optional_ | Current order status. Assigned by OMS or executor. | enum \(New, PartiallyFilled, Filled, DoneForDay, Canceled, Replaced, PendingCancel, Stopped, Rejected, Suspended, PendingNew, Calculated, Expired, AcceptedForBidding, PendingReplace, Error, Held\) |
| **StopPrice**   _optional_ | Stop price \(used for stop orders\). Assigned by client. | number \(double\) |
| **Symbol**   _optional_ |  | string |
| **Target**   _optional_ | Execution target. Assigned by OMS. | enum \(Ignore, New, Modify, Cancel, Execution, Status, CancelReject, Reject, Error, All\) |
| **TimeInForce**   _optional_ | Time in force. Assigned by client. | enum \(Day, GoodTillCancel, AtTheOpening, ImmediateOrCancel, FillOrKill, GoodTillCrossing, GoodTillDate, GoodTillTime\) |
| **Token**   _optional_ | Additional identity key \(usid in market scanner\). | string |
| **TrailingLimitAmount**   _optional_ | Assigned by client. | number \(double\) |
| **TrailingLimitAmountType**   _optional_ | Assigned by client. | enum \(Absolute, Persentage\) |
| **TrailingStopAmount**   _optional_ | Assigned by client. | number \(double\) |
| **TrailingStopAmountType**   _optional_ | Assigned by client. | enum \(Absolute, Persentage\) |
| **TransType**   _optional_ | Execution transaction type. | enum \(New, Cancel, Correct, Status\) |
| **TransactionDate**   _optional_ | Last transaction date. Assigned by OMS or executor. | string \(date-time\) |
| **Type**   _optional_ | Type. Assigned by client. | enum \(Market, Limit, Stop, StopLimit, Pegged, TrailingStop, TrailingStopLimit, OneCancelOther, OneTriggerOther, OneTriggerOneCancelOther, External\) |
| **UserId**   _optional_ | User id. Assigned by OMS. | integer \(int32\) |
| **ValidationsToBypass**   _optional_ | Flag property indicating validation rules to bypass | integer \(int32\) |

### PagingResult\[AccountModel\]

| Name | Description | Schema |
| :--- | :--- | :--- |
| **NextPageLink**   _optional_ | Next page | string |
| **PreviousPageLink**   _optional_ | Previous page | string |
| **Result**   _optional_ | Result collection | &lt; [AccountModel](definitions.md#accountmodel) &gt; array |
| **TotalCount**   _optional_ | Items total count | integer \(int32\) |

### PagingResult\[FeedbackModel\]

| Name | Description | Schema |
| :--- | :--- | :--- |
| **NextPageLink**   _optional_ | Next page | string |
| **PreviousPageLink**   _optional_ | Previous page | string |
| **Result**   _optional_ | Result collection | &lt; [FeedbackModel](definitions.md#feedbackmodel) &gt; array |
| **TotalCount**   _optional_ | Items total count | integer \(int32\) |

### PagingResult\[HotkeyMapModel\]

| Name | Description | Schema |
| :--- | :--- | :--- |
| **NextPageLink**   _optional_ | Next page | string |
| **PreviousPageLink**   _optional_ | Previous page | string |
| **Result**   _optional_ | Result collection | &lt; [HotkeyMapModel](definitions.md#hotkeymapmodel) &gt; array |
| **TotalCount**   _optional_ | Items total count | integer \(int32\) |

### PagingResult\[IList\[UserModel\]\]

| Name | Description | Schema |
| :--- | :--- | :--- |
| **NextPageLink**   _optional_ | Next page | string |
| **PreviousPageLink**   _optional_ | Previous page | string |
| **Result**   _optional_ | Result collection | &lt; &lt; [UserModel](definitions.md#usermodel) &gt; array &gt; array |
| **TotalCount**   _optional_ | Items total count | integer \(int32\) |

### PagingResult\[InternalSecurityResource\]

| Name | Description | Schema |
| :--- | :--- | :--- |
| **NextPageLink**   _optional_ | Next page | string |
| **PreviousPageLink**   _optional_ | Previous page | string |
| **Result**   _optional_ | Result collection | &lt; [InternalSecurityResource](definitions.md#internalsecurityresource) &gt; array |
| **TotalCount**   _optional_ | Items total count | integer \(int32\) |

### PagingResult\[LocalizationResourceMapModel\]

| Name | Description | Schema |
| :--- | :--- | :--- |
| **NextPageLink**   _optional_ | Next page | string |
| **PreviousPageLink**   _optional_ | Previous page | string |
| **Result**   _optional_ | Result collection | &lt; [LocalizationResourceMapModel](definitions.md#localizationresourcemapmodel) &gt; array |
| **TotalCount**   _optional_ | Items total count | integer \(int32\) |

### PagingResult\[PositionResource\]

| Name | Description | Schema |
| :--- | :--- | :--- |
| **NextPageLink**   _optional_ | Next page | string |
| **PreviousPageLink**   _optional_ | Previous page | string |
| **Result**   _optional_ | Result collection | &lt; [PositionResource](definitions.md#positionresource) &gt; array |
| **TotalCount**   _optional_ | Items total count | integer \(int32\) |

### PagingResult\[PriceAlertInfoModel\]

| Name | Description | Schema |
| :--- | :--- | :--- |
| **NextPageLink**   _optional_ | Next page | string |
| **PreviousPageLink**   _optional_ | Previous page | string |
| **Result**   _optional_ | Result collection | &lt; [PriceAlertInfoModel](definitions.md#pricealertinfomodel) &gt; array |
| **TotalCount**   _optional_ | Items total count | integer \(int32\) |

### PagingResult\[TransactionMapModel\]

| Name | Description | Schema |
| :--- | :--- | :--- |
| **NextPageLink**   _optional_ | Next page | string |
| **PreviousPageLink**   _optional_ | Previous page | string |
| **Result**   _optional_ | Result collection | &lt; [TransactionMapModel](definitions.md#transactionmapmodel) &gt; array |
| **TotalCount**   _optional_ | Items total count | integer \(int32\) |

### PagingResult\[WebActionMapModel\]

| Name | Description | Schema |
| :--- | :--- | :--- |
| **NextPageLink**   _optional_ | Next page | string |
| **PreviousPageLink**   _optional_ | Previous page | string |
| **Result**   _optional_ | Result collection | &lt; [WebActionMapModel](definitions.md#webactionmapmodel) &gt; array |
| **TotalCount**   _optional_ | Items total count | integer \(int32\) |

### PaymentInfoModel

| Name | Schema |
| :--- | :--- |
| **Amount**   _optional_ | number \(double\) |
| **CreateDate**   _optional_ | string \(date-time\) |
| **Description**   _optional_ | string |

### PhoneNumberModel

| Name | Schema |
| :--- | :--- |
| **PhoneNumber**   _optional_ | string |
| **PhoneNumberState**   _optional_ | enum \(NotLinked, Active, Suspended, NotVerified\) |

### PolicyEditableModel

Editable policy

| Name | Description | Schema |
| :--- | :--- | :--- |
| **Name**   _required_ | Name | string |

### PolicyInfoModel

| Name | Schema |
| :--- | :--- |
| **Date**   _optional_ | string \(date-time\) |
| **Id**   _optional_ | integer \(int32\) |
| **Name**   _optional_ | string |
| **Rules**   _optional_ | &lt; [PolicyRuleInfoModel](definitions.md#policyruleinfomodel) &gt; array |

### PolicyRuleEditableModel

Editable policy rule

| Name | Description | Schema |
| :--- | :--- | :--- |
| **Attributes**   _required_ | Rule attributes | &lt; string, string &gt; map |
| **Name**   _required_ | Rule name | string |

### PolicyRuleInfoModel

| Name | Schema |
| :--- | :--- |
| **Attributes**   _optional_ | &lt; string, string &gt; map |
| **Id**   _optional_ | integer \(int32\) |
| **Name**   _optional_ | string |

### PositionResource

| Name | Schema |
| :--- | :--- |
| **AccountId**   _optional_ | integer \(int32\) |
| **AverageClosePrice**   _optional_ | number \(double\) |
| **AverageOpenPrice**   _optional_ | number \(double\) |
| **CompanyName**   _optional_ | string |
| **ContractSize**   _optional_ | number \(double\) |
| **CostBasis**   _optional_ | number \(double\) |
| **CreateDate**   _optional_ | string \(date-time\) |
| **DailyCloseProfitLoss**   _optional_ | number \(double\) |
| **DailyCostBasis**   _optional_ | number \(double\) |
| **DayQuantity**   _optional_ | number \(double\) |
| **ExcessChanges**   _optional_ | number \(double\) |
| **Id**   _optional_ | integer \(int32\) |
| **ModifyDate**   _optional_ | string \(date-time\) |
| **Name**   _optional_ | string |
| **Quantity**   _optional_ | number \(double\) |
| **RealizedProfitLoss**   _optional_ | number \(double\) |
| **SecurityCurrency**   _optional_ | string |
| **SecurityId**   _optional_ | integer \(int32\) |
| **SecurityType**   _optional_ | string |
| **StopLossPrice**   _optional_ | number \(double\) |
| **Symbol**   _optional_ | string |
| **TakeProfitPrice**   _optional_ | number \(double\) |

### PriceAlertEditableModel

Editable price alert

| Name | Description | Schema |
| :--- | :--- | :--- |
| **Argument**   _optional_ | Trigger value   **Minimum value** : `0` | number \(double\) |
| **ExpirationDate**   _optional_ | Expiration date | integer \(int64\) |
| **Field**   _required_ | Alert type | string |
| **Operator**   _required_ | Alert trigger operator | string |
| **SecurityId**   _optional_ | Alert trigger security id   **Minimum value** : `0`   **Maximum value** : `2147483647` | integer \(int32\) |
| **State**   _optional_ | Target alert state | enum \(New, Expired, Completed, Stopped\) |

### PriceAlertInfoModel

Price alert info

| Name | Description | Schema |
| :--- | :--- | :--- |
| **Argument**   _optional_ | Trigger value | number \(double\) |
| **CreatedDate**   _optional_ | Created Date | integer \(int64\) |
| **ExpirationDate**   _optional_ | Expiration date | integer \(int64\) |
| **Field**   _optional_ | Alert type | string |
| **Id**   _optional_ | Internal price alert identifier | integer \(int32\) |
| **Operator**   _optional_ | Alert trigger operator | string |
| **SecurityId**   _optional_ | Alert trigger security id | integer \(int32\) |
| **State**   _optional_ | Target alert state | enum \(New, Expired, Completed, Stopped\) |

### QuoteModel

| Name | Schema |
| :--- | :--- |
| **Ask**   _optional_ | number \(double\) |
| **Bid**   _optional_ | number \(double\) |
| **Last**   _optional_ | number \(double\) |
| **OpenInterest**   _optional_ | number \(double\) |
| **Volume**   _optional_ | number \(double\) |

### ResendOrderReportRequest

| Name | Schema |
| :--- | :--- |
| **EndSequenceNumber**   _optional_ | integer \(int32\) |
| **ExecutionVenue**   _optional_ | string |
| **StartSequenceNumber**   _optional_ | integer \(int32\) |

### SecurityHistoryRequestSettings

| Name | Schema |
| :--- | :--- |
| **CandlesCount**   _optional_ | integer \(int32\) |
| **EndDate**   _optional_ | integer \(int32\) |
| **IncludeNonMarketData**   _optional_ | boolean |
| **Interval**   _optional_ | integer \(int32\) |
| **Period**   _optional_ | string |
| **StartDate**   _optional_ | integer \(int32\) |

### SecurityModel

| Name | Schema |
| :--- | :--- |
| **AddedDate**   _optional_ | string \(date-time\) |
| **BaseCurrency**   _optional_ | string |
| **ContractSize**   _optional_ | number \(double\) |
| **Currency**   _optional_ | string |
| **Cusip**   _optional_ | string |
| **Description**   _optional_ | string |
| **Exchange**   _optional_ | string |
| **ExpirationDate**   _optional_ | string \(date-time\) |
| **ExpirationType**   _optional_ | enum \(Regular, Quarterly, Weekly, Flex, Undefined, Mini, NonStandard\) |
| **Id**   _optional_ | integer \(int32\) |
| **Industry**   _optional_ | string |
| **Isin**   _optional_ | string |
| **MarginRate**   _optional_ | number \(double\) |
| **ModifyDate**   _optional_ | string \(date-time\) |
| **OptionType**   _optional_ | enum \(Call, Put, Undefined\) |
| **ParentId**   _optional_ | integer \(int32\) |
| **Precision**   _optional_ | integer \(int32\) |
| **Sector**   _optional_ | string |
| **Sedol**   _optional_ | string |
| **SeriesId**   _optional_ | integer \(int32\) |
| **Source**   _optional_ | integer \(int32\) |
| **StrikePrice**   _optional_ | number \(double\) |
| **Suffix**   _optional_ | string |
| **Symbol**   _optional_ | string |
| **TickSize**   _optional_ | number \(double\) |
| **Type**   _optional_ | enum \(BankersAcceptance, CertificateOfDeposit, CollateralizeMortgageObligation, CorporateBond, CommercialPaper, CorporatePrivatePlacement, CommonStock, FederalHousingAuthority, FederalHomeLoan, FederalNationalMortgageAssociation, ForeignExchangeContract, Future, GovernmentNationalMortgageAssociation, TreasuriesPlusAgencyDebenture, MutualFund, MortgageInterestOnly, MortgagePrincipleOnly, MortgagePrivatePlacement, MiscellaneousPassThru, MunicipalBond, NoIsitcSecurityType, Option, PreferredStock, RepurchaseAgreement, ReverseRepurchaseAgreement, StudentLoanMarketingAssociation, TimeDeposit, UsTreasuryBill, Warrant, CatsTigersLions, WildcardEntry, ConvertibleBond, MortgageIoette, Index, FakeStockForNonStandartOption, Right, Cryptocurrency, ETF, DepositoryReceipt, CoveredWarrant, Unit\) |
| **UnderlyingSecuritySymbol**   _optional_ | string |
| **Unit**   _optional_ | string |
| **VolumePrecision**   _optional_ | integer \(int32\) |

### SecuritySignature

| Name | Schema |
| :--- | :--- |
| **Currency**   _optional_ | string |
| **Exchange**   _optional_ | string |
| **Symbol**   _optional_ | string |

### SimpleAllocationRequest

| Name | Schema |
| :--- | :--- |
| **AccountType**   _optional_ | enum \(Cash, Margin\) |
| **Action**   _optional_ | enum \(Buy, Sell, SellShort, BuyToCover, SellToClose, BuyToClose, SellToOpen, BuyToOpen\) |
| **Comment**   _optional_ | string |
| **Commission**   _optional_ | number \(double\) |
| **FromAccount**   _optional_ | string |
| **Instructions**   _optional_ | &lt; string, string &gt; map |
| **Price**   _optional_ | number \(double\) |
| **Quantity**   _optional_ | number \(double\) |
| **Symbol**   _optional_ | string |
| **ToAccount**   _optional_ | string |

### SubscriptionModel

Web API notification service subscription representation

| Name | Description | Schema |
| :--- | :--- | :--- |
| **Channel**   _optional_ | Channel for subscription messages delivery | enum \(Email, MobileText, MobilePush, WebPopupAlert, Disabled\) |
| **State**   _optional_ | Subscription state | enum \(NotLinked, Active, Suspended, NotVerified\) |
| **SubscriptionType**   _optional_ | Subscription notification type | enum \(OrderExecution, OrderForReview, OrderOnReview, OrderPlacement, OrderReplacement, PriceAlert\) |

### Succeed

| Name | Schema |
| :--- | :--- |
| **State**   _optional_   _read-only_ | string |
| **Token**   _optional_ | string |

### SupportResistanceMapModel

| Name | Schema |
| :--- | :--- |
| **Levels**   _optional_ | &lt; [LevelInfoMapModel](definitions.md#levelinfomapmodel) &gt; array |
| **ResistancePrice**   _optional_ | number \(double\) |
| **SupportPrice**   _optional_ | number \(double\) |

### TimeFrameModel

| Name | Schema |
| :--- | :--- |
| **CandlesCount**   _optional_ | integer \(int32\) |
| **EndDate**   _optional_ | integer \(int32\) |
| **IncludeNonMarketData**   _optional_ | boolean |
| **Period**   _optional_ | string |
| **StartDate**   _optional_ | integer \(int32\) |

### TimeSeriesValueCandleMapModel

| Name | Schema |
| :--- | :--- |
| **Close**   _optional_ | number \(double\) |
| **DateTime**   _optional_   _read-only_ | string \(date-time\) |
| **High**   _optional_ | number \(double\) |
| **IsMarket**   _optional_ | boolean |
| **Low**   _optional_ | number \(double\) |
| **Open**   _optional_ | number \(double\) |
| **OpenInterest**   _optional_ | integer \(int32\) |
| **Time**   _optional_ | integer \(int32\) |
| **ValuationLevels**   _optional_ | &lt; number \(double\) &gt; array |
| **Volume**   _optional_ | number \(double\) |

### TransactionMapModel

| Name | Schema |
| :--- | :--- |
| **AccountId**   _optional_ | integer \(int32\) |
| **Date**   _optional_ | string \(date-time\) |
| **Description**   _optional_ | string |
| **Fee**   _optional_ | [FeeModel](definitions.md#feemodel) |
| **Id**   _optional_ | integer \(int32\) |
| **IsDayTrade**   _optional_ | boolean |
| **LeavesQuantity**   _optional_ | number \(double\) |
| **OrderStateId**   _optional_ | integer \(int32\) |
| **Quantity**   _optional_ | number \(double\) |
| **SecurityId**   _optional_ | integer \(int32\) |
| **Type**   _optional_ | enum \(Undefined, Commission, OrderExecution, OptionExpiration, Payment, ManualManipulation, Clearing, Rpl\) |
| **Value**   _optional_ | number \(double\) |

### Tuple\[Int32,String\]

| Name | Schema |
| :--- | :--- |
| **m\_Item1**   _optional_ | integer \(int32\) |
| **m\_Item2**   _optional_ | string |

### Tuple\[PhoneNumberModel,Int32\]

| Name | Schema |
| :--- | :--- |
| **m\_Item1**   _optional_ | [PhoneNumberModel](definitions.md#phonenumbermodel) |
| **m\_Item2**   _optional_ | integer \(int32\) |

### UserAccountModel

| Name | Schema |
| :--- | :--- |
| **AccessType**   _optional_ | enum \(Full, ReadOnly, ClosePositionsOnly\) |
| **Alias**   _optional_ | string |
| **ClearingAccount**   _optional_ | string |
| **Enabled**   _optional_ | boolean |
| **Id**   _optional_ | integer \(int32\) |
| **MarginType**   _optional_ | enum \(Empty, Cash, Margin, DayTrader, MarginIra\) |

### UserAddress

| Name | Schema |
| :--- | :--- |
| **City**   _optional_ | string |
| **CountryId**   _optional_ | integer \(int32\) |
| **PostalCode**   _optional_ | string |
| **State**   _optional_ | integer \(int32\) |
| **StreetAddress1**   _optional_ | string |
| **StreetAddress2**   _optional_ | string |

### UserInfoModel

| Name | Schema |
| :--- | :--- |
| **AddedDate**   _optional_ | string \(date-time\) |
| **Email**   _optional_ | string |
| **FirstName**   _optional_ | string |
| **LastName**   _optional_ | string |
| **Login**   _optional_ | string |
| **MiddleName**   _optional_ | string |
| **Salutation**   _optional_ | enum \(NoSalutation, Mr, Mrs, Ms, Dr, Sir, Madam\) |
| **Suffix**   _optional_ | enum \(NoSuffix, Jr, Sr, Second, Third, Fourth\) |
| **UserId**   _optional_ | integer \(int32\) |

### UserModel

| Name | Schema |
| :--- | :--- |
| **AddedDate**   _optional_ | string \(date-time\) |
| **Deleted**   _optional_ | boolean |
| **EmailAddress**   _optional_ | string |
| **Enabled**   _optional_ | boolean |
| **EntitlementsPhoneNumber**   _optional_ | string |
| **ExpirationDate**   _optional_ | string \(date-time\) |
| **FirstName**   _optional_ | string |
| **Id**   _optional_ | integer \(int32\) |
| **LastName**   _optional_ | string |
| **Login**   _optional_ | string |
| **Middle**   _optional_ | string |
| **PhoneNumber**   _optional_ | string |
| **Salutation**   _optional_ | enum \(NoSalutation, Mr, Mrs, Ms, Dr, Sir, Madam\) |
| **Suffix**   _optional_ | enum \(NoSuffix, Jr, Sr, Second, Third, Fourth\) |
| **TimeZoneInfoId**   _optional_ | string |

### UserToAccountRelationModel

| Name | Schema |
| :--- | :--- |
| **AccountAccessType**   _optional_ | enum \(Full, ReadOnly, ClosePositionsOnly\) |
| **UserModel**   _optional_ | [UserInfoModel](definitions.md#userinfomodel) |

### VerifyOrderModel

| Name | Description | Schema |
| :--- | :--- | :--- |
| **Commission**   _optional_ | The commission of the order. | number \(double\) |
| **Commissions**   _optional_ | The commission of the order. | &lt; string, number \(double\) &gt; map |
| **Cost**   _optional_ | The cost of the order. | number \(double\) |
| **ErrorDescription**   _optional_ | Error description. | string |
| **ErrorDescriptionArgs**   _optional_ | Error description arguments. | &lt; string &gt; array |
| **IsSuccessful**   _optional_ | Result. | boolean |
| **MarginChange**   _optional_ | Expected margin value changed. | number \(double\) |
| **NetCost**   _optional_ | The net cost of the order. | number \(double\) |
| **Quotes**   _optional_ | Order validation quotes. | &lt; [QuoteModel](definitions.md#quotemodel) &gt; array |

### WatchlistModel

| Name | Schema |
| :--- | :--- |
| **CreateDate**   _optional_ | string \(date-time\) |
| **Description**   _optional_ | string |
| **Id**   _optional_ | integer \(int32\) |
| **ModifyDate**   _optional_ | string \(date-time\) |
| **Name**   _optional_ | string |
| **ReadOnly**   _optional_ | boolean |
| **SecurityList**   _optional_ | &lt; [SecurityModel](definitions.md#securitymodel) &gt; array |
| **Source**   _optional_ | string |
| **Type**   _optional_ | enum \(UserList, SystemList, Snapshot\) |

### WebActionMapModel

| Name | Schema |
| :--- | :--- |
| **Action**   _optional_ | string |
| **Description**   _optional_ | string |
| **Id**   _optional_ | integer \(int32\) |
| **Name**   _optional_ | string |
| **Parameters**   _optional_ | &lt; [WebActionParameterMapModel](definitions.md#webactionparametermapmodel) &gt; array |

### WebActionModifyModel

| Name | Schema |
| :--- | :--- |
| **Action**   _optional_ | string |
| **Description**   _optional_ | string |
| **Name**   _optional_ | string |

### WebActionParameterMapModel

| Name | Schema |
| :--- | :--- |
| **ActionId**   _optional_ | integer \(int32\) |
| **Id**   _optional_ | integer \(int32\) |
| **Name**   _optional_ | string |
| **Type**   _optional_ | integer \(int32\) |

