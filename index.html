import { useState, useEffect } from 'react';
import io from 'socket.io-client';

const socket = io('https://your-replit-backend-url.com');

export default function Chat() {
  const [messages, setMessages] = useState([]);
  const [message, setMessage] = useState('');
  const [username, setUsername] = useState('');

  useEffect(() => {
    socket.on('connect', () => {
      setUsername(prompt('Enter your username:'));
      socket.emit('join', username);
    });

    socket.on('message', (msg) => {
      setMessages(prev => [...prev, msg]);
    });

    socket.on('user joined', (user) => {
      setMessages(prev => [...prev, { text: `${user} joined the chat!`, isSystem: true }]);
    });
  }, []);

  const handleSubmit = (e) => {
    e.preventDefault();
    if (message.trim()) {
      socket.emit('message', message);
      setMessage('');
    }
  };

  return (
    <div style={{ padding: '20px' }}>
      <h1>Chat Room</h1>
      <div style={{ height: '400px', border: '1px solid #ccc', padding: '10px', overflowY: 'auto' }}>
        {messages.map((msg, i) => (
          <div key={i} style={{ margin: '5px 0' }}>
            {msg.isSystem ? (
              <em>{msg.text}</em>
            ) : (
              <span>{msg.username}: {msg.text}</span>
            )}
          </div>
        ))}
      </div>
      <form onSubmit={handleSubmit} style={{ marginTop: '10px' }}>
        <input
          type="text"
          value={message}
          onChange={(e) => setMessage(e.target.value)}
          placeholder="Type a message..."
          style={{ padding: '5px', width: '200px' }}
        />
        <button type="submit" style={{ marginLeft: '5px', padding: '5px 10px' }}>
          Send
        </button>
      </form>
    </div>
  );
}
