🎯 Purpose
What It Does	Why
Prevents approved from coexisting with denied or needs-info	Ensures an issue has a single, clear status
Blocks adding denied or needs-info when approved is present	Protects the approval workflow from being overridden
Allows denied and needs-info to coexist	They are not mutually exclusive
📋 Behavior Matrix
Label Added	If approved is present	If approved is NOT present
approved	✅ denied and needs-info are removed	✅ approved added
denied	❌ denied is removed (blocked)	✅ denied added
needs-info	❌ needs-info is removed (blocked)	✅ needs-info added
