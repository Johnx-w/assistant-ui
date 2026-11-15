## aui-perf nightly record

_7 points · 2026-09-03T05:27:14.273Z to 2026-11-15T12:09:28.286Z · latest runner: AMD EPYC 9V74 80-Core Processor · Node v26.13.0_

| bench | latest | Δ7d | Δ30d | min | max | points |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 chunks from one source stream | 690.25µs |  |  | 476.48µs | 690.25µs | 3 |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 controller.enqueue calls | 993.24µs |  |  | 738.70µs | 993.24µs | 3 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 16 deltas × 250 chars | 44.67µs | +33.8% | +33.8% ⚠︎ | 34.03µs | 44.67µs | 3 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 250 deltas × 16 chars | 515.31µs | +33.1% | +33.1% ⚠︎ | 379.72µs | 515.31µs | 3 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 4000 deltas × 1 char (per-token) | 7.955ms | +30.7% | +30.7% ⚠︎ | 5.883ms | 7.955ms | 3 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 100 deltas | 216.32µs | +32.2% | +32.2% ⚠︎ | 158.96µs | 216.32µs | 3 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 1000 deltas | 2.078ms | +33.4% | +33.4% ⚠︎ | 1.444ms | 2.078ms | 3 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 4000 deltas | 7.989ms | +30.9% | +30.9% ⚠︎ | 5.858ms | 7.989ms | 3 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 100 deltas | 8.19µs | +26.5% | +26.5% ⚠︎ | 5.69µs | 8.19µs | 3 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 1000 deltas | 69.42µs | +32.1% | +32.1% ⚠︎ | 47.39µs | 69.42µs | 3 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 4000 deltas | 268.97µs | +28.3% | +28.3% ⚠︎ | 185.79µs | 268.97µs | 3 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 128 parts, distinct providers (stress) | 78.22µs |  |  | 51.69µs | 78.22µs | 3 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 16 parts, one repeated provider | 42.61µs |  |  | 26.56µs | 42.61µs | 3 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 2 parts, one repeated provider | 41.70µs |  |  | 29.80µs | 41.70µs | 3 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 512 parts, distinct providers (stress) | 246.75µs |  |  | 173.51µs | 246.75µs | 3 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 10 static tools | 52.20µs |  |  | 42.17µs | 52.20µs | 3 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 100 static tools | 513.56µs |  |  | 443.80µs | 513.56µs | 3 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 10 static tools | 7.43µs |  |  | 5.61µs | 7.43µs | 3 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 100 static tools | 61.03µs |  |  | 48.78µs | 61.03µs | 3 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 100 deltas | 582.34µs | +2.4% | +2.4% | 401.19µs | 582.34µs | 3 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 1000 deltas | 4.985ms | -3.9% | -3.9% | 3.536ms | 4.985ms | 3 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 4000 deltas | 19.645ms | -4.4% | -4.4% | 14.250ms | 19.645ms | 3 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 100 deltas | 284.90µs | -28.3% | -28.3% ⚠︎ | 203.90µs | 284.90µs | 3 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 1000 deltas | 2.743ms | -25.6% | -25.6% ⚠︎ | 2.016ms | 2.743ms | 3 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 4000 deltas | 10.955ms | -26.5% | -26.5% ⚠︎ | 8.083ms | 10.955ms | 3 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 1000 messages, 6-part replies | 210.73µs |  |  | 146.96µs | 213.59µs | 3 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 5000 messages, 20-part replies | 1.400ms |  |  | 901.12µs | 1.400ms | 3 |
| external-message-conversion › core: external message reasoning continuations › 100 matches | 50.21µs |  |  | 36.38µs | 50.21µs | 3 |
| external-message-conversion › core: external message reasoning continuations › 1000 matches | 504.30µs |  |  | 369.87µs | 504.30µs | 3 |
| external-message-conversion › core: external message reasoning continuations › 5000 matches | 2.689ms |  |  | 1.948ms | 2.689ms | 3 |
| external-message-conversion › core: external message tool results › 100 matches | 59.63µs |  |  | 41.24µs | 59.63µs | 3 |
| external-message-conversion › core: external message tool results › 1000 matches | 600.72µs |  |  | 412.26µs | 600.72µs | 3 |
| external-message-conversion › core: external message tool results › 5000 matches | 3.157ms |  |  | 2.154ms | 3.157ms | 3 |
| external-message-conversion › core: external message unique tool calls › 100 matches | 31.37µs |  |  | 22.21µs | 31.37µs | 3 |
| external-message-conversion › core: external message unique tool calls › 1000 matches | 296.45µs |  |  | 203.99µs | 296.45µs | 3 |
| external-message-conversion › core: external message unique tool calls › 5000 matches | 1.597ms |  |  | 1.104ms | 1.597ms | 3 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 1 text parts | 0.21µs | +103.0% | +103.0% ⚠︎ | 0.15µs | 0.21µs | 3 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 10 text parts | 0.36µs | +106.7% | +106.7% ⚠︎ | 0.27µs | 0.36µs | 3 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 100 text parts | 2.09µs | +99.1% | +99.1% ⚠︎ | 1.57µs | 2.09µs | 3 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 1 tool calls | 0.48µs | +49.6% | +49.6% ⚠︎ | 0.37µs | 0.48µs | 3 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 10 tool calls | 2.46µs | +47.3% | +47.3% ⚠︎ | 1.72µs | 2.46µs | 3 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 100 tool calls | 22.76µs | +45.4% | +45.4% ⚠︎ | 15.52µs | 22.76µs | 3 |
| interactable-array-patches › core: id-keyed interactable array patches › 1000 items and patches | 113.51µs |  |  | 94.45µs | 113.54µs | 3 |
| interactable-array-patches › core: id-keyed interactable array patches › 5000 items and patches | 590.54µs |  |  | 481.41µs | 655.41µs | 3 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tilde runs on one line | 2.114ms |  |  | 1.429ms | 2.114ms | 3 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tildes after prose | 161.40µs |  |  | 103.49µs | 161.40µs | 3 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 triple-backtick spans on one line | 2.750ms |  |  | 1.905ms | 2.750ms | 3 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 5,000 code spans in one paragraph | 390.24µs |  |  | 271.77µs | 390.24µs | 3 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, mixed message, 100 sections | 498.30µs |  |  | 393.09µs | 517.72µs | 3 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tilde runs on one line | 5.772ms |  |  | 4.008ms | 5.793ms | 3 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tildes after prose | 765.22µs |  |  | 467.20µs | 765.22µs | 3 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 triple-backtick spans on one line | 16.301ms |  |  | 11.077ms | 16.301ms | 3 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 5,000 code spans in one paragraph | 2.734ms |  |  | 1.849ms | 2.734ms | 3 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, mixed message, 100 sections | 1.928ms |  |  | 1.494ms | 1.928ms | 3 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown | 2.317ms |  |  | 1.666ms | 2.317ms | 3 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown deferred | 2.490ms |  |  | 1.727ms | 2.490ms | 3 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown | 16.785ms |  |  | 11.568ms | 16.785ms | 3 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown deferred | 17.949ms |  |  | 13.259ms | 17.949ms | 3 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 1 paragraphs | 997.99µs | +90.1% | +90.1% ⚠︎ | 823.48µs | 1.135ms | 3 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 10 paragraphs | 2.094ms | +102.3% | +102.3% ⚠︎ | 1.568ms | 2.094ms | 3 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 50 paragraphs | 7.371ms | +74.0% | +74.0% ⚠︎ | 6.011ms | 7.371ms | 3 |
| markdown-streaming › react-markdown: the same token with defer on › 1 paragraphs deferred | 1.363ms | +21.6% | +21.6% ⚠︎ | 1.200ms | 1.382ms | 3 |
| markdown-streaming › react-markdown: the same token with defer on › 10 paragraphs deferred | 1.444ms | +37.7% | +37.7% ⚠︎ | 1.352ms | 1.447ms | 3 |
| markdown-streaming › react-markdown: the same token with defer on › 50 paragraphs deferred | 4.428ms | +52.0% | +52.0% ⚠︎ | 2.917ms | 4.428ms | 3 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 1000 character argument in 16-character deltas | 245.29µs |  |  | 204.84µs | 245.29µs | 3 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 10000 character argument in 16-character deltas | 2.083ms |  |  | 1.722ms | 2.083ms | 3 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 500 short object entries in 16-character deltas | 213.861ms |  |  | 159.907ms | 213.861ms | 3 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 50000 character argument in 16-character deltas | 10.196ms |  |  | 8.250ms | 10.196ms | 3 |
| react-pi-message-projection › react-pi: streaming tail projection › 10 stable messages | 1.79µs |  |  | 1.24µs | 1.79µs | 3 |
| react-pi-message-projection › react-pi: streaming tail projection › 1000 stable messages | 8.96µs |  |  | 5.48µs | 8.96µs | 3 |
| react-pi-message-projection › react-pi: streaming tail projection › 5000 stable messages | 34.48µs |  |  | 20.30µs | 34.48µs | 3 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 1 chunks | 7.32µs |  |  | 4.47µs | 7.32µs | 3 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 101 chunks | 19.34µs |  |  | 14.31µs | 19.34µs | 3 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1 chunks | 72.46µs |  |  | 45.85µs | 72.46µs | 3 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1025 chunks | 231.65µs |  |  | 194.20µs | 231.65µs | 3 |
| thread-scaling › external-store thread: mount+unmount by message count › 10 messages | 4.524ms | +163.2% | +163.2% ⚠︎ | 4.079ms | 4.524ms | 3 |
| thread-scaling › external-store thread: mount+unmount by message count › 100 messages | 29.490ms | +166.7% | +166.7% ⚠︎ | 25.271ms | 29.490ms | 3 |
| thread-scaling › external-store thread: mount+unmount by message count › 1000 messages | 378.751ms | +130.1% | +130.1% ⚠︎ | 323.257ms | 378.751ms | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 10 messages | 463.14µs |  |  | 255.66µs | 463.14µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 100 messages | 705.63µs |  |  | 441.32µs | 705.63µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 1000 messages | 3.051ms |  |  | 2.432ms | 3.162ms | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 10 messages | 530.04µs |  |  | 277.82µs | 530.04µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 100 messages | 1.064ms |  |  | 757.09µs | 1.069ms | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 1000 messages | 10.682ms |  |  | 8.826ms | 12.737ms | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 10 messages | 459.59µs |  |  | 262.22µs | 459.59µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 100 messages | 780.84µs |  |  | 543.05µs | 909.11µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 1000 messages | 5.928ms |  |  | 5.784ms | 5.939ms | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 10 messages | 248.96µs |  |  | 125.13µs | 248.96µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 100 messages | 396.21µs |  |  | 252.74µs | 396.21µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 1000 messages | 2.346ms |  |  | 1.668ms | 2.760ms | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 10 messages | 12.73µs |  |  | 9.90µs | 12.73µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 100 messages | 26.94µs |  |  | 20.67µs | 26.94µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 1000 messages | 208.48µs |  |  | 143.53µs | 208.48µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 10 messages | 437.23µs | +64.6% | +64.6% ⚠︎ | 306.59µs | 437.23µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 100 messages | 796.44µs | -49.0% | -49.0% ⚠︎ | 520.07µs | 879.87µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 1000 messages | 6.154ms | -83.5% | -83.5% ⚠︎ | 5.509ms | 9.374ms | 3 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 1000 bytes | 199.50µs |  |  | 146.66µs | 199.50µs | 3 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 10000 bytes | 1.775ms |  |  | 1.366ms | 1.775ms | 3 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 5000 bytes | 899.94µs |  |  | 667.89µs | 899.94µs | 3 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 1000 bytes | 239.21µs |  |  | 179.78µs | 239.21µs | 3 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 10000 bytes | 2.107ms |  |  | 1.563ms | 2.107ms | 3 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 5000 bytes | 1.066ms |  |  | 787.57µs | 1.066ms | 3 |
| tool-args › assistant-stream: complete accumulated arguments (single delta) › 10,000 array elements | 264.97µs |  |  | 193.61µs | 264.97µs | 3 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 array entries | 20.598ms |  |  | 15.347ms | 20.598ms | 3 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 object entries | 466.049ms |  |  | 406.028ms | 661.633ms | 3 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 1000 bytes | 185.85µs |  |  | 131.86µs | 185.85µs | 3 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 10000 bytes | 1.538ms |  |  | 1.095ms | 1.538ms | 3 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 5000 bytes | 786.70µs |  |  | 546.32µs | 786.70µs | 3 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 10000 bytes | 165.35µs |  |  | 108.45µs | 165.35µs | 3 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 50000 bytes | 760.35µs |  |  | 492.66µs | 760.35µs | 3 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 10000 bytes | 177.51µs |  |  | 116.87µs | 177.51µs | 3 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 50000 bytes | 788.68µs |  |  | 513.58µs | 802.27µs | 3 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRoot | 2.616ms | +58.2% | +58.2% ⚠︎ | 2.128ms | 2.616ms | 3 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootDeps | 2.639ms | +62.8% | +62.8% ⚠︎ | 2.140ms | 2.639ms | 3 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootStable | 2.585ms | +60.6% | +60.6% ⚠︎ | 2.049ms | 2.585ms | 3 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › react | 2.639ms | +83.9% | +83.9% ⚠︎ | 2.055ms | 2.639ms | 3 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › tapRoot | 1.684ms | +87.2% | +87.2% ⚠︎ | 1.279ms | 1.684ms | 3 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRoot | 2.480ms | +71.6% | +71.6% ⚠︎ | 1.923ms | 2.480ms | 3 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootDeps | 2.500ms | +78.3% | +78.3% ⚠︎ | 1.853ms | 2.500ms | 3 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootStable | 194.93µs | +12.2% | +12.2% ⚠︎ | 163.47µs | 220.62µs | 3 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › react | 108.10µs | +75.7% | +75.7% ⚠︎ | 83.51µs | 108.10µs | 3 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › tapRoot | 1.294ms | +71.3% | +71.3% ⚠︎ | 977.24µs | 1.294ms | 3 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › deps | 1.423ms | +89.2% | +89.2% ⚠︎ | 1.016ms | 1.423ms | 3 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › no-deps | 1.507ms | +97.8% | +97.8% ⚠︎ | 1.080ms | 1.507ms | 3 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › deps | 37.90µs | +2.4% | +2.4% | 29.27µs | 37.90µs | 3 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › no-deps | 39.72µs | -93.8% | -93.8% ⚠︎ | 30.72µs | 39.72µs | 3 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › deps | 52.84µs | +52.4% | +52.4% ⚠︎ | 42.36µs | 52.84µs | 3 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › no-deps | 1.116ms | +77.0% | +77.0% ⚠︎ | 796.05µs | 1.116ms | 3 |

informational; points come from different runners of the same class, so read trends, not single deltas.
