<p>The <em><a href="https://bluerobotics.com/store/sensors-sonars-cameras/sensors/bar30-sensor-r1/">Bar30</a></em> pressure sensor is a pressure sensor designed to be used underwater at pressures up to 30 bar, or around 300 meters depth in water. It communicates via I<sup>2</sup>C and comes with a 4-pin DF-13 connector that is compatible with the <a href="https://bluerobotics.com/store/comm-control-power/elec-packages/pixhawk-r1-rp/">Pixhawk</a> autopilot, the <em><a href="https://bluerobotics.com/store/sensors-sonars-cameras/sensors/level-converter-r1/">Level Converter</a></em> and other microcontrollers.</p>

<div class="woocommerce columns-1 guide-product-featured"><ul class="products columns-1">
<li class="post-5016 product type-product status-publish has-post-thumbnail product_cat-sensors first instock taxable shipping-taxable purchasable product-type-simple">
	<a href="https://www.bluerobotics.com/store/sensors-sonars-cameras/sensors/bar30-sensor-r1/" class="woocommerce-LoopProduct-link woocommerce-loop-product__link"><img width="300" height="300" src="https://www.bluerobotics.com/wp-content/uploads/2016/01/IMG_0965-300x300.jpg?x26453" class="attachment-woocommerce_thumbnail size-woocommerce_thumbnail" alt="" srcset="https://www.bluerobotics.com/wp-content/uploads/2016/01/IMG_0965-300x300.jpg 300w, https://www.bluerobotics.com/wp-content/uploads/2016/01/IMG_0965-150x150.jpg 150w, https://www.bluerobotics.com/wp-content/uploads/2016/01/IMG_0965-768x768.jpg 768w, https://www.bluerobotics.com/wp-content/uploads/2016/01/IMG_0965-1024x1024.jpg 1024w, https://www.bluerobotics.com/wp-content/uploads/2016/01/IMG_0965-64x64.jpg 64w, https://www.bluerobotics.com/wp-content/uploads/2016/01/IMG_0965-900x900.jpg 900w, https://www.bluerobotics.com/wp-content/uploads/2016/01/IMG_0965-100x100.jpg 100w" sizes="(max-width: 300px) 100vw, 300px" pagespeed_url_hash="505925041" onload="pagespeed.CriticalImages.checkImageForCriticality(this);"/><h2 class="woocommerce-loop-product__title">Bar30 High-Resolution 300m Depth/Pressure Sensor</h2>
           
      

</div>

<p>Using a <em>Bar30</em> with most Arduino (including the Uno, Mega, Micro and Nano) and other 5v microcontrollers requires an I2C logic level converter to communicate with a 3.3v device such as the Bar30. Note that some Arduino and other microcontrollers which run at 3.3v (including Raspberry Pis and the Pixhawk autopilot) do not require a logic level converter. Always make sure to check what voltage your microcontroller or computer uses before wiring up a sensor.</p>

<p>Note that the voltages being discussed here are the logic voltage levels, that is, what the I<sup>2</sup>C pins will be experiencing. This is typically the same voltage at which the device runs, but not necessarily the voltage of the input power supply. The Bar30 has a built-in 3.3v converter for power, so it can accept power anywhere from 3.3v to 5.5v. The <em>Level Converter</em> can also be used to supply 3.3v power from a 5v source: in this tutorial it is assumed that your <em>Level Converter</em> is set up to provide either 3.3v or 5v to the sensor. It is also assumed that both sets of header pins have been soldered to the Level Converter. See the <em>Level Converter</em>’s <a href="https://www.bluerobotics.com/store/electronics/level-converter-r1/#tab-learn">store page</a> for details.</p>

<div class="alert alert-danger"><div class="row"><div class="col-sm-1"><i class="fa fa-exclamation-triangle fa-fw fa-3x text-warning"></i></div><div class="col-sm-11"><p>Most 3.3v devices do not tolerate higher voltages, so directly connecting the pins on an Arduino Uno to a such a device may fry your device. Some 3.3v devices are 5v-tolerant, meaning they will still function after being connected to 5v logic, but they will not necessarily be able to communicate with a microcontroller with 5v logic.</p></div></div></div>

<h1 class="anchor-heading" id="parts-and-tools">Parts and Tools <a href="#parts-and-tools" class="anchor"><i class="fa fa-link" aria-hidden="true"></i>
	</a></h1>

