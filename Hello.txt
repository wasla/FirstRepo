<?php
try{
    echo 'Begin van de try<br/>';
    $a = 12 ; //test ook de waarden 1, 12.2, 'test'
    $fac =1;
if (is_integer($a)){
    if ($a >0){
        for ($i =1; $i< $a; $i++ ){
            $fac *= $i;
        }
    }else{
        if ($a == 0){
            $fac =1;
        } else {
            throw new Exception("fout: $a < 0");
        }
    }
} else {
    throw new Exception("fout: $a is geen getal");
}
echo "<br/>$a! = $fac<br/>";
echo 'Einde van de try<br/>';
} catch (Exception $e){
    echo '<pre>'; var_dump ($e); echo '</pre>';
}
