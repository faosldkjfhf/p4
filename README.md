        # self.sequence = 0
        # self.ack_received = 0
        # self.window_size = 2

    # def can_send(self):
        # return self.sequence - self.ack_received < self.window_size

    # def handle_ack(self):
        # data, _ = self.socket.recvfrom(1024)
        # ack_msg = json.loads(data.decode('utf-8'))

        # if ack_msg["type"] == "ack":
        # self.ack_recieved = max(self.ack_received, ack_msg["sequence"])