<div class="guide-image-wrapper"><a href="https://www.bluerobotics.com/wp-content/uploads/2019/01/parts-list.jpg?x26453" rel="lightbox[67899]" title="All of the components used in this guide."><img src="https://www.bluerobotics.com/wp-content/uploads/2019/01/parts-list-1024x653.jpg?x26453" alt="All of the components used in this guide." class="img-responsive img-center no-lazy-load img-guide" pagespeed_url_hash="3526976370" onload="pagespeed.CriticalImages.checkImageForCriticality(this);"/></a><p class="guide-image-caption text-center">All of the components used in this guide.</p></div>

<h2 class="anchor-heading" id="you-will-need">You Will Need <a href="#you-will-need" class="anchor"><i class="fa fa-link" aria-hidden="true"></i>
	</a></h2>

<div class="woocommerce columns-4 guide-product"><ul class="products columns-4">
<li class="post-5016 product type-product status-publish has-post-thumbnail product_cat-sensors first instock taxable shipping-taxable purchasable product-type-simple">
	<a href="https://www.bluerobotics.com/store/sensors-sonars-cameras/sensors/bar30-sensor-r1/" class="woocommerce-LoopProduct-link woocommerce-loop-product__link"><img width="300" height="300" src="https://www.bluerobotics.com/wp-content/uploads/2016/01/IMG_0965-300x300.jpg?x26453" class="attachment-woocommerce_thumbnail size-woocommerce_thumbnail" alt="" srcset="https://www.bluerobotics.com/wp-content/uploads/2016/01/IMG_0965-300x300.jpg 300w, https://www.bluerobotics.com/wp-content/uploads/2016/01/IMG_0965-150x150.jpg 150w, https://www.bluerobotics.com/wp-content/uploads/2016/01/IMG_0965-768x768.jpg 768w, https://www.bluerobotics.com/wp-content/uploads/2016/01/IMG_0965-1024x1024.jpg 1024w, https://www.bluerobotics.com/wp-content/uploads/2016/01/IMG_0965-64x64.jpg 64w, https://www.bluerobotics.com/wp-content/uploads/2016/01/IMG_0965-900x900.jpg 900w, https://www.bluerobotics.com/wp-content/uploads/2016/01/IMG_0965-100x100.jpg 100w" sizes="(max-width: 300px) 100vw, 300px" pagespeed_url_hash="505925041" onload="pagespeed.CriticalImages.checkImageForCriticality(this);"/><h2 class="woocommerce-loop-product__title">Bar30 High-Resolution 300m Depth/Pressure Sensor</h2>
	<span class="price"><span class="woocommerce-Price-amount amount"><span class="woocommerce-Price-currencySymbol">&#36;</span>68.00</span></span>
</a><a href="/learn/bar30-arduino-guide/?add-to-cart=5016" data-quantity="1" class="button product_type_simple add_to_cart_button ajax_add_to_cart" data-product_id="5016" data-product_sku="BAR30-SENSOR-R1-RP" aria-label="Add &ldquo;Bar30 High-Resolution 300m Depth/Pressure Sensor&rdquo; to your cart" rel="nofollow">Add to Cart</a>            
            </li>
<li class="post-11611 product type-product status-publish has-post-thumbnail product_cat-sensors product_cat-tether-interface instock taxable shipping-taxable purchasable product-type-simple">
	<a href="https://www.bluerobotics.com/store/sensors-sonars-cameras/sensors/level-converter-r1/" class="woocommerce-LoopProduct-link woocommerce-loop-product__link"><img width="300" height="300" src="https://www.bluerobotics.com/wp-content/uploads/2016/11/level-converter-1-300x300.png?x26453" class="attachment-woocommerce_thumbnail size-woocommerce_thumbnail" alt="" srcset="https://www.bluerobotics.com/wp-content/uploads/2016/11/level-converter-1-300x300.png 300w, https://www.bluerobotics.com/wp-content/uploads/2016/11/level-converter-1-150x150.png 150w, https://www.bluerobotics.com/wp-content/uploads/2016/11/level-converter-1-768x768.png 768w, https://www.bluerobotics.com/wp-content/uploads/2016/11/level-converter-1-1024x1024.png 1024w, https://www.bluerobotics.com/wp-content/uploads/2016/11/level-converter-1-64x64.png 64w, https://www.bluerobotics.com/wp-content/uploads/2016/11/level-converter-1-900x900.png 900w, https://www.bluerobotics.com/wp-content/uploads/2016/11/level-converter-1-100x100.png 100w" sizes="(max-width: 300px) 100vw, 300px" pagespeed_url_hash="3778218343" onload="pagespeed.CriticalImages.checkImageForCriticality(this);"/><h2 class="woocommerce-loop-product__title">I2C Level Converter</h2>
	<span class="price"><span class="woocommerce-Price-amount amount"><span class="woocommerce-Price-currencySymbol">&#36;</span>14.00</span></span>
