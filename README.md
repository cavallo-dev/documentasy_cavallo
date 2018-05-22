# documentasy_cavallo


<h1 id="introduction">Introduction</h1>
<a href="javascript:" id="return-to-top"><i class="fa fa-hand-o-up" aria-hidden="true"></i></a>


<h3 id="introduction">Introduction</h3>

<p>Welcome to Cavallocoin.io API documentation! Cavallocoin is a simple,accessed over HTTP or HTTPS from the cavallocoin.io domain. </p>



<h1 id="integrasi">Integration</h1>

<h3 id="tahapan-integrasi">How to make integrate :</h3>

<ol>
<li>Develop (make) modul interface on your system (member) that contains of sender functions transaction request  <strong>to environment development</strong> system Cavallocoin.io based on spesification.</li>
</ol>

<h2 id="development">Development</h2>

<p>We dedicate this environmental development to ease you doing integration modul your H2H system to Cavallocoin.io. </p>

<p>In this phase, please make an interface modul on your system (member) who has to send the request to URL API in Cavallocoin.io which appropriates with the spesification.</p>

<h3 id="target-url-api-development">Target URL API Development</h3>

<table><thead>
<tr>
<th>Format</th>
<th>Target URL</th>
</tr>
</thead><tbody>
<tr>
<td>JSON</td>
<td><code class="prettyprint">POST https://www.cavallocoin.io/api</code></td>
</tr>
</tbody></table>

<h1 id="referensi-api">API Referention</h1>

<p>Please use message format which is convenient for your (member), there is some format that is available, such as : JSON. </p>


<p>You can check your current limits and usage via a POST on the following endpoint, outside of our normal coin/chain pattern:</p>

<p> Generally, in the option JSON format , every transaction request is sent through HTTPS protocol <code class="prettyprint">HTTPS</code> to target URL API cavallocoin.io with condition: </p>

<ol>
<li>header <code>Content-Type: application/json</code>  to JSON format.</li>
<li>contains to contents request according to API cavallocoin.io spesification.</li>
<li>And set <code>Authorization: Bearer $api_token</code>.</li>
</ol>

          <h2 id="make-transaction">Make Transaction</h2>

<p>Making the latest transaction.<br>
first you need to provide the input password, wallet, and amount. </p>

<blockquote>
<p>Make Transaction Request</p>
</blockquote>
<pre class="highlight json"><code><span class="p">curl https://www.cavallocoin.io/api/transac</span>
<span class="p">{</span><span class="w">
  </span><span class="nt">"password"</span><span class="p">:</span><span class="w"> </span><span class="s2">"YOUR_PASSWORD"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"address"</span><span class="p">:</span><span class="w"> </span><span class="s2">"MEMBER_ADDRESS"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"amount"</span><span class="p">:</span><span class="w"> </span><span class="s2">"MEMBER_AMOUNT"</span><span class="p">,</span><span class="w">
</span><span class="p">}</span><span class="w">
</span></code></pre>
<p><strong>Request Parameters</strong></p>

 <table><thead>
              <tr>
              <th>Parameters</th>
              <th>Value</th>
              <th>Description</th>
              </tr>
              </thead><tbody>
              <tr>
              <td>password</td>
              <td>YOUR_PASSWORD</code></td>
              <td>your password</td>
              </tr>
              <tr>
              <td>address</td>
              <td>MEMBER_ADDRESS</td>
              <td>member address.</td>
              </tr>
              <tr>
              <td>amount</td>
              <td>MEMBER_AMOUNT</td>
              <td>amount member.</td>
              </tr>

              </tbody></table>


<blockquote>
<p>Make Transaction Response</p>
</blockquote>

