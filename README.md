## aui-perf nightly record

_8 points · 2026-09-03T05:27:14.273Z to 2026-11-16T13:03:04.689Z · latest runner: AMD EPYC 7763 64-Core Processor · Node v26.13.0_

| bench | latest | Δ7d | Δ30d | min | max | points |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 chunks from one source stream | 859.41µs |  |  | 476.48µs | 859.41µs | 4 |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 controller.enqueue calls | 1.228ms |  |  | 738.70µs | 1.228ms | 4 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 16 deltas × 250 chars | 57.79µs | +73.2% | +73.2% ⚠︎ | 34.03µs | 57.79µs | 4 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 250 deltas × 16 chars | 648.88µs | +67.6% | +67.6% ⚠︎ | 379.72µs | 648.88µs | 4 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 4000 deltas × 1 char (per-token) | 10.154ms | +66.9% | +66.9% ⚠︎ | 5.883ms | 10.154ms | 4 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 100 deltas | 281.61µs | +72.0% | +72.0% ⚠︎ | 158.96µs | 281.61µs | 4 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 1000 deltas | 2.557ms | +64.1% | +64.1% ⚠︎ | 1.444ms | 2.557ms | 4 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 4000 deltas | 10.034ms | +64.4% | +64.4% ⚠︎ | 5.858ms | 10.034ms | 4 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 100 deltas | 9.76µs | +50.8% | +50.8% ⚠︎ | 5.69µs | 9.76µs | 4 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 1000 deltas | 86.15µs | +63.9% | +63.9% ⚠︎ | 47.39µs | 86.15µs | 4 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 4000 deltas | 340.27µs | +62.3% | +62.3% ⚠︎ | 185.79µs | 340.27µs | 4 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 128 parts, distinct providers (stress) | 140.93µs |  |  | 51.69µs | 140.93µs | 4 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 16 parts, one repeated provider | 81.28µs |  |  | 26.56µs | 81.28µs | 4 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 2 parts, one repeated provider | 83.42µs |  |  | 29.80µs | 83.42µs | 4 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 512 parts, distinct providers (stress) | 325.02µs |  |  | 173.51µs | 325.02µs | 4 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 10 static tools | 75.95µs |  |  | 42.17µs | 75.95µs | 4 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 100 static tools | 692.65µs |  |  | 443.80µs | 692.65µs | 4 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 10 static tools | 9.95µs |  |  | 5.61µs | 9.95µs | 4 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 100 static tools | 82.70µs |  |  | 48.78µs | 82.70µs | 4 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 100 deltas | 762.40µs | +34.1% | +34.1% ⚠︎ | 401.19µs | 762.40µs | 4 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 1000 deltas | 6.083ms | +17.3% | +17.3% ⚠︎ | 3.536ms | 6.083ms | 4 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 4000 deltas | 23.899ms | +16.3% | +16.3% ⚠︎ | 14.250ms | 23.899ms | 4 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 100 deltas | 350.65µs | -11.7% | -11.7% ⚠︎ | 203.90µs | 350.65µs | 4 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 1000 deltas | 3.342ms | -9.4% | -9.4% | 2.016ms | 3.342ms | 4 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 4000 deltas | 13.264ms | -11.0% | -11.0% ⚠︎ | 8.083ms | 13.264ms | 4 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 1000 messages, 6-part replies | 275.38µs |  |  | 146.96µs | 275.38µs | 4 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 5000 messages, 20-part replies | 2.191ms |  |  | 901.12µs | 2.191ms | 4 |
| external-message-conversion › core: external message reasoning continuations › 100 matches | 69.32µs |  |  | 36.38µs | 69.32µs | 4 |
| external-message-conversion › core: external message reasoning continuations › 1000 matches | 698.19µs |  |  | 369.87µs | 698.19µs | 4 |
| external-message-conversion › core: external message reasoning continuations › 5000 matches | 3.720ms |  |  | 1.948ms | 3.720ms | 4 |
| external-message-conversion › core: external message tool results › 100 matches | 82.03µs |  |  | 41.24µs | 82.03µs | 4 |
| external-message-conversion › core: external message tool results › 1000 matches | 820.91µs |  |  | 412.26µs | 820.91µs | 4 |
| external-message-conversion › core: external message tool results › 5000 matches | 4.283ms |  |  | 2.154ms | 4.283ms | 4 |
| external-message-conversion › core: external message unique tool calls › 100 matches | 42.05µs |  |  | 22.21µs | 42.05µs | 4 |
| external-message-conversion › core: external message unique tool calls › 1000 matches | 419.19µs |  |  | 203.99µs | 419.19µs | 4 |
| external-message-conversion › core: external message unique tool calls › 5000 matches | 2.201ms |  |  | 1.104ms | 2.201ms | 4 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 1 text parts | 0.28µs | +169.7% | +169.7% ⚠︎ | 0.15µs | 0.28µs | 4 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 10 text parts | 0.46µs | +165.9% | +165.9% ⚠︎ | 0.27µs | 0.46µs | 4 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 100 text parts | 2.41µs | +129.9% | +129.9% ⚠︎ | 1.57µs | 2.41µs | 4 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 1 tool calls | 0.67µs | +108.5% | +108.5% ⚠︎ | 0.37µs | 0.67µs | 4 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 10 tool calls | 3.41µs | +104.2% | +104.2% ⚠︎ | 1.72µs | 3.41µs | 4 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 100 tool calls | 30.97µs | +97.9% | +97.9% ⚠︎ | 15.52µs | 30.97µs | 4 |
| interactable-array-patches › core: id-keyed interactable array patches › 1000 items and patches | 144.99µs |  |  | 94.45µs | 144.99µs | 4 |
| interactable-array-patches › core: id-keyed interactable array patches › 5000 items and patches | 816.23µs |  |  | 481.41µs | 816.23µs | 4 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tilde runs on one line | 2.839ms |  |  | 1.429ms | 2.839ms | 4 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tildes after prose | 207.34µs |  |  | 103.49µs | 207.34µs | 4 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 triple-backtick spans on one line | 3.667ms |  |  | 1.905ms | 3.667ms | 4 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 5,000 code spans in one paragraph | 492.76µs |  |  | 271.77µs | 492.76µs | 4 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, mixed message, 100 sections | 722.70µs |  |  | 393.09µs | 722.70µs | 4 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tilde runs on one line | 7.826ms |  |  | 4.008ms | 7.826ms | 4 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tildes after prose | 932.81µs |  |  | 467.20µs | 932.81µs | 4 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 triple-backtick spans on one line | 24.360ms |  |  | 11.077ms | 24.360ms | 4 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 5,000 code spans in one paragraph | 3.627ms |  |  | 1.849ms | 3.627ms | 4 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, mixed message, 100 sections | 2.754ms |  |  | 1.494ms | 2.754ms | 4 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown | 3.178ms |  |  | 1.666ms | 3.178ms | 4 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown deferred | 3.374ms |  |  | 1.727ms | 3.374ms | 4 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown | 21.687ms |  |  | 11.568ms | 21.687ms | 4 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown deferred | 23.240ms |  |  | 13.259ms | 23.240ms | 4 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 1 paragraphs | 1.495ms | +184.9% | +184.9% ⚠︎ | 823.48µs | 1.495ms | 4 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 10 paragraphs | 3.156ms | +204.8% | +204.8% ⚠︎ | 1.568ms | 3.156ms | 4 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 50 paragraphs | 9.843ms | +132.4% | +132.4% ⚠︎ | 6.011ms | 9.843ms | 4 |
| markdown-streaming › react-markdown: the same token with defer on › 1 paragraphs deferred | 1.197ms | +6.8% | +6.8% | 1.197ms | 1.382ms | 4 |
| markdown-streaming › react-markdown: the same token with defer on › 10 paragraphs deferred | 1.926ms | +83.6% | +83.6% ⚠︎ | 1.352ms | 1.926ms | 4 |
| markdown-streaming › react-markdown: the same token with defer on › 50 paragraphs deferred | 4.458ms | +53.0% | +53.0% ⚠︎ | 2.917ms | 4.458ms | 4 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 1000 character argument in 16-character deltas | 341.30µs |  |  | 204.84µs | 341.30µs | 4 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 10000 character argument in 16-character deltas | 2.692ms |  |  | 1.722ms | 2.692ms | 4 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 500 short object entries in 16-character deltas | 302.802ms |  |  | 159.907ms | 302.802ms | 4 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 50000 character argument in 16-character deltas | 12.718ms |  |  | 8.250ms | 12.718ms | 4 |
| react-pi-message-projection › react-pi: streaming tail projection › 10 stable messages | 2.31µs |  |  | 1.24µs | 2.31µs | 4 |
| react-pi-message-projection › react-pi: streaming tail projection › 1000 stable messages | 9.91µs |  |  | 5.48µs | 9.91µs | 4 |
| react-pi-message-projection › react-pi: streaming tail projection › 5000 stable messages | 41.19µs |  |  | 20.30µs | 41.19µs | 4 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 1 chunks | 6.44µs |  |  | 4.47µs | 7.32µs | 4 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 101 chunks | 21.78µs |  |  | 14.31µs | 21.78µs | 4 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1 chunks | 62.85µs |  |  | 45.85µs | 72.46µs | 4 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1025 chunks | 301.46µs |  |  | 194.20µs | 301.46µs | 4 |
| thread-scaling › external-store thread: mount+unmount by message count › 10 messages | 7.164ms | +316.8% | +316.8% ⚠︎ | 4.079ms | 7.164ms | 4 |
| thread-scaling › external-store thread: mount+unmount by message count › 100 messages | 46.091ms | +316.8% | +316.8% ⚠︎ | 25.271ms | 46.091ms | 4 |
| thread-scaling › external-store thread: mount+unmount by message count › 1000 messages | 487.662ms | +196.2% | +196.2% ⚠︎ | 323.257ms | 487.662ms | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 10 messages | 653.21µs |  |  | 255.66µs | 653.21µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 100 messages | 986.05µs |  |  | 441.32µs | 986.05µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 1000 messages | 4.465ms |  |  | 2.432ms | 4.465ms | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 10 messages | 632.25µs |  |  | 277.82µs | 632.25µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 100 messages | 1.432ms |  |  | 757.09µs | 1.432ms | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 1000 messages | 15.648ms |  |  | 8.826ms | 15.648ms | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 10 messages | 672.64µs |  |  | 262.22µs | 672.64µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 100 messages | 1.120ms |  |  | 543.05µs | 1.120ms | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 1000 messages | 10.683ms |  |  | 5.784ms | 10.683ms | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 10 messages | 344.42µs |  |  | 125.13µs | 344.42µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 100 messages | 561.29µs |  |  | 252.74µs | 561.29µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 1000 messages | 3.404ms |  |  | 1.668ms | 3.404ms | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 10 messages | 24.07µs |  |  | 9.90µs | 24.07µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 100 messages | 40.91µs |  |  | 20.67µs | 40.91µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 1000 messages | 281.62µs |  |  | 143.53µs | 281.62µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 10 messages | 687.92µs | +159.0% | +159.0% ⚠︎ | 306.59µs | 687.92µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 100 messages | 1.181ms | -24.4% | -24.4% ⚠︎ | 520.07µs | 1.181ms | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 1000 messages | 8.730ms | -76.6% | -76.6% ⚠︎ | 5.509ms | 9.374ms | 4 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 1000 bytes | 262.44µs |  |  | 146.66µs | 262.44µs | 4 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 10000 bytes | 2.262ms |  |  | 1.366ms | 2.262ms | 4 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 5000 bytes | 1.140ms |  |  | 667.89µs | 1.140ms | 4 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 1000 bytes | 317.67µs |  |  | 179.78µs | 317.67µs | 4 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 10000 bytes | 2.615ms |  |  | 1.563ms | 2.615ms | 4 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 5000 bytes | 1.311ms |  |  | 787.57µs | 1.311ms | 4 |
| tool-args › assistant-stream: complete accumulated arguments (single delta) › 10,000 array elements | 352.71µs |  |  | 193.61µs | 352.71µs | 4 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 array entries | 27.397ms |  |  | 15.347ms | 27.397ms | 4 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 object entries | 677.556ms |  |  | 406.028ms | 677.556ms | 4 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 1000 bytes | 240.30µs |  |  | 131.86µs | 240.30µs | 4 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 10000 bytes | 1.869ms |  |  | 1.095ms | 1.869ms | 4 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 5000 bytes | 951.39µs |  |  | 546.32µs | 951.39µs | 4 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 10000 bytes | 211.12µs |  |  | 108.45µs | 211.12µs | 4 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 50000 bytes | 976.85µs |  |  | 492.66µs | 976.85µs | 4 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 10000 bytes | 234.25µs |  |  | 116.87µs | 234.25µs | 4 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 50000 bytes | 1.018ms |  |  | 513.58µs | 1.018ms | 4 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRoot | 3.678ms | +122.5% | +122.5% ⚠︎ | 2.128ms | 3.678ms | 4 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootDeps | 3.573ms | +120.5% | +120.5% ⚠︎ | 2.140ms | 3.573ms | 4 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootStable | 3.542ms | +120.0% | +120.0% ⚠︎ | 2.049ms | 3.542ms | 4 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › react | 3.758ms | +161.9% | +161.9% ⚠︎ | 2.055ms | 3.758ms | 4 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › tapRoot | 2.245ms | +149.7% | +149.7% ⚠︎ | 1.279ms | 2.245ms | 4 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRoot | 3.384ms | +134.1% | +134.1% ⚠︎ | 1.923ms | 3.384ms | 4 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootDeps | 3.379ms | +140.9% | +140.9% ⚠︎ | 1.853ms | 3.379ms | 4 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootStable | 248.95µs | +43.3% | +43.3% ⚠︎ | 163.47µs | 248.95µs | 4 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › react | 147.28µs | +139.4% | +139.4% ⚠︎ | 83.51µs | 147.28µs | 4 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › tapRoot | 1.748ms | +131.3% | +131.3% ⚠︎ | 977.24µs | 1.748ms | 4 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › deps | 1.963ms | +160.9% | +160.9% ⚠︎ | 1.016ms | 1.963ms | 4 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › no-deps | 2.108ms | +176.8% | +176.8% ⚠︎ | 1.080ms | 2.108ms | 4 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › deps | 54.54µs | +47.3% | +47.3% ⚠︎ | 29.27µs | 54.54µs | 4 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › no-deps | 55.23µs | -91.3% | -91.3% ⚠︎ | 30.72µs | 55.23µs | 4 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › deps | 72.30µs | +108.5% | +108.5% ⚠︎ | 42.36µs | 72.30µs | 4 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › no-deps | 1.516ms | +140.5% | +140.5% ⚠︎ | 796.05µs | 1.516ms | 4 |

informational; points come from different runners of the same class, so read trends, not single deltas.
