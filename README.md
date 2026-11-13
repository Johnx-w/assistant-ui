## aui-perf nightly record

_5 points · 2026-09-03T05:27:14.273Z to 2026-11-13T12:29:22.231Z · latest runner: AMD EPYC 9V45 96-Core Processor · Node v26.13.0_

| bench | latest | Δ7d | Δ30d | min | max | points |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 chunks from one source stream | 476.48µs |  |  | 476.48µs | 476.48µs | 1 |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 controller.enqueue calls | 738.70µs |  |  | 738.70µs | 738.70µs | 1 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 16 deltas × 250 chars | 34.03µs | +2.0% | +2.0% | 34.03µs | 34.03µs | 1 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 250 deltas × 16 chars | 381.75µs | -1.4% | -1.4% | 381.75µs | 381.75µs | 1 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 4000 deltas × 1 char (per-token) | 5.943ms | -2.3% | -2.3% | 5.943ms | 5.943ms | 1 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 100 deltas | 158.96µs | -2.9% | -2.9% | 158.96µs | 158.96µs | 1 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 1000 deltas | 1.470ms | -5.6% | -5.6% | 1.470ms | 1.470ms | 1 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 4000 deltas | 5.889ms | -3.5% | -3.5% | 5.889ms | 5.889ms | 1 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 100 deltas | 5.69µs | -12.1% | -12.1% ⚠︎ | 5.69µs | 5.69µs | 1 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 1000 deltas | 47.39µs | -9.8% | -9.8% | 47.39µs | 47.39µs | 1 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 4000 deltas | 185.79µs | -11.4% | -11.4% ⚠︎ | 185.79µs | 185.79µs | 1 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 128 parts, distinct providers (stress) | 51.69µs |  |  | 51.69µs | 51.69µs | 1 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 16 parts, one repeated provider | 26.56µs |  |  | 26.56µs | 26.56µs | 1 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 2 parts, one repeated provider | 29.80µs |  |  | 29.80µs | 29.80µs | 1 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 512 parts, distinct providers (stress) | 173.51µs |  |  | 173.51µs | 173.51µs | 1 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 10 static tools | 42.17µs |  |  | 42.17µs | 42.17µs | 1 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 100 static tools | 443.80µs |  |  | 443.80µs | 443.80µs | 1 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 10 static tools | 5.61µs |  |  | 5.61µs | 5.61µs | 1 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 100 static tools | 48.78µs |  |  | 48.78µs | 48.78µs | 1 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 100 deltas | 401.19µs | -29.5% | -29.5% ⚠︎ | 401.19µs | 401.19µs | 1 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 1000 deltas | 3.536ms | -31.8% | -31.8% ⚠︎ | 3.536ms | 3.536ms | 1 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 4000 deltas | 14.337ms | -30.2% | -30.2% ⚠︎ | 14.337ms | 14.337ms | 1 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 100 deltas | 203.90µs | -48.7% | -48.7% ⚠︎ | 203.90µs | 203.90µs | 1 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 1000 deltas | 2.016ms | -45.3% | -45.3% ⚠︎ | 2.016ms | 2.016ms | 1 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 4000 deltas | 8.083ms | -45.8% | -45.8% ⚠︎ | 8.083ms | 8.083ms | 1 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 1000 messages, 6-part replies | 146.96µs |  |  | 146.96µs | 146.96µs | 1 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 5000 messages, 20-part replies | 901.12µs |  |  | 901.12µs | 901.12µs | 1 |
| external-message-conversion › core: external message reasoning continuations › 100 matches | 36.38µs |  |  | 36.38µs | 36.38µs | 1 |
| external-message-conversion › core: external message reasoning continuations › 1000 matches | 369.87µs |  |  | 369.87µs | 369.87µs | 1 |
| external-message-conversion › core: external message reasoning continuations › 5000 matches | 1.948ms |  |  | 1.948ms | 1.948ms | 1 |
| external-message-conversion › core: external message tool results › 100 matches | 41.24µs |  |  | 41.24µs | 41.24µs | 1 |
| external-message-conversion › core: external message tool results › 1000 matches | 412.26µs |  |  | 412.26µs | 412.26µs | 1 |
| external-message-conversion › core: external message tool results › 5000 matches | 2.154ms |  |  | 2.154ms | 2.154ms | 1 |
| external-message-conversion › core: external message unique tool calls › 100 matches | 22.21µs |  |  | 22.21µs | 22.21µs | 1 |
| external-message-conversion › core: external message unique tool calls › 1000 matches | 203.99µs |  |  | 203.99µs | 203.99µs | 1 |
| external-message-conversion › core: external message unique tool calls › 5000 matches | 1.104ms |  |  | 1.104ms | 1.104ms | 1 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 1 text parts | 0.15µs | +46.7% | +46.7% ⚠︎ | 0.15µs | 0.15µs | 1 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 10 text parts | 0.27µs | +54.2% | +54.2% ⚠︎ | 0.27µs | 0.27µs | 1 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 100 text parts | 1.57µs | +49.0% | +49.0% ⚠︎ | 1.57µs | 1.57µs | 1 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 1 tool calls | 0.37µs | +16.0% | +16.0% ⚠︎ | 0.37µs | 0.37µs | 1 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 10 tool calls | 1.72µs | +2.9% | +2.9% | 1.72µs | 1.72µs | 1 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 100 tool calls | 15.52µs | -0.9% | -0.9% | 15.52µs | 15.52µs | 1 |
| interactable-array-patches › core: id-keyed interactable array patches › 1000 items and patches | 94.45µs |  |  | 94.45µs | 94.45µs | 1 |
| interactable-array-patches › core: id-keyed interactable array patches › 5000 items and patches | 481.41µs |  |  | 481.41µs | 481.41µs | 1 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tilde runs on one line | 1.429ms |  |  | 1.429ms | 1.429ms | 1 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tildes after prose | 103.49µs |  |  | 103.49µs | 103.49µs | 1 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 triple-backtick spans on one line | 1.905ms |  |  | 1.905ms | 1.905ms | 1 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 5,000 code spans in one paragraph | 271.77µs |  |  | 271.77µs | 271.77µs | 1 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, mixed message, 100 sections | 393.09µs |  |  | 393.09µs | 393.09µs | 1 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tilde runs on one line | 4.008ms |  |  | 4.008ms | 4.008ms | 1 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tildes after prose | 473.20µs |  |  | 473.20µs | 473.20µs | 1 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 triple-backtick spans on one line | 11.077ms |  |  | 11.077ms | 11.077ms | 1 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 5,000 code spans in one paragraph | 1.849ms |  |  | 1.849ms | 1.849ms | 1 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, mixed message, 100 sections | 1.494ms |  |  | 1.494ms | 1.494ms | 1 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown | 1.666ms |  |  | 1.666ms | 1.666ms | 1 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown deferred | 1.727ms |  |  | 1.727ms | 1.727ms | 1 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown | 11.568ms |  |  | 11.568ms | 11.568ms | 1 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown deferred | 13.259ms |  |  | 13.259ms | 13.259ms | 1 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 1 paragraphs | 823.48µs | +56.9% | +56.9% ⚠︎ | 823.48µs | 823.48µs | 1 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 10 paragraphs | 1.568ms | +51.4% | +51.4% ⚠︎ | 1.568ms | 1.568ms | 1 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 50 paragraphs | 6.011ms | +41.9% | +41.9% ⚠︎ | 6.011ms | 6.011ms | 1 |
| markdown-streaming › react-markdown: the same token with defer on › 1 paragraphs deferred | 1.200ms | +7.0% | +7.0% | 1.200ms | 1.200ms | 1 |
| markdown-streaming › react-markdown: the same token with defer on › 10 paragraphs deferred | 1.352ms | +28.9% | +28.9% ⚠︎ | 1.352ms | 1.352ms | 1 |
| markdown-streaming › react-markdown: the same token with defer on › 50 paragraphs deferred | 2.917ms | +0.1% | +0.1% | 2.917ms | 2.917ms | 1 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 1000 character argument in 16-character deltas | 205.02µs |  |  | 205.02µs | 205.02µs | 1 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 10000 character argument in 16-character deltas | 1.722ms |  |  | 1.722ms | 1.722ms | 1 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 500 short object entries in 16-character deltas | 159.907ms |  |  | 159.907ms | 159.907ms | 1 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 50000 character argument in 16-character deltas | 8.856ms |  |  | 8.856ms | 8.856ms | 1 |
| react-pi-message-projection › react-pi: streaming tail projection › 10 stable messages | 1.36µs |  |  | 1.36µs | 1.36µs | 1 |
| react-pi-message-projection › react-pi: streaming tail projection › 1000 stable messages | 6.54µs |  |  | 6.54µs | 6.54µs | 1 |
| react-pi-message-projection › react-pi: streaming tail projection › 5000 stable messages | 20.30µs |  |  | 20.30µs | 20.30µs | 1 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 1 chunks | 4.47µs |  |  | 4.47µs | 4.47µs | 1 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 101 chunks | 14.31µs |  |  | 14.31µs | 14.31µs | 1 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1 chunks | 46.76µs |  |  | 46.76µs | 46.76µs | 1 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1025 chunks | 212.06µs |  |  | 212.06µs | 212.06µs | 1 |
| thread-scaling › external-store thread: mount+unmount by message count › 10 messages | 4.079ms | +137.3% | +137.3% ⚠︎ | 4.079ms | 4.079ms | 1 |
| thread-scaling › external-store thread: mount+unmount by message count › 100 messages | 28.252ms | +155.5% | +155.5% ⚠︎ | 28.252ms | 28.252ms | 1 |
| thread-scaling › external-store thread: mount+unmount by message count › 1000 messages | 374.547ms | +127.5% | +127.5% ⚠︎ | 374.547ms | 374.547ms | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 10 messages | 255.66µs |  |  | 255.66µs | 255.66µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 100 messages | 441.32µs |  |  | 441.32µs | 441.32µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 1000 messages | 2.432ms |  |  | 2.432ms | 2.432ms | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 10 messages | 277.82µs |  |  | 277.82µs | 277.82µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 100 messages | 757.09µs |  |  | 757.09µs | 757.09µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 1000 messages | 12.737ms |  |  | 12.737ms | 12.737ms | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 10 messages | 262.22µs |  |  | 262.22µs | 262.22µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 100 messages | 543.05µs |  |  | 543.05µs | 543.05µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 1000 messages | 5.784ms |  |  | 5.784ms | 5.784ms | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 10 messages | 125.13µs |  |  | 125.13µs | 125.13µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 100 messages | 252.74µs |  |  | 252.74µs | 252.74µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 1000 messages | 1.668ms |  |  | 1.668ms | 1.668ms | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 10 messages | 9.90µs |  |  | 9.90µs | 9.90µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 100 messages | 20.67µs |  |  | 20.67µs | 20.67µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 1000 messages | 143.53µs |  |  | 143.53µs | 143.53µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 10 messages | 306.59µs | +15.4% | +15.4% ⚠︎ | 306.59µs | 306.59µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 100 messages | 520.07µs | -66.7% | -66.7% ⚠︎ | 520.07µs | 520.07µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 1000 messages | 9.374ms | -74.9% | -74.9% ⚠︎ | 9.374ms | 9.374ms | 1 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 1000 bytes | 146.66µs |  |  | 146.66µs | 146.66µs | 1 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 10000 bytes | 1.366ms |  |  | 1.366ms | 1.366ms | 1 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 5000 bytes | 667.89µs |  |  | 667.89µs | 667.89µs | 1 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 1000 bytes | 186.53µs |  |  | 186.53µs | 186.53µs | 1 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 10000 bytes | 1.643ms |  |  | 1.643ms | 1.643ms | 1 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 5000 bytes | 819.98µs |  |  | 819.98µs | 819.98µs | 1 |
| tool-args › assistant-stream: complete accumulated arguments (single delta) › 10,000 array elements | 193.61µs |  |  | 193.61µs | 193.61µs | 1 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 array entries | 15.347ms |  |  | 15.347ms | 15.347ms | 1 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 object entries | 406.028ms |  |  | 406.028ms | 406.028ms | 1 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 1000 bytes | 140.86µs |  |  | 140.86µs | 140.86µs | 1 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 10000 bytes | 1.152ms |  |  | 1.152ms | 1.152ms | 1 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 5000 bytes | 586.53µs |  |  | 586.53µs | 586.53µs | 1 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 10000 bytes | 108.45µs |  |  | 108.45µs | 108.45µs | 1 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 50000 bytes | 492.66µs |  |  | 492.66µs | 492.66µs | 1 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 10000 bytes | 116.87µs |  |  | 116.87µs | 116.87µs | 1 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 50000 bytes | 513.58µs |  |  | 513.58µs | 513.58µs | 1 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRoot | 2.128ms | +28.7% | +28.7% ⚠︎ | 2.128ms | 2.128ms | 1 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootDeps | 2.140ms | +32.1% | +32.1% ⚠︎ | 2.140ms | 2.140ms | 1 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootStable | 2.049ms | +27.3% | +27.3% ⚠︎ | 2.049ms | 2.049ms | 1 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › react | 2.055ms | +43.2% | +43.2% ⚠︎ | 2.055ms | 2.055ms | 1 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › tapRoot | 1.279ms | +42.3% | +42.3% ⚠︎ | 1.279ms | 1.279ms | 1 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRoot | 1.923ms | +33.1% | +33.1% ⚠︎ | 1.923ms | 1.923ms | 1 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootDeps | 1.853ms | +32.1% | +32.1% ⚠︎ | 1.853ms | 1.853ms | 1 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootStable | 163.47µs | -5.9% | -5.9% | 163.47µs | 163.47µs | 1 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › react | 83.51µs | +35.7% | +35.7% ⚠︎ | 83.51µs | 83.51µs | 1 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › tapRoot | 977.24µs | +29.3% | +29.3% ⚠︎ | 977.24µs | 977.24µs | 1 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › deps | 1.016ms | +35.0% | +35.0% ⚠︎ | 1.016ms | 1.016ms | 1 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › no-deps | 1.080ms | +41.8% | +41.8% ⚠︎ | 1.080ms | 1.080ms | 1 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › deps | 29.27µs | -20.9% | -20.9% ⚠︎ | 29.27µs | 29.27µs | 1 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › no-deps | 30.72µs | -95.2% | -95.2% ⚠︎ | 30.72µs | 30.72µs | 1 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › deps | 42.36µs | +22.2% | +22.2% ⚠︎ | 42.36µs | 42.36µs | 1 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › no-deps | 796.05µs | +26.3% | +26.3% ⚠︎ | 796.05µs | 796.05µs | 1 |

informational; points come from different runners of the same class, so read trends, not single deltas.