<pre class="highlight json"><code><span class="p">{</span><span class="w">
  </span><span class="nt">"success"</span><span class="p">:</span><span class="w"> </span><span class="s2">"true"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"data"</span><span class="p">:</span><span class="w"><span class="p">{</span><span class="w">
  <span class="nt">"message"</span><span class="p">:</span> </span><span class="s2">"Your transaction has ben success"</span><span class="p">,</span><span class="w"><span class="w">
  <span class="nt">"balance"</span><span class="p">:</span> </span><span class="s2">"0.000000000"</span><span class="p">,<span class="w"></span><span class="p">
  </span><span class="nt">"block"</span><span class="p">:</span><span class="w"><span class="p">{</span>
  <span class="nt">"hash"</span><span class="p">:</span><span class="w"> </span><span class="s2">"e1ec83047d0beb49ba9e2f480f206386869e81dbf461ee1c15bc7592e003453a"</span><span class="p">,</span>
  <span class="nt">"sender_id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"5a16c59a402c5a04a84ea3be"</span><span class="p">,</span>
  <span class="nt">"receiver_id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"5aa8b74e402c5a4ebf2cf2a2"</span><span class="p">,</span>
  <span class="nt">"data"</span><span class="p">:</span><span class="w"> </span><span class="s2">"5fd85baed63db0722d44d7063bbc154daedc38ee304e22cc23fe3bacffe9ca6a"</span><span class="p">,</span>
  <span class="nt">"value"</span><span class="p">:</span><span class="w"> </span><span class="s2">"1.0000000000"</span><span class="p">,</span>
  <span class="nt">"created_at"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2018-05-01 11:20:17"</span><span class="p">,</span>
  <span class="nt">"_id"</span><span class="p">:</span><span class="w"> </span><span class="s2">"5ae83151402c5a17653f06e3"</span><span class="w">
</span><span class="p">}</span><span class="w"><span class="p">}</span>
<span class="p">}</span>
</span></code></pre>

          <h2 id="create-wallet">Create Wallet</h2>

<p></p>

<blockquote>
<p>Create Wallet Request</p>
</blockquote>
<pre class="highlight json"><code><span class="p">curl https://www.cavallocoin.io/api/new</span><br>
<span class="p">{</span><span class="w">
</span><span class="nt">"password"</span><span class="p">:</span><span class="w"> </span><span class="s2">"YOUR_PASSWORD"</span>
<span class="p">}</span><span class="w">
</span></code></pre> 
<p><strong>Parameters Request</strong></p>

<table><thead>
              <tr>
              <th>Parameters</th>
              <th>Value</th>
              <th>Description</th>
              </tr>
              </thead><tbody>
              <tr>
              <td>password</td>
              <td>YOUR_PASSWORD</code></td>
              <td>your password</td>
              </tr>

</tbody></table>

<!-- <p>Nama kode produk untuk melakukan pengecekan harga :
<br /><br />"TELKOMSEL", "INDOSAT", "XLAXIATA", "SMARTFREN", "THREE", "AXIS",
<br />"PULSAPASCA", "PLN", "PDAM", "TV", "TELKOM", "FINANCE", "ASURANSI",
<br />"CC"</p> -->

<blockquote>
<p>Create Wallet Response</p>
</blockquote>
<pre class="highlight json"><code><span class="p">curl https://www.cavallocoin.io/api/new</span>
<span class="p">{</span><span class="w">
</span><span class="nt">"success"</span><span class="p">:</span><span class="w"> </span><span class="s2">"true"</span><span class="p">,</span><span class="w">
</span><span class="nt">"data"</span><span class="p">:</span><span class="p">{</span><br>
 <span class="nt">"message"</span><span class="p">:</span> <span class="s2">"Account created"</span><span>,</span><span class="w">
 </span>
 <span class="nt">"detail"</span><span class="p">:</span><span class="p">{</span>
 <br><span class="w"> </span>
 <span class="nt"> "wallet"</span><span class="p">:</span><span class="s2">"SYrOykTM6LEL3jhCxQEXrqXMO8lhVMicoYu9owGp46YLn8PaGVNOTB5ekz54pxPGk6VAgkX9cGiYR"</span>,
 <span class="nt"> "balance"</span><span class="p">:</span><span class="s2">"0"</span>,
 <span class="nt"> "secret_key"</span><span class="p">:</span><span class="s2">"645716fb88007616783d818c9b2a7d616fc97154932757357e3e79a70363c5ee673ffce2d4453fd3de8e817eb7aa86d9b79339e850aa35c26e387c427e183485"</span>,
 <span class="nt"> "id"</span><span class="p">:</span><span class="s2">"5ae825d8402c5a230812ea73"</span>,
 <span class="nt"> "token"</span><span class="p">:</span><span class="s2">"010fa85d20fa4e586254c9a386a57a9f2ce1937ae904d22f7865aa5f09aea7626de2b22897ada7f5e4843ecdee0135281733807686dd8b3bad7efeae4e3cabd3"</span><span class="w"></span><span class="p">}</span>
 <span class="p">}</span>
 <span class="p">}</span>
 <span class="w"></span></code></pre>


          <h2 id="check-ballance">Check Balance</h2>

