# Mark-Comments-with-Very-Long-URLs-as-Spam




<?php
 
  function rkv_url_spamcheck( $approved , $commentdata ) {
    return ( strlen( $commentdata['comment_author_url'] ) > 50 ) ? 'spam' : $approved;
  }
 
  add_filter( 'pre_comment_approved', 'rkv_url_spamcheck', 99, 2 );
 
?>