</a><a href="/learn/bar30-arduino-guide/?add-to-cart=11611" data-quantity="1" class="button product_type_simple add_to_cart_button ajax_add_to_cart" data-product_id="11611" data-product_sku="LEVELCONVERTER-R1-RP" aria-label="Add &ldquo;I2C Level Converter&rdquo; to your cart" rel="nofollow">Add to Cart</a>            
            </li>
</ul>
</div>

<p>You will also need:</p>

<ul>
	<li>1 x Arduino microcontroller (This tutorial uses an Arduino Uno)</li>
	<li>4 x Breadboard Jumpers: M/F</li>
        <li>1 x USB A to B cable (for connecting to your Arduino board)</li>
</ul>

<h1 class="anchor-heading" id="wire-connections">Wire Connections <a href="#wire-connections" class="anchor"><i class="fa fa-link" aria-hidden="true"></i>
	</a></h1>

<p>Connect the <em>Bar30</em> to the <em>Level Converter</em> using the DF-13 connector.</p>

<p>If your <em>Level Converter</em> does not have the header pins soldered on as shown, you will need to solder them on yourself for the following step. Please see the <em>Level Converter</em>’s store page for details.</p>

<div class="guide-image-wrapper"><a href="https://www.bluerobotics.com/wp-content/uploads/2019/01/level-converter-df-13.jpg?x26453" rel="lightbox[67899]" title="level-converter-df-13"><img src="https://www.bluerobotics.com/wp-content/uploads/2019/01/level-converter-df-13-1024x677.jpg?x26453" alt="level-converter-df-13" class="img-responsive img-center no-lazy-load img-guide" pagespeed_url_hash="2089368342" onload="pagespeed.CriticalImages.checkImageForCriticality(this);"/></a></div>

<p>Connect the +5V, SDA, SCL, and GND pins on the Level Converter to the 5V, SDA, SCL, and GND pins on the Arduino using four jumper wires. Make sure you are connecting to the Level Converter pins on the far side from the DF-13 connector. See the table below for the pin assignments for SDA and SCL on a few common Arduino boards.</p>

