# LocalStorage

You can back your stores with LocalStorage by including the `LocalStoragePlugin` plugin.

```TS
import { NgxsModule, LocalStoragePluginModule } from 'ngxs';

@NgModule({
  imports: [
    NgxsModule.forRoot([]),
    LocalStoragePluginModule.forRoot(
      // Default, you can pass single string or array of strings
      // that could be deeply nested too
      key: '@@STATE',
      // Custom serializer, defaults to JSON
      serialize: JSON.stringify,
      // Custom deserializer, defaults to JSON
      deserialize: JSON.parse
    )
  ]
})
export class MyModule {}
```