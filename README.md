<html>
<head>
    <!-- Load Lightning Out -->
    <script src="https://orgfarm-de8616b37d-dev-ed.develop.my.salesforce.com/lightning/lightning.out.js"></script>
    <script>
        // Initialize Lightning Out
        $Lightning.use(
            "c:externalApp", // Lightning Out App
            function() {

                // Create the Aura wrapper component dynamically
                $Lightning.createComponent(
                    "c:agentChatWrapper", // Aura wrapper of your LWC
                    {},                   // Attributes (empty)
                    "lightningContainer", // Div id on your page
                    function(cmp) {
                        console.log("Agent Chat loaded!");
                    }
                );

            },
            "https://orgfarm-de8616b37d-dev-ed.develop.my.salesforce.com" // Salesforce org base URL
        );
    </script>
</head>
<body>
    <div id="lightningContainer"></div>
</body>
</html>
