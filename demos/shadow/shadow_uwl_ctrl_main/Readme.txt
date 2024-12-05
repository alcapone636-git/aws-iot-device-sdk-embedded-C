Currently the software does not run very well.

If the following variables from the file 'shadow_uwl_ctrl_main.c' are configured like the following then software runs successfully with no errors on the terminal.
Neverhteless, it can be seen that SHADOW_DESIRED_JSON was not initiated correctly as it says 'reported' instead 'desired' in the JSON file:

#define SHADOW_DESIRED_JSON           \
    "{"                               \
    "\"state\":{"                     \
    "\"reported\":{"                  \
    "\"powerOn\":%01d,"               \
    "\"PoolLight\":%.2f,"             \
    "\"SpaLight\":%.2f"               \
    "}"                               \
    "},"                              \
    "\"clientToken\":\"%06lu\""       \
    "}"

#define SHADOW_DESIRED_JSON_LENGTH    ( sizeof( SHADOW_DESIRED_JSON ) + 3 )

#define SHADOW_REPORTED_JSON_LENGTH    ( sizeof( SHADOW_REPORTED_JSON ) + 3 )



