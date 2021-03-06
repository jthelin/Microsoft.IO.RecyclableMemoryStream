# RecyclableMemoryStream.CopyToAsync method

Asynchronously reads all the bytes from the current position in this stream and writes them to another stream.

```csharp
public override Task CopyToAsync(Stream destination, int bufferSize, 
    CancellationToken cancellationToken)
```

| parameter | description |
| --- | --- |
| destination | The stream to which the contents of the current stream will be copied. |
| bufferSize | This parameter is ignored. |
| cancellationToken | The token to monitor for cancellation requests. |

## Return Value

A task that represents the asynchronous copy operation.

## Exceptions

| exception | condition |
| --- | --- |
| ArgumentNullException | *destination* is `null`. |
| ObjectDisposedException | Either the current stream or the destination stream is disposed. |
| NotSupportedException | The current stream does not support reading, or the destination stream does not support writing. |

## Remarks

Similarly to `MemoryStream`'s behavior, `CopyToAsync` will adjust the source stream's position by the number of bytes written to the destination stream, as a Read would do.

## See Also

* class [RecyclableMemoryStream](../RecyclableMemoryStream.md)
* namespace [Microsoft.IO](../../Microsoft.IO.RecyclableMemoryStream.md)

<!-- DO NOT EDIT: generated by xmldocmd for Microsoft.IO.RecyclableMemoryStream.dll -->
