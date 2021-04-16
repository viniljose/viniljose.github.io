<h1 id="header-1">Introduction to RSocket</h1>

RSocket is a binary protocol for use on byte stream transports such as TCP, WebSockets, and Aeron.

<ul>
  <li>support for interaction models beyond request/response such as streaming responses and push</li>
  <li>application-level flow control semantics (async pull/push of bounded batch sizes) across network boundaries</li>
  <li>binary, multiplexed use of a single connection</li>
  <li>support resumption of long-lived subscriptions across transport connections</li>
  <li>need of an application protocol in order to use transport protocols such as WebSockets and Aeron</li>
</ul>



This “RSocket” protocol is a formal communication protocol that embraces the “reactive” principles.

RSocket seeks to:
<blockquote>
<p>Reduce perceived latency and increase system efficiency by supporting non-blocking, duplex, async application communication with flow control over multiple transports from any language</p>
</blockquote>


Reduce hardware footprint (and thus cost and operational complexity) by:
<blockquote>
<p>increasing CPU and memory efficiency through use of binary encoding</p>
<p>avoiding redundant work by allowing persistent connections</p>
</blockquote>


Reduce perceived user latency by:
<blockquote>
<p>avoiding handshakes and the associated round-trip network overhead</p>
<p>reducing computation time by using binary encoding</p>
<p>allocating less memory and reducing garbage collection cost</p>
</blockquote>



<h4 id="header-4">Interaction Models</h4>
<ol>
  <li>Request/Response (single-response)</li>
  <li>Request/Stream (multi-response, finite)</li>
  <li>Fire-and-Forget</li>
  <li>Channel</li>
</ol>


<h4 id="header-4">Request/Response (single-response)</h4>

These request/response interactions can be considered optimized “streams of only 1 response”, and are asynchronous messages multiplexed over a single connection.

The consumer “waits” for the response message, so it looks like a typical request/response, but underneath it never synchronously blocks.

<div class="highlight"><code>Future<Payload> response = socketClient.requestResponse(requestPayload);
</code></div>

    


<h4 id="header-4">References</h4>
<p><a href="https://rsocket.io/">https://rsocket.io</a></p>





