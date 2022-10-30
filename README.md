# AB Testing
Personal a/b, a/b/n... study repo.

<hr>

<h2>Summary</h2>
<hr>

- [0. Business Cases](#0-business-cases)
  - [0.1. Eletronic House Company](#01-eletronic-house-company)
    - [0.1.1. Conversion Rate Lift](#011-conversion-rate-lift)
    - [0.1.2. Mean Price Lift](#012-mean-price-lift)
  - [0.2. AB Test Key Facts On Ecommerce](#02-ab-test-key-facts-on-ecommerce)
- [1. Solution Strategy and Assumptions](#1-solution-strategy-and-assumptions)
  - [1.1. Conversion Rate Lift First CRISP Cycle](#11-conversion-rate-lift-first-crisp-cycle)
  - [1.2. Mean Price Lift First CRISP Cycle](#12-mean-price-lift-first-crisp-cycle)
- [2. AB Test Key Facts](#2-ab-test-key-facts)
  - [2.1. The Effect Size](#21-the-effect-size)
  - [2.2. The Sample Size](#22-the-sample-size)
  - [2.3. The Statistical Inference](#23-the-statistical-inference)
- [3. References](#3-references)

---

<h2>0. Business Cases</h2>
<hr>

<h3>0.1. Eletronic House Company</h3>
<p>The electronic house company is an online commerce (e-commerce) that sells various computer products for homes and offices. Customers can purchase from smaller equipment such as mice, headphones and hdmi cables to computers and laptops through the company's website, after purchase the products arrive in the comfort of their homes.</p>

<h4>0.1.1. Conversion Rate Lift</h4>
<p>The ux designers team has been working on a new sales page with the objective of increasing the sales rate of a product in the store, this product is the bluetooth keyboard. The product manager said that the average page conversion rate is 13% and he expects a 2% increase in conversion from the new page being developed.</p>
<p>The bluetooth keyboard can be purchased for 4,500 in cash or 12 interest-free installments on your credit card.</p>
<p>But before actually changing the page when it is developed, the product manager would like to test the effectiveness of the page on a smaller group of customers in order to avoid possible drops in conversion or whatever other problems the page may have in production.</p>
<p>Before the new page goes into production, it will be tested on a smaller group of customers in order to avoid risks such as a drop in conversion and others, but it will be possible for this smaller group to calculate the potential and expected revenue rates of this new page!</p>

<h5>0.1.1.1. Metric Definition</h5>
<p>For this problem, the success metric is "conversion rate", based on status quo conversion (12%) the P.M. expects a new conversion based on ux designers team new page. The expected new conversion is 15% ([13% status quo] + [2% of new page]) for bluetooth keyboard.</p>
<p>The word conversion has several meanings, for this specific problem it is precisely the purchase, "the purchase of the bluetooth keyboard".</p>

<h4>0.1.2. Mean Price Lift</h4>
<p>For this problem, the success metric is the "price" or "number of itens purchases" not a proportion (0.15% -> 0.03% Lift), is a absolute number, (100 is the price sales mean for page A). The expected new price sales mean is 110 (status_quo * 1.10). Same problesm but with other expected metric for A/B Testing.</p>

<h3>0.2. AB Test Key Facts On Ecommerce</h3>
<p>Why AB Testing ?</p>
<p>You do a/b tests in order to improve a business metric for example a click conversion rate (CTR), sales, views or others. To improve these metrics, several techniques are developed, in the world of ux and design, the creation of new pages, color changes or other factors that influence the click, purchase or other metric that you are trying to improve with the elaboration of the new page.</p>

<p>Top 5 E-commerce metrics:</p>

<ul>
  <li>CTR / Click Through Rate. Total of new customers per button click or similar.</li>
  <li>CVR / Sales Conversion Rate. Total of new customers per successful sale.</li>
  <li>CLF / Customer Lifetime Value. Total revenue acquired by a customer.</li>
  <li>CAC / Customer Aquisition Cost. Price for aquisition of each client.</li>
  <li>CAR / Cart Abandoned Rate. Why are customers abandoning carts??</li>
</ul>

<h2>1. Solution Strategy and Assumptions</h2>
<hr>

<p>For this problem, one way to solve is using ab test or other ab test approaches like multi armed bandits.</p>

<h3>1.1. Conversion Rate Lift First CRISP Cycle</h3>
<p>If do not have Data, its necessary to perform a Experiment Design step to infer number of samples and tools to segment the population into two groups called control and treatment. In this case, the samples were previously collected.</p>

<ul>
  <dl>
    <dt>Descriptive Statistical.</dt>
      <dd>This is the first step after you get the dataset, in this step you make simple cleanings like removing duplicates rows, erros on public segmentation and others cleanings, and see some statistical status when possible.</p>
    <dt>Exploratory Data Analysis.</dt>
      <dd>In this step you make some analysis on data and metric observed on the public segmentation experiment, the analyzes in this case are the visualization of the obtained distributions and some validations of homogeneity.</dt>
    <dt>Experiment Design.</dt>
      <dd>Focus on previos hypothesis definition validation, setup the parameters of test, re-sample if necessary, compute explcit metrics, select and apply inference statistical test and translate results to money!.</dd>
  </dl>
</ul>

<p></p>

<h3>1.2. Mean Price Lift First CRISP Cycle</h3>
<p>If do not have Data, its necessary to perform a Experiment Design step to infer number of samples and tools to segment the population into two groups called control and treatment. In this case, the samples were previously collected.</p>
<p>Same steps of proportion test</p>

<ul>
  <dl>
    <dt>Descriptive Statistical.</dt>
      <dd>This is the first step after you get the dataset, in this step you make simple cleanings like removing duplicates rows, erros on public segmentation and others cleanings, and see some statistical status when possible.</p>
    <dt>Exploratory Data Analysis.</dt>
      <dd>In this step you make some analysis on data and metric observed on the public segmentation experiment, the analyzes in this case are the visualization of the obtained distributions and some validations of homogeneity.</dt>
    <dt>Experiment Design.</dt>
      <dd>Focus on previos hypothesis definition validation, setup the parameters of test, re-sample if necessary, compute explcit metrics, select and apply inference statistical test and translate results to money!.</dd>
  </dl>
</ul>


<h2>2. AB Test Key Facts</h2>
<hr>

<p></p>

<h3>2.1. The Effect Size</h3>
<p>The effect size is nothing more than a result based on how big the expected effect is. In other words, the power of a statistical test is the probability that it will produce statistically significant results.</p>

- The effect size defines the size of the sample to be collected in both groups to start the segmentation of control and treatment.
- Small differences require more data, larger differences require less data.

<p>There are two distributions, the normal distribution already measured (status quo) and the distribution observed after collecting and preparing these data. If the expected observation is small, then both distributions will be close and more data will be needed because there is a lot of uncertainty (overlapping), whereas when the observation is very large, little data is needed because both distributions will be well separated.</p>

<h3>2.2. The Sample Size</h3>
</p>The sample size or $n$ is the function of $effect~size$, $a$ and $power$. In this example, when the investigator anticipates a certain effect size or calculates it including the alpha and power of the test, with these three parameters it is possible to calculate the minimum size of a sample for the appropriate statistical inferences.</p>

<p>Based on cohen's book, there are tables for certain sample sizes based on the type of test, for example the chi square test there are tables for the sample size of the type (contingency test and fit test) for various definitions of alpha, effect size and power.</p>

<p>Some of the formulas and definitions is implemented on pythons library called "statsmodels", but, for Anova test, it's gives "wrongs" samples sizes, need to checkout on future ;-;</p>

<h3>2.3. The Statistical Inference</h3>
<p>"Statistical inference is the process of using a sample to infer the properties of a population. Statistical procedures use sample data to estimate the characteristics of the whole population from which the sample was drawn." ~ Jim</p>

<p>By using procedures that can make statistical inferences, you can estimate the properties and processes of a population. More specifically, sample statistics can estimate population parameters.</p>

<h2>3. References</h2>
<hr>

<p></p>

<ul>
  <li><a href="https://www.shopify.com/blog/basic-ecommerce-metrics">Basic Ecommerce Metrics.</a></li>
  <li><a href="https://statisticsbyjim.com/hypothesis-testing/statistical-inference/">Statisticsbyjim.</a></li>
</ul>
