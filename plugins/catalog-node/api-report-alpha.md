## API Report File for "@backstage/plugin-catalog-node"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { CatalogApi } from '@backstage/catalog-client';
import { CatalogProcessor } from '@backstage/plugin-catalog-node';
import { Entity } from '@backstage/catalog-model';
import { EntityProvider } from '@backstage/plugin-catalog-node';
import { ExtensionPoint } from '@backstage/backend-plugin-api';
import { PermissionRule } from '@backstage/plugin-permission-node';
import { PermissionRuleParams } from '@backstage/plugin-permission-common';
import { PlaceholderResolver } from '@backstage/plugin-catalog-node';
import { ScmLocationAnalyzer } from '@backstage/plugin-catalog-node';
import { ServiceRef } from '@backstage/backend-plugin-api';

// @alpha (undocumented)
export interface CatalogAnalysisExtensionPoint {
  // (undocumented)
  addLocationAnalyzer(analyzer: ScmLocationAnalyzer): void;
}

// @alpha (undocumented)
export const catalogAnalysisExtensionPoint: ExtensionPoint<CatalogAnalysisExtensionPoint>;

// @alpha (undocumented)
export interface CatalogPermissionExtensionPoint {
  // (undocumented)
  addPermissionRules(
    ...rules: Array<
      CatalogPermissionRuleInput | Array<CatalogPermissionRuleInput>
    >
  ): void;
}

// @alpha (undocumented)
export const catalogPermissionExtensionPoint: ExtensionPoint<CatalogPermissionExtensionPoint>;

// @alpha (undocumented)
export type CatalogPermissionRuleInput<
  TParams extends PermissionRuleParams = PermissionRuleParams,
> = PermissionRule<Entity, EntitiesSearchFilter, 'catalog-entity', TParams>;

// @alpha (undocumented)
export interface CatalogProcessingExtensionPoint {
  // (undocumented)
  addEntityProvider(
    ...providers: Array<EntityProvider | Array<EntityProvider>>
  ): void;
  // (undocumented)
  addPlaceholderResolver(key: string, resolver: PlaceholderResolver): void;
  // (undocumented)
  addProcessor(
    ...processors: Array<CatalogProcessor | Array<CatalogProcessor>>
  ): void;
}

// @alpha (undocumented)
export const catalogProcessingExtensionPoint: ExtensionPoint<CatalogProcessingExtensionPoint>;

// @alpha
export const catalogServiceRef: ServiceRef<CatalogApi, 'plugin'>;

// @alpha (undocumented)
export type EntitiesSearchFilter = {
  key: string;
  values?: string[];
};

// (No @packageDocumentation comment for this package)
```
