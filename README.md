// api/token.js
import { StreamChat } from 'stream-chat';

export default async function handler(req, res) {
  if (req.method !== 'POST') {
    return res.status(405).json({ error: 'Method not allowed' });
  }

  const API_KEY = process.env.STREAM_API_KEY;
  const API_SECRET = process.env.STREAM_API_SECRET;

  if (!API_KEY || !API_SECRET) {
    return res.status(500).json({ error: 'Missing Stream credentials' });
  }

  try {
    const serverClient = StreamChat.getInstance(API_KEY, API_SECRET);
    const token = serverClient.createToken(undefined, { server: true });
    return res.status(200).json({ token });
  } catch (e) {
    return res.status(500).json({ error: e.message });
  }
}
