## API Report File for "@shopware-pwa/shopware-6-client"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { AxiosInstance } from 'axios';
import { Cart } from '@shopware-pwa/commons/interfaces/models/checkout/cart/Cart';
import { Category } from '@shopware-pwa/commons/interfaces/models/content/category/Category';
import { CmsPage } from '@shopware-pwa/commons/interfaces/models/content/cms/CmsPage';
import { ContextTokenResponse } from '@shopware-pwa/commons/interfaces/response/SessionContext';
import { Country } from '@shopware-pwa/commons/interfaces/models/system/country/Country';
import { Currency } from '@shopware-pwa/commons/interfaces/models/system/currency/Currency';
import { Customer } from '@shopware-pwa/commons/interfaces/models/checkout/customer/Customer';
import { CustomerAddress } from '@shopware-pwa/commons/interfaces/models/checkout/customer/CustomerAddress';
import { CustomerRegistrationParams } from '@shopware-pwa/commons/interfaces/request/CustomerRegistrationParams';
import { EqualsAnyFilter } from '@shopware-pwa/commons/interfaces/search/SearchFilter';
import { EqualsFilter } from '@shopware-pwa/commons/interfaces/search/SearchFilter';
import { Grouping } from '@shopware-pwa/commons/interfaces/search/Grouping';
import { GuestOrderParams } from '@shopware-pwa/commons/interfaces/request/GuestOrderParams';
import { Language } from '@shopware-pwa/commons/interfaces/models/framework/language/Language';
import { MultiFilter } from '@shopware-pwa/commons/interfaces/search/SearchFilter';
import { NavigationResponse } from '@shopware-pwa/commons/interfaces/models/content/navigation/Navigation';
import { NotFilter } from '@shopware-pwa/commons/interfaces/search/SearchFilter';
import { Order } from '@shopware-pwa/commons/interfaces/models/checkout/order/Order';
import { PaymentMethod } from '@shopware-pwa/commons/interfaces/models/checkout/payment/PaymentMethod';
import { Product } from '@shopware-pwa/commons/interfaces/models/content/product/Product';
import { ProductListingResult } from '@shopware-pwa/commons/interfaces/response/ProductListingResult';
import { RangeFilter } from '@shopware-pwa/commons/interfaces/search/SearchFilter';
import { Salutation } from '@shopware-pwa/commons/interfaces/models/system/salutation/Salutation';
import { SearchCriteria } from '@shopware-pwa/commons/interfaces/search/SearchCriteria';
import { SearchResult } from '@shopware-pwa/commons/interfaces/response/SearchResult';
import { SessionContext } from '@shopware-pwa/commons/interfaces/response/SessionContext';
import { ShippingMethod } from '@shopware-pwa/commons/interfaces/models/checkout/shipping/ShippingMethod';
import { ShopwareAssociation } from '@shopware-pwa/commons/interfaces/search/Association';

// @alpha
export function addCartItemQuantity(itemId: string, quantity: number, contextInstance?: ShopwareApiInstance): Promise<Cart>;

// @alpha
export function addProductToCart(productId: string, quantity?: number, contextInstance?: ShopwareApiInstance): Promise<Cart>;

// @alpha
export function addPromotionCode(promotionCode: string, contextInstance?: ShopwareApiInstance): Promise<Cart>;

// @alpha
export function changeCartItemQuantity(itemId: string, newQuantity?: number, contextInstance?: ShopwareApiInstance): Promise<Cart>;

// @alpha
export function clearCart(contextInstance?: ShopwareApiInstance): Promise<ContextTokenResponse>;

// @beta (undocumented)
export interface ClientSettings {
    // (undocumented)
    accessToken?: string;
    // (undocumented)
    contextToken?: string;
    // (undocumented)
    defaultPaginationLimit?: number;
    // (undocumented)
    endpoint?: string;
    // (undocumented)
    languageId?: string;
    // (undocumented)
    timeout?: number;
}

// @beta (undocumented)
export const config: ClientSettings;

// @beta (undocumented)
export interface ConfigChangedArgs {
    // (undocumented)
    config: ClientSettings;
}

// @alpha
export function createCustomerAddress(params: Partial<CustomerAddress>, contextInstance?: ShopwareApiInstance): Promise<string>;

// @alpha
export function createGuestOrder(params: GuestOrderParams, contextInstance?: ShopwareApiInstance): Promise<Order>;

// @beta (undocumented)
export function createInstance(initialConfig?: ClientSettings): ShopwareApiInstance;

// @alpha
export function createOrder(contextInstance?: ShopwareApiInstance): Promise<Order>;

// @alpha (undocumented)
export interface CustomerRegisterResponse {
    // (undocumented)
    data: string;
}

// @alpha (undocumented)
export interface CustomerResetPasswordParam {
    // (undocumented)
    email: string;
    // (undocumented)
    storefrontUrl?: string;
}

