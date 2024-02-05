- Provide already cleaned data in nice exports
- Export to JSON or CSV
- Unoptimized version may be fine for sqlite; PostGres is more important
	- General sqlite solution: `node-sequelize-stream` (this is probably slow, but should at least not run out of memory?)

- Fixed Assumption: Responses do not update / change; there will only ever be extra responses

- Current target format: `response` CSV with first level of payload keys expanded

- Multiple Steps
	1. Get list of all keys in payload
		- Long Term: Store these somewhere to support incremental updates of the list
	2. Use list of keys to generate a complex query that will already take care of extracting values from JSON

Retrieve JSON keys in SQLITE
```sql
-- With counts
SELECT payload_json.key as key, count(payload_json.key) as n
  FROM wwl_responses, json_each(payload) payload_json
  GROUP BY payload_json.key;

-- just keys
SELECT DISTINCT payload_json.key as key
  FROM wwl_responses, json_each(payload) payload_json;

-- with join
SELECT DISTINCT payload_json.key as key
  FROM wwl_responses, json_each(payload) payload_json
  INNER JOIN wwl_runs ON wwl_runs.runId = wwl_responses.runId
  WHERE wwl_runs.studyId = "example";
```

TODO
Retrieve JSON keys in PostGres
```sql
```

High performance solution for PostGres to CSV: `pg-copy-streams`
Using \copy or COPY from PostGres to immediately write CSVs in the end.
https://www.npmjs.com/package/pg-copy-streams

