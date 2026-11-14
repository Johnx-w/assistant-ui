## aui-perf nightly record

_6 points · 2026-09-03T05:27:14.273Z to 2026-11-14T11:44:00.988Z · latest runner: Intel(R) Xeon(R) 6975P-C · Node v26.13.0_

| bench | latest | Δ7d | Δ30d | min | max | points |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 chunks from one source stream | 562.21µs |  |  | 476.48µs | 562.21µs | 2 |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 controller.enqueue calls | 817.69µs |  |  | 738.70µs | 817.69µs | 2 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 16 deltas × 250 chars | 35.77µs | +7.2% | +7.2% | 34.03µs | 35.77µs | 2 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 250 deltas × 16 chars | 379.72µs | -1.9% | -1.9% | 379.72µs | 381.75µs | 2 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 4000 deltas × 1 char (per-token) | 5.883ms | -3.3% | -3.3% | 5.883ms | 5.943ms | 2 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 100 deltas | 161.46µs | -1.4% | -1.4% | 158.96µs | 161.46µs | 2 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 1000 deltas | 1.444ms | -7.3% | -7.3% | 1.444ms | 1.470ms | 2 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 4000 deltas | 5.858ms | -4.0% | -4.0% | 5.858ms | 5.889ms | 2 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 100 deltas | 6.40µs | -1.2% | -1.2% | 5.69µs | 6.40µs | 2 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 1000 deltas | 54.72µs | +4.1% | +4.1% | 47.39µs | 54.72µs | 2 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 4000 deltas | 218.38µs | +4.2% | +4.2% | 185.79µs | 218.38µs | 2 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 128 parts, distinct providers (stress) | 55.60µs |  |  | 51.69µs | 55.60µs | 2 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 16 parts, one repeated provider | 30.90µs |  |  | 26.56µs | 30.90µs | 2 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 2 parts, one repeated provider | 31.70µs |  |  | 29.80µs | 31.70µs | 2 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 512 parts, distinct providers (stress) | 200.76µs |  |  | 173.51µs | 200.76µs | 2 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 10 static tools | 45.25µs |  |  | 42.17µs | 45.25µs | 2 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 100 static tools | 482.24µs |  |  | 443.80µs | 482.24µs | 2 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 10 static tools | 6.35µs |  |  | 5.61µs | 6.35µs | 2 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 100 static tools | 52.25µs |  |  | 48.78µs | 52.25µs | 2 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 100 deltas | 436.76µs | -23.2% | -23.2% ⚠︎ | 401.19µs | 436.76µs | 2 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 1000 deltas | 3.692ms | -28.8% | -28.8% ⚠︎ | 3.536ms | 3.692ms | 2 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 4000 deltas | 14.250ms | -30.6% | -30.6% ⚠︎ | 14.250ms | 14.337ms | 2 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 100 deltas | 206.33µs | -48.1% | -48.1% ⚠︎ | 203.90µs | 206.33µs | 2 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 1000 deltas | 2.026ms | -45.1% | -45.1% ⚠︎ | 2.016ms | 2.026ms | 2 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 4000 deltas | 8.123ms | -45.5% | -45.5% ⚠︎ | 8.083ms | 8.123ms | 2 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 1000 messages, 6-part replies | 213.59µs |  |  | 146.96µs | 213.59µs | 2 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 5000 messages, 20-part replies | 1.344ms |  |  | 901.12µs | 1.344ms | 2 |
| external-message-conversion › core: external message reasoning continuations › 100 matches | 42.99µs |  |  | 36.38µs | 42.99µs | 2 |
| external-message-conversion › core: external message reasoning continuations › 1000 matches | 424.77µs |  |  | 369.87µs | 424.77µs | 2 |
| external-message-conversion › core: external message reasoning continuations › 5000 matches | 2.332ms |  |  | 1.948ms | 2.332ms | 2 |
| external-message-conversion › core: external message tool results › 100 matches | 54.36µs |  |  | 41.24µs | 54.36µs | 2 |
| external-message-conversion › core: external message tool results › 1000 matches | 537.42µs |  |  | 412.26µs | 537.42µs | 2 |
| external-message-conversion › core: external message tool results › 5000 matches | 2.903ms |  |  | 2.154ms | 2.903ms | 2 |
| external-message-conversion › core: external message unique tool calls › 100 matches | 28.16µs |  |  | 22.21µs | 28.16µs | 2 |
| external-message-conversion › core: external message unique tool calls › 1000 matches | 268.32µs |  |  | 203.99µs | 268.32µs | 2 |
| external-message-conversion › core: external message unique tool calls › 5000 matches | 1.451ms |  |  | 1.104ms | 1.451ms | 2 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 1 text parts | 0.17µs | +68.7% | +68.7% ⚠︎ | 0.15µs | 0.17µs | 2 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 10 text parts | 0.31µs | +78.7% | +78.7% ⚠︎ | 0.27µs | 0.31µs | 2 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 100 text parts | 1.63µs | +55.5% | +55.5% ⚠︎ | 1.57µs | 1.63µs | 2 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 1 tool calls | 0.38µs | +17.7% | +17.7% ⚠︎ | 0.37µs | 0.38µs | 2 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 10 tool calls | 2.42µs | +45.0% | +45.0% ⚠︎ | 1.72µs | 2.42µs | 2 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 100 tool calls | 19.80µs | +26.5% | +26.5% ⚠︎ | 15.52µs | 19.80µs | 2 |
| interactable-array-patches › core: id-keyed interactable array patches › 1000 items and patches | 113.54µs |  |  | 94.45µs | 113.54µs | 2 |
| interactable-array-patches › core: id-keyed interactable array patches › 5000 items and patches | 655.41µs |  |  | 481.41µs | 655.41µs | 2 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tilde runs on one line | 1.956ms |  |  | 1.429ms | 1.956ms | 2 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tildes after prose | 118.69µs |  |  | 103.49µs | 118.69µs | 2 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 triple-backtick spans on one line | 2.542ms |  |  | 1.905ms | 2.542ms | 2 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 5,000 code spans in one paragraph | 345.64µs |  |  | 271.77µs | 345.64µs | 2 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, mixed message, 100 sections | 517.72µs |  |  | 393.09µs | 517.72µs | 2 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tilde runs on one line | 5.793ms |  |  | 4.008ms | 5.793ms | 2 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tildes after prose | 467.20µs |  |  | 467.20µs | 473.20µs | 2 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 triple-backtick spans on one line | 14.870ms |  |  | 11.077ms | 14.870ms | 2 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 5,000 code spans in one paragraph | 2.341ms |  |  | 1.849ms | 2.341ms | 2 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, mixed message, 100 sections | 1.779ms |  |  | 1.494ms | 1.779ms | 2 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown | 2.006ms |  |  | 1.666ms | 2.006ms | 2 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown deferred | 2.217ms |  |  | 1.727ms | 2.217ms | 2 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown | 13.587ms |  |  | 11.568ms | 13.587ms | 2 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown deferred | 14.802ms |  |  | 13.259ms | 14.802ms | 2 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 1 paragraphs | 1.135ms | +116.2% | +116.2% ⚠︎ | 823.48µs | 1.135ms | 2 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 10 paragraphs | 1.910ms | +84.5% | +84.5% ⚠︎ | 1.568ms | 1.910ms | 2 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 50 paragraphs | 6.622ms | +56.4% | +56.4% ⚠︎ | 6.011ms | 6.622ms | 2 |
| markdown-streaming › react-markdown: the same token with defer on › 1 paragraphs deferred | 1.382ms | +23.2% | +23.2% ⚠︎ | 1.200ms | 1.382ms | 2 |
| markdown-streaming › react-markdown: the same token with defer on › 10 paragraphs deferred | 1.447ms | +37.9% | +37.9% ⚠︎ | 1.352ms | 1.447ms | 2 |
| markdown-streaming › react-markdown: the same token with defer on › 50 paragraphs deferred | 3.971ms | +36.3% | +36.3% ⚠︎ | 2.917ms | 3.971ms | 2 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 1000 character argument in 16-character deltas | 204.84µs |  |  | 204.84µs | 205.02µs | 2 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 10000 character argument in 16-character deltas | 1.746ms |  |  | 1.722ms | 1.746ms | 2 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 500 short object entries in 16-character deltas | 183.853ms |  |  | 159.907ms | 183.853ms | 2 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 50000 character argument in 16-character deltas | 8.250ms |  |  | 8.250ms | 8.856ms | 2 |
| react-pi-message-projection › react-pi: streaming tail projection › 10 stable messages | 1.24µs |  |  | 1.24µs | 1.36µs | 2 |
| react-pi-message-projection › react-pi: streaming tail projection › 1000 stable messages | 5.48µs |  |  | 5.48µs | 6.54µs | 2 |
| react-pi-message-projection › react-pi: streaming tail projection › 5000 stable messages | 26.16µs |  |  | 20.30µs | 26.16µs | 2 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 1 chunks | 4.72µs |  |  | 4.47µs | 4.72µs | 2 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 101 chunks | 15.33µs |  |  | 14.31µs | 15.33µs | 2 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1 chunks | 45.85µs |  |  | 45.85µs | 46.76µs | 2 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1025 chunks | 194.20µs |  |  | 194.20µs | 212.06µs | 2 |
| thread-scaling › external-store thread: mount+unmount by message count › 10 messages | 4.457ms | +159.3% | +159.3% ⚠︎ | 4.079ms | 4.457ms | 2 |
| thread-scaling › external-store thread: mount+unmount by message count › 100 messages | 25.271ms | +128.5% | +128.5% ⚠︎ | 25.271ms | 28.252ms | 2 |
| thread-scaling › external-store thread: mount+unmount by message count › 1000 messages | 323.257ms | +96.3% | +96.3% ⚠︎ | 323.257ms | 374.547ms | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 10 messages | 363.03µs |  |  | 255.66µs | 363.03µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 100 messages | 619.36µs |  |  | 441.32µs | 619.36µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 1000 messages | 3.162ms |  |  | 2.432ms | 3.162ms | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 10 messages | 367.42µs |  |  | 277.82µs | 367.42µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 100 messages | 1.069ms |  |  | 757.09µs | 1.069ms | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 1000 messages | 8.826ms |  |  | 8.826ms | 12.737ms | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 10 messages | 339.30µs |  |  | 262.22µs | 339.30µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 100 messages | 909.11µs |  |  | 543.05µs | 909.11µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 1000 messages | 5.939ms |  |  | 5.784ms | 5.939ms | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 10 messages | 151.87µs |  |  | 125.13µs | 151.87µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 100 messages | 358.53µs |  |  | 252.74µs | 358.53µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 1000 messages | 2.760ms |  |  | 1.668ms | 2.760ms | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 10 messages | 10.92µs |  |  | 9.90µs | 10.92µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 100 messages | 22.35µs |  |  | 20.67µs | 22.35µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 1000 messages | 201.96µs |  |  | 143.53µs | 201.96µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 10 messages | 429.28µs | +61.6% | +61.6% ⚠︎ | 306.59µs | 429.28µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 100 messages | 879.87µs | -43.7% | -43.7% ⚠︎ | 520.07µs | 879.87µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 1000 messages | 5.509ms | -85.2% | -85.2% ⚠︎ | 5.509ms | 9.374ms | 2 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 1000 bytes | 160.30µs |  |  | 146.66µs | 160.30µs | 2 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 10000 bytes | 1.461ms |  |  | 1.366ms | 1.461ms | 2 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 5000 bytes | 751.76µs |  |  | 667.89µs | 751.76µs | 2 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 1000 bytes | 179.78µs |  |  | 179.78µs | 186.53µs | 2 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 10000 bytes | 1.563ms |  |  | 1.563ms | 1.643ms | 2 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 5000 bytes | 787.57µs |  |  | 787.57µs | 819.98µs | 2 |
| tool-args › assistant-stream: complete accumulated arguments (single delta) › 10,000 array elements | 244.05µs |  |  | 193.61µs | 244.05µs | 2 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 array entries | 17.056ms |  |  | 15.347ms | 17.056ms | 2 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 object entries | 661.633ms |  |  | 406.028ms | 661.633ms | 2 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 1000 bytes | 131.86µs |  |  | 131.86µs | 140.86µs | 2 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 10000 bytes | 1.095ms |  |  | 1.095ms | 1.152ms | 2 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 5000 bytes | 546.32µs |  |  | 546.32µs | 586.53µs | 2 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 10000 bytes | 155.93µs |  |  | 108.45µs | 155.93µs | 2 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 50000 bytes | 748.94µs |  |  | 492.66µs | 748.94µs | 2 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 10000 bytes | 163.43µs |  |  | 116.87µs | 163.43µs | 2 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 50000 bytes | 802.27µs |  |  | 513.58µs | 802.27µs | 2 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRoot | 2.292ms | +38.6% | +38.6% ⚠︎ | 2.128ms | 2.292ms | 2 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootDeps | 2.359ms | +45.5% | +45.5% ⚠︎ | 2.140ms | 2.359ms | 2 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootStable | 2.266ms | +40.7% | +40.7% ⚠︎ | 2.049ms | 2.266ms | 2 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › react | 2.205ms | +53.7% | +53.7% ⚠︎ | 2.055ms | 2.205ms | 2 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › tapRoot | 1.532ms | +70.4% | +70.4% ⚠︎ | 1.279ms | 1.532ms | 2 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRoot | 2.269ms | +57.0% | +57.0% ⚠︎ | 1.923ms | 2.269ms | 2 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootDeps | 2.279ms | +62.5% | +62.5% ⚠︎ | 1.853ms | 2.279ms | 2 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootStable | 220.62µs | +27.0% | +27.0% ⚠︎ | 163.47µs | 220.62µs | 2 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › react | 96.07µs | +56.2% | +56.2% ⚠︎ | 83.51µs | 96.07µs | 2 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › tapRoot | 1.169ms | +54.7% | +54.7% ⚠︎ | 977.24µs | 1.169ms | 2 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › deps | 1.242ms | +65.1% | +65.1% ⚠︎ | 1.016ms | 1.242ms | 2 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › no-deps | 1.320ms | +73.2% | +73.2% ⚠︎ | 1.080ms | 1.320ms | 2 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › deps | 30.97µs | -16.4% | -16.4% ⚠︎ | 29.27µs | 30.97µs | 2 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › no-deps | 33.25µs | -94.8% | -94.8% ⚠︎ | 30.72µs | 33.25µs | 2 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › deps | 50.15µs | +44.6% | +44.6% ⚠︎ | 42.36µs | 50.15µs | 2 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › no-deps | 979.46µs | +55.4% | +55.4% ⚠︎ | 796.05µs | 979.46µs | 2 |

informational; points come from different runners of the same class, so read trends, not single deltas.