// @alpha (undocumented)
export interface CustomerUpdateEmailParam {
    // (undocumented)
    email: string;
    // (undocumented)
    emailConfirmation: string;
    // (undocumented)
    password: string;
}

// @alpha (undocumented)
export interface CustomerUpdatePasswordParam {
    // (undocumented)
    newPassword: string;
    // (undocumented)
    newPasswordConfirm: string;
    // (undocumented)
    password: string;
}

// @alpha (undocumented)
export interface CustomerUpdateProfileParam {
    // (undocumented)
    firstName: string;
    // (undocumented)
    lastName: string;
    // (undocumented)
    salutationId: string;
    // (undocumented)
    title: string | null;
}

// @alpha
export function deleteCustomerAddress(addressId: string, contextInstance?: ShopwareApiInstance): Promise<void>;

// @alpha
export function getAvailableCountries(contextInstance?: ShopwareApiInstance): Promise<SearchResult<Country[]>>;

// @alpha (undocumented)
export function getAvailableCurrencies(contextInstance?: ShopwareApiInstance): Promise<Currency[]>;

// @alpha (undocumented)
export function getAvailableLanguages(contextInstance?: ShopwareApiInstance): Promise<Language[]>;

// @alpha (undocumented)
export function getAvailablePaymentMethods(contextInstance?: ShopwareApiInstance): Promise<PaymentMethod[]>;

// @alpha
export function getAvailableSalutations(contextInstance?: ShopwareApiInstance): Promise<SearchResult<Salutation[]>>;

// @alpha (undocumented)
export function getAvailableShippingMethods(contextInstance?: ShopwareApiInstance): Promise<ShippingMethod[]>;

// @alpha
export function getCart(contextInstance?: ShopwareApiInstance): Promise<Cart>;

// @alpha (undocumented)
export function getCategories(searchCriteria?: SearchCriteria, contextInstance?: ShopwareApiInstance): Promise<SearchResult<Category[]>>;

// @alpha (undocumented)
export function getCategory(categoryId: string, contextInstance?: ShopwareApiInstance): Promise<Category>;

// @alpha
export const getCategoryProductsListing: (categoryId: string, searchCriteria?: SearchCriteria | undefined, contextInstance?: ShopwareApiInstance) => Promise<ProductListingResult>;

// @beta
export function getCustomer(contextInstance?: ShopwareApiInstance): Promise<Customer | null>;

// @alpha
export function getCustomerAddress(addressId: string, contextInstance?: ShopwareApiInstance): Promise<CustomerAddress>;

// @beta
export function getCustomerAddresses(contextInstance?: ShopwareApiInstance): Promise<CustomerAddress[]>;

// @alpha
export function getCustomerOrderDetails(orderId: string, contextInstance?: ShopwareApiInstance): Promise<Order | undefined>;

// @beta
export function getCustomerOrders(contextInstance?: ShopwareApiInstance): Promise<Order[]>;

// @alpha (undocumented)
export function getNavigation(params: GetNavigationParams, contextInstance?: ShopwareApiInstance): Promise<NavigationResponse>;

// @alpha (undocumented)
export interface GetNavigationParams {
    // (undocumented)
    depth: number;
    // (undocumented)
    rootNode?: string;
}

// @beta
export function getOrderPaymentUrl({ orderId, finishUrl, }: {
    orderId: string;
    finishUrl?: string;
}, contextInstance?: ShopwareApiInstance): Promise<{
    paymentUrl: string;
}>;

// @alpha (undocumented)
export function getPage(path: string, searchCriteria?: SearchCriteria, contextInstance?: ShopwareApiInstance): Promise<PageResolverResult<CmsPage>>;

// @alpha (undocumented)
export function getPaymentMethodDetails(paymentId: string, contextInstance?: ShopwareApiInstance): Promise<PaymentMethod>;

// @alpha
export function getProduct(productId: string, params?: any, contextInstance?: ShopwareApiInstance): Promise<Product>;

// @alpha
export const getProducts: (searchCriteria?: SearchCriteria | undefined, contextInstance?: ShopwareApiInstance) => Promise<SearchResult<Product[]>>;

// @alpha
export const getProductsIds: (options?: any, contextInstance?: ShopwareApiInstance) => Promise<SearchResult<string[]>>;

// @beta (undocumented)
export function getResults(term: string, searchCriteria?: SearchCriteria, contextInstance?: ShopwareApiInstance): Promise<ProductListingResult>;

// @alpha
export function getSessionContext(contextInstance?: ShopwareApiInstance): Promise<SessionContext>;

// @alpha (undocumented)
export function getShippingMethodDetails(shippingId: string, contextInstance?: ShopwareApiInstance): Promise<ShippingMethod>;

// @beta (undocumented)
export function getSuggestedResults(term: string, searchCriteria?: SearchCriteria, contextInstance?: ShopwareApiInstance): Promise<ProductListingResult>;