<p></p>

<blockquote>
<p>Check Balance Request</p>
</blockquote>
<pre class="highlight json"><code><span class="p">curl https://www.cavallocoin.io/api/balance</span>
<span class="p">{</span><span class="w">
  </span><span class="nt">"password"</span><span class="p">:</span><span class="w"> </span><span class="s2">"YOUR_PASSWORD"</span><span class="p">,</span><span class="w">
  </span><span class="nt">"key"</span><span class="p">:</span><span class="w"> </span><span class="s2">"YOUR_SECRET_KEY"</span><span class="p"></span><span class="w">
</span><span class="p">}</span><span class="w">
</span></code></pre>
<p><strong>Parameters Request</strong></p>

<table><thead>
              <tr>
              <th>Parameters</th>
              <th>Value</th>
              <th>Description</th>
              </tr>
              </thead><tbody>
              <tr>
              <td>password</td>
              <td>YOUR_PASSWORD</code></td>
              <td>your password</td>
              </tr>
              <tr>
              <td>key</td>
              <td>SECRET_KEY</code></td>
              <td>your key</td>
              </tr>

              </tbody></table>


<blockquote>
<p>Check Balance Response</p>
</blockquote>
<pre class="highlight json"><code><span class="p">curl https://www.cavallocoin.io/api/new</span>
<span class="p">{</span><span class="w">
</span><span class="nt">"success"</span><span class="p">:</span><span class="w"> </span><span class="s2">"true"</span><span class="p">,</span><span class="w">
</span><span class="nt">"data"</span><span class="p">:</span><span class="p">{</span><br>
 <span class="nt">"message"</span><span class="p">:</span> <span class="s2">"Account created"</span><span>,</span><span class="w">
 </span>
 <span class="nt">"detail"</span><span class="p">:</span><span class="p">{</span>
 <br><span class="w"> </span>
 <span class="nt"> "wallet"</span><span class="p">:</span><span class="s2">"SYrOykTM6LEL3jhCxQEXrqXMO8lhVMicoYu9owGp46YLn8PaGVNOTB5ekz54pxPGk6VAgkX9cGiYR"</span>,
 <span class="nt"> "balance"</span><span class="p">:</span><span class="s2">"0"</span>,
 <span class="nt"> "secret_key"</span><span class="p">:</span><span class="s2">"645716fb88007616783d818c9b2a7d616fc97154932757357e3e79a70363c5ee673ffce2d4453fd3de8e817eb7aa86d9b79339e850aa35c26e387c427e183485"</span>,
 <span class="nt"> "id"</span><span class="p">:</span><span class="s2">"5ae825d8402c5a230812ea73"</span>,
 <span class="nt"> "token"</span><span class="p">:</span><span class="s2">"010fa85d20fa4e586254c9a386a57a9f2ce1937ae904d22f7865aa5f09aea7626de2b22897ada7f5e4843ecdee0135281733807686dd8b3bad7efeae4e3cabd3"</span><span class="w"></span><span class="p">}</span>
 <span class="p">}</span>
 <span class="p">}</span>
 <span class="w"></span></code></pre>

          

<h1 id="response-code">Response Code</h1>

<p>Response Code is a respond code that is given by cavallocoin.io system as status from every transaction request which is sent by member system (CA).</p>

<p>Based on the outline, the following are response code less:</p>

<table><thead>
<tr>
<th>Status Code</th>
<th>Description</th>
</tr>
</thead><tbody>

<tr>
<td>200</td>
<td>Your transaction has been success</td>
</tr>

<tr>
<td>200</td>
<td>Account created</td>
</tr>

<tr>
<td>500</td>
<td>Unauthenticated</td>
</tr>

<tr>
<td>500</td>
<td>The given data was invalid.</td>
</tr>

<tr>
<td>200</td>
<td>Something wrong.</td>
</tr>

<tr>
<td>405</td>
<td>method not allowed.</td>
</tr>

<tr>
<td>404</td>
<td>page not found.</td>
</tr>


</tbody></table>

<aside class="notice"><span class="glyphicon glyphicon-info-sign"></span>The list of code response can change along with the increase of
    product scope which is supported by cavallocoin.co.</aside>

      </div>
      <div class="dark-box">
          <div class="lang-selector">
                <a href="#" data-language-name="json">json</a>
          </div>
      </div>
    </div>
	</body>
</html>

