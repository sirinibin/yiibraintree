<h2>yiibraintree</h2>

Yiibraintree is a Yii framework extension for Simplifying Integration of Braintree payment Solution into your ecommerce apps.

<h3>Requirements</h3>

Yii 1.1 or above Installation

<pre>
step1:Extract the file into your components directory step2:Update your components section in config/main.php eg:

'braintree' => array(
                                     'class'=>'application.components.braintree.YiiBraintree',
 
                                      'ENV' => 'sandbox',//sandbox or production
 
                                      'MERCHANT_ID' => 'merchant id here',
 
                                      'MERCHANT_ACCOUNT_ID'=>'Merchant account id here',
 
                                      'PUBLIC_KEY' => 'public key here',
 
                                      'PRIVATE_KEY'=>'private key here',
 
                                      'CSEK'=>'your CSEK here'
 
 
                                      ),
</pre>                                      
 

<h3>Usage</h3>

<pre>
$data=array(
                'amount' => '10.50',
                'merchantAccountId' => Yii::app()->braintree->MERCHANT_ACCOUNT_ID,
                'creditCard' => array(
                          'number' => '5105105105105100',
                          'expirationMonth' => '05',
                          'expirationYear' => '12'
                             )
               );
   $r=Yii::app()->braintree->sale($data);
</pre>   