// @alpha (undocumented)
export function getUserCountry(countryId: string, contextInstance?: ShopwareApiInstance): Promise<Country>;

// @alpha (undocumented)
export function getUserSalutation(salutationId: string, contextInstance?: ShopwareApiInstance): Promise<Salutation>;

// @beta
export function invokeGet({ address }: {
    address: string;
}, contextInstance?: ShopwareApiInstance): Promise<any>;

// @beta
export function invokePost({ address, payload, }: {
    address: string;
    payload?: any;
}, contextInstance?: ShopwareApiInstance): Promise<any>;

// @beta
export function login({ username, password }?: {
    username?: string;
    password?: string;
}, contextInstance?: ShopwareApiInstance): Promise<ContextTokenResponse>;

// @beta
export function logout(contextInstance?: ShopwareApiInstance): Promise<void>;

// @beta (undocumented)
export const onConfigChange: (fn: (context: ConfigChangedArgs) => void) => void;

// @alpha (undocumented)
export interface PageResolverResult<T> {
    // (undocumented)
    breadcrumb: {
        [id: string]: {
            name: string;
            path: string;
        };
    };
    // (undocumented)
    cmsPage: T;
    // (undocumented)
    resourceIdentifier: string;
    // (undocumented)
    resourceType: string;
}

// @alpha
export function register(params: CustomerRegistrationParams, contextInstance?: ShopwareApiInstance): Promise<CustomerRegisterResponse>;

// @alpha
export function removeCartItem(itemId: string, contextInstance?: ShopwareApiInstance): Promise<Cart>;

// @alpha
export function resetPassword(params: CustomerResetPasswordParam, contextInstance?: ShopwareApiInstance): Promise<void>;

// @alpha
export function setCurrentBillingAddress(billingAddressId: string, contextInstance?: ShopwareApiInstance): Promise<ContextTokenResponse>;

// @alpha (undocumented)
export function setCurrentCurrency(newCurrencyID: string, contextInstance?: ShopwareApiInstance): Promise<ContextTokenResponse>;

// @alpha (undocumented)
export function setCurrentLanguage(newLanguageId: string, contextInstance?: ShopwareApiInstance): Promise<ContextTokenResponse>;

// @alpha (undocumented)
export function setCurrentPaymentMethod(newPaymentMethodId: string, contextInstance?: ShopwareApiInstance): Promise<ContextTokenResponse>;

// @alpha
export function setCurrentShippingAddress(shippingAddressId: string, contextInstance?: ShopwareApiInstance): Promise<ContextTokenResponse>;

// @alpha (undocumented)
export function setCurrentShippingMethod(newShippingMethodId: string, contextInstance?: ShopwareApiInstance): Promise<ContextTokenResponse>;

// @alpha
export function setDefaultCustomerBillingAddress(addressId: string, contextInstance?: ShopwareApiInstance): Promise<string>;

// @alpha
export function setDefaultCustomerShippingAddress(addressId: string, contextInstance?: ShopwareApiInstance): Promise<string>;

// @beta
export const setup: (config?: ClientSettings) => void;

// @beta (undocumented)
export interface ShopwareApiInstance {
    // (undocumented)
    config: ClientSettings;
    // (undocumented)
    defaults: AxiosInstance["defaults"];
    // (undocumented)
    invoke: {
        post: AxiosInstance["post"];
        get: AxiosInstance["get"];
        put: AxiosInstance["put"];
        patch: AxiosInstance["patch"];
        delete: AxiosInstance["delete"];
    };
    // (undocumented)
    onConfigChange: (fn: (context: ConfigChangedArgs) => void) => void;
    // (undocumented)
    setup: (config?: ClientSettings) => void;
    // (undocumented)
    update: (config?: ClientSettings) => void;
}

// @alpha (undocumented)
export interface ShopwareParams {
    // (undocumented)
    associations?: ShopwareAssociation;
    // (undocumented)
    filter?: (NotFilter | MultiFilter | EqualsFilter | EqualsAnyFilter | RangeFilter)[];
    // (undocumented)
    grouping?: Grouping;
    // (undocumented)
    limit?: number;
    // (undocumented)
    manufacturer?: string;
    // (undocumented)
    p?: number;
    // (undocumented)
    page?: number;
    // (undocumented)
    properties?: string;
    // (undocumented)
    sort?: string;
    // (undocumented)
    term?: string;
}

// @beta
export const update: (config?: ClientSettings) => void;

// @alpha
export function updateEmail(params: CustomerUpdateEmailParam, contextInstance?: ShopwareApiInstance): Promise<void>;

// @alpha
export function updatePassword(params: CustomerUpdatePasswordParam, contextInstance?: ShopwareApiInstance): Promise<void>;

// @alpha
export function updateProfile(params: CustomerUpdateProfileParam, contextInstance?: ShopwareApiInstance): Promise<void>;


// (No @packageDocumentation comment for this package)

```
