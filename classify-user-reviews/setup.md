Before we start, we have to set up our training environment.

Execute the following command to install some utility functions and load some sample data:

` cd /
git clone https://github.com/rapyd-ai/use-cases.git
pip install requests
`{{execute}}

Let's launch Python which will help us with some data preparation:

` python`{{execute}}

In Python, we add our utility functions by executing the following code:

`import sys
sys.path.append('/use-cases/classify-user-reviews/utils')
from rapyd_ai_utils import *`{{execute}} 

We're now all set and ready to load our data.