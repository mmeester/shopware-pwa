<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@shopware-pwa/shopware-6-client](./shopware-6-client.md) &gt; [ShopwareApiInstance](./shopware-6-client.shopwareapiinstance.md)

## ShopwareApiInstance interface

> This API is provided as a preview for developers and may change based on feedback that we receive. Do not use this API in a production environment.
> 


<b>Signature:</b>

```typescript
export interface ShopwareApiInstance 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [config](./shopware-6-client.shopwareapiinstance.config.md) | <code>ClientSettings</code> | <b><i>(BETA)</i></b> |
|  [defaults](./shopware-6-client.shopwareapiinstance.defaults.md) | <code>AxiosInstance[&quot;defaults&quot;]</code> | <b><i>(BETA)</i></b> |
|  [invoke](./shopware-6-client.shopwareapiinstance.invoke.md) | <code>{</code><br/><code>        post: AxiosInstance[&quot;post&quot;];</code><br/><code>        get: AxiosInstance[&quot;get&quot;];</code><br/><code>        put: AxiosInstance[&quot;put&quot;];</code><br/><code>        patch: AxiosInstance[&quot;patch&quot;];</code><br/><code>        delete: AxiosInstance[&quot;delete&quot;];</code><br/><code>    }</code> | <b><i>(BETA)</i></b> |
|  [onConfigChange](./shopware-6-client.shopwareapiinstance.onconfigchange.md) | <code>(fn: (context: ConfigChangedArgs) =&gt; void) =&gt; void</code> | <b><i>(BETA)</i></b> |
|  [setup](./shopware-6-client.shopwareapiinstance.setup.md) | <code>(config?: ClientSettings) =&gt; void</code> | <b><i>(BETA)</i></b> |
|  [update](./shopware-6-client.shopwareapiinstance.update.md) | <code>(config?: ClientSettings) =&gt; void</code> | <b><i>(BETA)</i></b> |