[table &#8220;guide_bar30_arduino_pin&#8221; not found /]<br/>


<p> Make sure the <em>Level Converter&#8217;s</em> +5V pin is connected to the Arduino&#8217;s 5V pin and <em>not</em> the 3.3V pin.  Although the <em>Bar30</em> is a 3.3 V device which can be powered at either 3.3 V or 5 V, the <em>Level Converter</em> is a 5 V device and as such requires a 5 V supply. </p>

<div class="guide-image-wrapper"><a href="https://www.bluerobotics.com/wp-content/uploads/2019/01/level-converter-jumper-pins.jpg?x26453" rel="lightbox[67899]" title="Jumper wire connections on the <em>Level Converter</em> board."><img src="https://www.bluerobotics.com/wp-content/uploads/2019/01/level-converter-jumper-pins-1024x708.jpg?x26453" alt="Jumper wire connections on the <em>Level Converter</em> board." class="img-responsive img-center no-lazy-load img-guide" pagespeed_url_hash="2033792328" onload="pagespeed.CriticalImages.checkImageForCriticality(this);"/></a><p class="guide-image-caption text-center">Jumper wire connections on the <em>Level Converter</em> board.</p></div>
</br>
<div class="guide-image-wrapper"><a href="https://www.bluerobotics.com/wp-content/uploads/2019/01/arduino-jumper-pins.jpg?x26453" rel="lightbox[67899]" title="Jumper wire connections on the Arduino."><img src="https://www.bluerobotics.com/wp-content/uploads/2019/01/arduino-jumper-pins-1024x635.jpg?x26453" alt="Jumper wire connections on the Arduino." class="img-responsive img-center no-lazy-load img-guide" pagespeed_url_hash="3023407736" onload="pagespeed.CriticalImages.checkImageForCriticality(this);"/></a><p class="guide-image-caption text-center">Jumper wire connections on the Arduino.</p></div>

<h1 class="anchor-heading" id="arduino-library-installation">Arduino Library Installation <a href="#arduino-library-installation" class="anchor"><i class="fa fa-link" aria-hidden="true"></i>
	</a></h1>

<p>Download the BlueRobotics MS5837 Library</p>
<ul>
	<li>via Library Manager (Sketch&#8211;&gt;Include Library&#8211;&gt;Manage Libraries):</li>
	<li>open the Library Manager and search for &#8220;BlueRobotics MS5837&#8221;</li>
<div class="guide-image-wrapper"><a href="https://www.bluerobotics.com/wp-content/uploads/2019/01/library-manager-br-library.png?x26453" rel="lightbox[67899]" title="library-manager-br-library"><img src="https://www.bluerobotics.com/wp-content/uploads/2019/01/library-manager-br-library.png?x26453" alt="library-manager-br-library" class="img-responsive img-center no-lazy-load img-guide" pagespeed_url_hash="3095080607" onload="pagespeed.CriticalImages.checkImageForCriticality(this);"/></a></div>
        <li>click &#8220;Install&#8221;</li></ul>
via GitHub:
<ul>&#8211; download the library in zip format from: https://github.com/bluerobotics/BlueRobotics_MS5837_Library</ul>
<ul>&#8211; unzip the library and place the folder in your Arduino/libraries folder</ul>

<h1 class="anchor-heading" id="uploading-example-sketch">Uploading Example Sketch <a href="#uploading-example-sketch" class="anchor"><i class="fa fa-link" aria-hidden="true"></i>
	</a></h1>

<p>Open the example code.  You may need to restart the Arduino IDE to see it.</p>
<div class="guide-image-wrapper"><a href="https://www.bluerobotics.com/wp-content/uploads/2019/01/examples-list.png?x26453" rel="lightbox[67899]" title="examples-list"><img src="https://www.bluerobotics.com/wp-content/uploads/2019/01/examples-list.png?x26453" alt="examples-list" class="img-responsive img-center no-lazy-load img-guide" pagespeed_url_hash="651971" onload="pagespeed.CriticalImages.checkImageForCriticality(this);"/></a></div>
<p>Upload your code to the Arduino.</p>
<p>Open the Serial Monitor, making sure the Baud rate is set to 9600.</p>
<div class="guide-image-wrapper"><a href="https://www.bluerobotics.com/wp-content/uploads/2019/01/serial-output.png?x26453" rel="lightbox[67899]" title="serial-output"><img src="https://www.bluerobotics.com/wp-content/uploads/2019/01/serial-output.png?x26453" alt="serial-output" class="img-responsive img-center no-lazy-load img-guide" pagespeed_url_hash="883246887" onload="pagespeed.CriticalImages.checkImageForCriticality(this);"/></a></div>
<p>That&#8217;s it!  You should see pressure, depth, and temperature data being printed to the Serial Monitor.  If not, check the Troubleshooting section below.</p>

<h1 class="anchor-heading" id="troubleshooting">Troubleshooting <a href="#troubleshooting" class="anchor"><i class="fa fa-link" aria-hidden="true"></i>
	</a></h1>

<h2>I can’t communicate with my Bar30</h2>
<ul>
	<li>Make sure the Bar30 is receiving power. Check the Level Converter’s voltage selection jumper pads. Either 3.3 V or 5 V will work (5 V is recommended). See the Level Converter’s store page for details.</li>

	<li>Check your SCL and SDA connections. Try swapping the two jumpers: reversing them will not damage the sensor or microcontroller.</li>

	<li>Check your jumpers for continuity. Some cheap jumper cables have terrible electrical connections.</li>
</ul>


<h2>The values I’m seeing are way off</h2>

<ul>
	<li>Make sure you are using the correct model sensor in your code. Code interfacing with a Bar30 should contain the following line for sensor initialization:
<code>sensor.setModel(MS5837::MS5837_30BA);</code></li>

	<li>If your code sets the model as <code>MS5837::MS5837_02BA</code>, the library will assume it is communicating with a Bar02 pressure sensor and will incorrectly interpret the incoming pressure data, resulting in absurd pressure and depth “measurements”.</li>
</ul>

      	
