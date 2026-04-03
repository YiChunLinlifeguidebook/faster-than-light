Protocol Contracts

RawEvent

```ts
export type RawEvent = {
  source: string;
  entityId: string;
  timestamp: string;
  payload: Record<string, unknown>;
};
```

NormalizedMetric

```ts
export type NormalizedMetric = {
  entityId: string;
  metricName: string;
  value: number | string | boolean;
  unit?: string;
  timestamp: string;
  quality?: "good" | "warn" | "bad";
};
```

FeatureSet

```ts
export type FeatureSet = {
  entityId: string;
  timestamp: string;
  features: Record<string, number>;
};
```

IndicatorResult

```ts
export type IndicatorResult = {
  indicatorId: string;
  entityId: string;
  value: number;
  score?: number;
  state?: string;
  direction?: "up" | "down" | "flat";
  confidence?: number;
  severity?: "low" | "medium" | "high" | "critical";
  summary?: string;
  timestamp: string;
  version: string;
};
```
