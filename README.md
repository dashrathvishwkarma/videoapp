    @app.route('/webhook', 
    def webhook_receiver():
        # Process the incoming webhook data
        try:
            data = request.json  # Assumes the incoming data is JSON
            print(f"Received webhook data: {data}")

            # Add your custom logic here to process the data
            # For example, save to a database, trigger another action, etc.

            return jsonify({"message": "Webhook received successfully!"}), 200
        except Exception as e:
            print(f"Error processing webhook: {e}")
            return jsonify({"message": "Error processing webhook"}), 500
