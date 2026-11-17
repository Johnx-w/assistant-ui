## aui-perf nightly record

_9 points · 2026-09-03T05:27:14.273Z to 2026-11-17T13:44:27.567Z · latest runner: Intel(R) Xeon(R) 6975P-C · Node v26.13.0_

| bench | latest | Δ7d | Δ30d | min | max | points |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 chunks from one source stream | 531.95µs |  |  | 476.48µs | 859.41µs | 5 |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 controller.enqueue calls | 765.99µs |  |  | 738.70µs | 1.228ms | 5 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 16 deltas × 250 chars | 35.15µs | +5.3% | +5.3% | 34.03µs | 57.79µs | 5 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 250 deltas × 16 chars | 370.90µs | -4.2% | -4.2% | 370.90µs | 648.88µs | 5 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 4000 deltas × 1 char (per-token) | 5.741ms | -5.7% | -5.7% | 5.741ms | 10.154ms | 5 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 100 deltas | 153.07µs | -6.5% | -6.5% | 153.07µs | 281.61µs | 5 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 1000 deltas | 1.401ms | -10.1% | -10.1% ⚠︎ | 1.401ms | 2.557ms | 5 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 4000 deltas | 5.634ms | -7.7% | -7.7% | 5.634ms | 10.034ms | 5 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 100 deltas | 6.16µs | -4.8% | -4.8% | 5.69µs | 9.76µs | 5 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 1000 deltas | 52.09µs | -0.9% | -0.9% | 47.39µs | 86.15µs | 5 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 4000 deltas | 205.48µs | -2.0% | -2.0% | 185.79µs | 340.27µs | 5 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 128 parts, distinct providers (stress) | 55.84µs |  |  | 51.69µs | 140.93µs | 5 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 16 parts, one repeated provider | 30.32µs |  |  | 26.56µs | 81.28µs | 5 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 2 parts, one repeated provider | 31.62µs |  |  | 29.80µs | 83.42µs | 5 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 512 parts, distinct providers (stress) | 202.12µs |  |  | 173.51µs | 325.02µs | 5 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 10 static tools | 43.49µs |  |  | 42.17µs | 75.95µs | 5 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 100 static tools | 449.57µs |  |  | 443.80µs | 692.65µs | 5 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 10 static tools | 6.20µs |  |  | 5.61µs | 9.95µs | 5 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 100 static tools | 53.02µs |  |  | 48.78µs | 82.70µs | 5 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 100 deltas | 443.50µs | -22.0% | -22.0% ⚠︎ | 401.19µs | 762.40µs | 5 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 1000 deltas | 3.723ms | -28.2% | -28.2% ⚠︎ | 3.536ms | 6.083ms | 5 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 4000 deltas | 14.430ms | -29.8% | -29.8% ⚠︎ | 14.250ms | 23.899ms | 5 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 100 deltas | 203.07µs | -48.9% | -48.9% ⚠︎ | 203.07µs | 350.65µs | 5 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 1000 deltas | 1.993ms | -46.0% | -46.0% ⚠︎ | 1.993ms | 3.342ms | 5 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 4000 deltas | 7.917ms | -46.9% | -46.9% ⚠︎ | 7.917ms | 13.264ms | 5 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 1000 messages, 6-part replies | 199.21µs |  |  | 146.96µs | 275.38µs | 5 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 5000 messages, 20-part replies | 1.248ms |  |  | 901.12µs | 2.191ms | 5 |
| external-message-conversion › core: external message reasoning continuations › 100 matches | 42.13µs |  |  | 36.38µs | 69.32µs | 5 |
| external-message-conversion › core: external message reasoning continuations › 1000 matches | 413.70µs |  |  | 369.87µs | 698.19µs | 5 |
| external-message-conversion › core: external message reasoning continuations › 5000 matches | 2.236ms |  |  | 1.948ms | 3.720ms | 5 |
| external-message-conversion › core: external message tool results › 100 matches | 52.51µs |  |  | 41.24µs | 82.03µs | 5 |
| external-message-conversion › core: external message tool results › 1000 matches | 523.95µs |  |  | 412.26µs | 820.91µs | 5 |
| external-message-conversion › core: external message tool results › 5000 matches | 2.743ms |  |  | 2.154ms | 4.283ms | 5 |
| external-message-conversion › core: external message unique tool calls › 100 matches | 27.01µs |  |  | 22.21µs | 42.05µs | 5 |
| external-message-conversion › core: external message unique tool calls › 1000 matches | 253.28µs |  |  | 203.99µs | 419.19µs | 5 |
| external-message-conversion › core: external message unique tool calls › 5000 matches | 1.375ms |  |  | 1.104ms | 2.201ms | 5 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 1 text parts | 0.17µs | +68.5% | +68.5% ⚠︎ | 0.15µs | 0.28µs | 5 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 10 text parts | 0.30µs | +75.2% | +75.2% ⚠︎ | 0.27µs | 0.46µs | 5 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 100 text parts | 1.62µs | +54.2% | +54.2% ⚠︎ | 1.57µs | 2.41µs | 5 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 1 tool calls | 0.37µs | +15.7% | +15.7% ⚠︎ | 0.37µs | 0.67µs | 5 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 10 tool calls | 2.21µs | +32.4% | +32.4% ⚠︎ | 1.72µs | 3.41µs | 5 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 100 tool calls | 19.88µs | +27.0% | +27.0% ⚠︎ | 15.52µs | 30.97µs | 5 |
| interactable-array-patches › core: id-keyed interactable array patches › 1000 items and patches | 111.84µs |  |  | 94.45µs | 144.99µs | 5 |
| interactable-array-patches › core: id-keyed interactable array patches › 5000 items and patches | 623.78µs |  |  | 481.41µs | 816.23µs | 5 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tilde runs on one line | 1.937ms |  |  | 1.429ms | 2.839ms | 5 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tildes after prose | 119.17µs |  |  | 103.49µs | 207.34µs | 5 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 triple-backtick spans on one line | 2.566ms |  |  | 1.905ms | 3.667ms | 5 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 5,000 code spans in one paragraph | 337.02µs |  |  | 271.77µs | 492.76µs | 5 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, mixed message, 100 sections | 491.60µs |  |  | 393.09µs | 722.70µs | 5 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tilde runs on one line | 5.773ms |  |  | 4.008ms | 7.826ms | 5 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tildes after prose | 485.62µs |  |  | 467.20µs | 932.81µs | 5 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 triple-backtick spans on one line | 14.373ms |  |  | 11.077ms | 24.360ms | 5 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 5,000 code spans in one paragraph | 2.283ms |  |  | 1.849ms | 3.627ms | 5 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, mixed message, 100 sections | 1.775ms |  |  | 1.494ms | 2.754ms | 5 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown | 1.955ms |  |  | 1.666ms | 3.178ms | 5 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown deferred | 2.182ms |  |  | 1.727ms | 3.374ms | 5 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown | 13.319ms |  |  | 11.568ms | 21.687ms | 5 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown deferred | 14.637ms |  |  | 13.259ms | 23.240ms | 5 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 1 paragraphs | 1.121ms | +113.6% | +113.6% ⚠︎ | 823.48µs | 1.495ms | 5 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 10 paragraphs | 1.871ms | +80.7% | +80.7% ⚠︎ | 1.568ms | 3.156ms | 5 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 50 paragraphs | 6.426ms | +51.8% | +51.8% ⚠︎ | 6.011ms | 9.843ms | 5 |
| markdown-streaming › react-markdown: the same token with defer on › 1 paragraphs deferred | 1.455ms | +29.8% | +29.8% ⚠︎ | 1.197ms | 1.455ms | 5 |
| markdown-streaming › react-markdown: the same token with defer on › 10 paragraphs deferred | 1.350ms | +28.7% | +28.7% ⚠︎ | 1.350ms | 1.926ms | 5 |
| markdown-streaming › react-markdown: the same token with defer on › 50 paragraphs deferred | 3.719ms | +27.6% | +27.6% ⚠︎ | 2.917ms | 4.458ms | 5 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 1000 character argument in 16-character deltas | 191.35µs |  |  | 191.35µs | 341.30µs | 5 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 10000 character argument in 16-character deltas | 1.575ms |  |  | 1.575ms | 2.692ms | 5 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 500 short object entries in 16-character deltas | 181.036ms |  |  | 159.907ms | 302.802ms | 5 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 50000 character argument in 16-character deltas | 8.017ms |  |  | 8.017ms | 12.718ms | 5 |
| react-pi-message-projection › react-pi: streaming tail projection › 10 stable messages | 1.15µs |  |  | 1.15µs | 2.31µs | 5 |
| react-pi-message-projection › react-pi: streaming tail projection › 1000 stable messages | 5.35µs |  |  | 5.35µs | 9.91µs | 5 |
| react-pi-message-projection › react-pi: streaming tail projection › 5000 stable messages | 25.36µs |  |  | 20.30µs | 41.19µs | 5 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 1 chunks | 4.70µs |  |  | 4.47µs | 7.32µs | 5 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 101 chunks | 15.14µs |  |  | 14.31µs | 21.78µs | 5 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1 chunks | 45.79µs |  |  | 45.79µs | 72.46µs | 5 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1025 chunks | 197.01µs |  |  | 194.20µs | 301.46µs | 5 |
| thread-scaling › external-store thread: mount+unmount by message count › 10 messages | 4.181ms | +143.2% | +143.2% ⚠︎ | 4.079ms | 7.164ms | 5 |
| thread-scaling › external-store thread: mount+unmount by message count › 100 messages | 24.114ms | +118.1% | +118.1% ⚠︎ | 24.114ms | 46.091ms | 5 |
| thread-scaling › external-store thread: mount+unmount by message count › 1000 messages | 290.658ms | +76.5% | +76.5% ⚠︎ | 290.658ms | 487.662ms | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 10 messages | 357.02µs |  |  | 255.66µs | 653.21µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 100 messages | 605.43µs |  |  | 441.32µs | 986.05µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 1000 messages | 3.157ms |  |  | 2.432ms | 4.465ms | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 10 messages | 361.33µs |  |  | 277.82µs | 632.25µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 100 messages | 1.087ms |  |  | 757.09µs | 1.432ms | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 1000 messages | 8.080ms |  |  | 8.080ms | 15.648ms | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 10 messages | 348.30µs |  |  | 262.22µs | 672.64µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 100 messages | 847.51µs |  |  | 543.05µs | 1.120ms | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 1000 messages | 5.296ms |  |  | 5.296ms | 10.683ms | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 10 messages | 152.82µs |  |  | 125.13µs | 344.42µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 100 messages | 365.88µs |  |  | 252.74µs | 561.29µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 1000 messages | 2.685ms |  |  | 1.668ms | 3.404ms | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 10 messages | 10.45µs |  |  | 9.90µs | 24.07µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 100 messages | 21.98µs |  |  | 20.67µs | 40.91µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 1000 messages | 198.72µs |  |  | 143.53µs | 281.62µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 10 messages | 394.97µs | +48.7% | +48.7% ⚠︎ | 306.59µs | 687.92µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 100 messages | 858.54µs | -45.1% | -45.1% ⚠︎ | 520.07µs | 1.181ms | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 1000 messages | 5.400ms | -85.5% | -85.5% ⚠︎ | 5.400ms | 9.374ms | 5 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 1000 bytes | 153.30µs |  |  | 146.66µs | 262.44µs | 5 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 10000 bytes | 1.387ms |  |  | 1.366ms | 2.262ms | 5 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 5000 bytes | 705.76µs |  |  | 667.89µs | 1.140ms | 5 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 1000 bytes | 171.71µs |  |  | 171.71µs | 317.67µs | 5 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 10000 bytes | 1.508ms |  |  | 1.508ms | 2.615ms | 5 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 5000 bytes | 766.53µs |  |  | 766.53µs | 1.311ms | 5 |
| tool-args › assistant-stream: complete accumulated arguments (single delta) › 10,000 array elements | 242.28µs |  |  | 193.61µs | 352.71µs | 5 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 array entries | 16.229ms |  |  | 15.347ms | 27.397ms | 5 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 object entries | 624.502ms |  |  | 406.028ms | 677.556ms | 5 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 1000 bytes | 127.29µs |  |  | 127.29µs | 240.30µs | 5 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 10000 bytes | 1.050ms |  |  | 1.050ms | 1.869ms | 5 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 5000 bytes | 530.92µs |  |  | 530.92µs | 951.39µs | 5 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 10000 bytes | 139.65µs |  |  | 108.45µs | 211.12µs | 5 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 50000 bytes | 679.75µs |  |  | 492.66µs | 976.85µs | 5 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 10000 bytes | 152.54µs |  |  | 116.87µs | 234.25µs | 5 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 50000 bytes | 703.43µs |  |  | 513.58µs | 1.018ms | 5 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRoot | 2.182ms | +32.0% | +32.0% ⚠︎ | 2.128ms | 3.678ms | 5 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootDeps | 2.232ms | +37.7% | +37.7% ⚠︎ | 2.140ms | 3.573ms | 5 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootStable | 2.145ms | +33.2% | +33.2% ⚠︎ | 2.049ms | 3.542ms | 5 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › react | 2.156ms | +50.2% | +50.2% ⚠︎ | 2.055ms | 3.758ms | 5 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › tapRoot | 1.389ms | +54.4% | +54.4% ⚠︎ | 1.279ms | 2.245ms | 5 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRoot | 2.108ms | +45.9% | +45.9% ⚠︎ | 1.923ms | 3.384ms | 5 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootDeps | 2.053ms | +46.4% | +46.4% ⚠︎ | 1.853ms | 3.379ms | 5 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootStable | 229.66µs | +32.2% | +32.2% ⚠︎ | 163.47µs | 248.95µs | 5 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › react | 95.57µs | +55.3% | +55.3% ⚠︎ | 83.51µs | 147.28µs | 5 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › tapRoot | 1.107ms | +46.6% | +46.6% ⚠︎ | 977.24µs | 1.748ms | 5 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › deps | 1.217ms | +61.8% | +61.8% ⚠︎ | 1.016ms | 1.963ms | 5 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › no-deps | 1.303ms | +71.0% | +71.0% ⚠︎ | 1.080ms | 2.108ms | 5 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › deps | 29.95µs | -19.1% | -19.1% ⚠︎ | 29.27µs | 54.54µs | 5 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › no-deps | 32.09µs | -95.0% | -95.0% ⚠︎ | 30.72µs | 55.23µs | 5 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › deps | 44.37µs | +28.0% | +28.0% ⚠︎ | 42.36µs | 72.30µs | 5 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › no-deps | 1.024ms | +62.6% | +62.6% ⚠︎ | 796.05µs | 1.516ms | 5 |

informational; points come from different runners of the same class, so read trends, not single deltas.
