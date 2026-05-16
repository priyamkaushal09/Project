# Deployment Guide

## Frontend Deployment (Vercel)

### Prerequisites
- GitHub account connected to Vercel
- Vercel account

### Steps
1. Push code to GitHub
2. Go to [Vercel Dashboard](https://vercel.com/dashboard)
3. Click "New Project"
4. Select your GitHub repository
5. Configure:
   - Build Command: `npm run build`
   - Output Directory: `dist`
   - Environment Variables:
     - `VITE_API_URL`: Your backend URL

### Deploy
```bash
npm run build
vercel
```

---

## Backend Deployment (Render)

### Prerequisites
- GitHub repository
- Render account

### Steps
1. Go to [Render Dashboard](https://render.com/dashboard)
2. Click "New +" → "Web Service"
3. Connect GitHub repository
4. Configure:
   - Name: `ai-resume-analyzer-api`
   - Environment: `Python 3`
   - Build Command: `pip install -r requirements.txt`
   - Start Command: `gunicorn app:app`
   - Environment Variables:
     - `MONGODB_URI`: MongoDB Atlas connection string
     - `JWT_SECRET`: Your JWT secret
     - `FLASK_ENV`: `production`

### Deploy
Push to main branch - Render will auto-deploy.

---

## Database Setup (MongoDB Atlas)

### Steps
1. Go to [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
2. Create a cluster (Free tier available)
3. Create a database user
4. Get connection string
5. Add to backend `.env`:
   ```
   MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/dbname
   ```

---

## Environment Variables Checklist

### Frontend
- [ ] `VITE_API_URL`

### Backend
- [ ] `MONGODB_URI`
- [ ] `JWT_SECRET`
- [ ] `FLASK_ENV`
- [ ] `CORS_ORIGINS` (for development)

---

## Post-Deployment

1. Test all endpoints with production URL
2. Monitor logs on Render dashboard
3. Set up error tracking (optional: Sentry)
4. Configure custom domain (optional)
5. Enable HTTPS (automatic on Vercel/Render)

---

## Troubleshooting

**CORS Errors:** Update `CORS_ORIGINS` in backend
**MongoDB Connection:** Verify IP whitelist in Atlas
**Build Failures:** Check logs in Vercel/Render dashboards
**JWT Issues:** Ensure `JWT_SECRET` matches between environments
