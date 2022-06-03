
Updating the data of a settings will trigger the reconciliation process with LSP. 
This is not done in a single ATOMIC unit and follows a two stage control flow. 
Changes made through the API will be persisted in the initial stage. Another threadwill be responsible for detecting changes and executing the reconciliation process. 
All reconciliation processes will be idempotent. Executing the same reconciliation step will always result in the same outcome.
