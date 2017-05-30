// Returning an authentication error if a user who is not logged in tries to query the REST API
add_filter( 'rest_authentication_errors', function( $access ) {
   if( ! is_user_logged_in() ) {
      return new WP_Error( 'rest_API_cannot_access', __( 'Only authenticated users can access the REST API.', 'disable-json-api' ), array( 'status' => rest_authorization_required_code() ) );
   }
return $access; 
});