# Particular searches

If we wish to select what is inside the curly braces only after disabled then:

```
<input type="text" name="address" id="address" className="mt-1 block w-full rounded-md px-3 py-1.5 text-gray-900 ring-1 ring-inset ring-gray-300placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm disabled:bg-gray-50 disabled:text-gray-500 disabled:ring-gray-200" value={address.address} disabled={true} />
```

then we use the \v magic method, following by lookahead (diabled\=\{)
\zs and \ze indicate the start and end of pattern to be selected/matched
followed by \} in the end

search pattern:
```
:s/\v(disabled\=\{)\zs(.*)\ze\}
```
