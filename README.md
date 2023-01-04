## Setup and run a RabbitMQ server
# Before installing make sure the taps are up-to-date:

brew update

brew install rabbitmq

brew info rabbitmq

# To start a node in the foreground: (recommended)
CONF_ENV_FILE="/opt/homebrew/etc/rabbitmq/rabbitmq-env.conf" /opt/homebrew/opt/rabbitmq/sbin/rabbitmq-server

# To start a node in the background:
brew services start rabbitmq

# Stopping the Server
brew services stop rabbitmq

or CLI tools directly:
/opt/homebrew/opt/rabbitmq/sbin/rabbitmqctl shutdown

# Show Listing queues:
sudo rabbitmqctl list_queues

# Run Consumer
node ./receive.js

# Run Publisher
node ./send.js


