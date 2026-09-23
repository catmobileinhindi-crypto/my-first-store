# Nova Store — E-Commerce Demo

Ek self-contained e-commerce demo: customer storefront + admin dashboard, sab ek hi `index.html` file mein. Data browser ke localStorage mein save hota hai (per-visitor, koi shared database nahi).

## Admin Access
- URL ke end mein `#/admin` likho (jaise: `https://yoursite.vercel.app/#/admin`)
- Username: `admin`
- Password: `demo123`

⚠️ Ye demo-level login hai (password JS code mein hai) — sirf demo/testing ke liye, real business ke liye backend authentication chahiye.

---

## Vercel pe Deploy Karne Ka Tareeqa

### Option A — Vercel Dashboard se (sabse asaan, no coding)
1. [vercel.com](https://vercel.com) pe account banao/login karo
2. Dashboard mein **"Add New" → "Project"** click karo
3. **"Deploy without Git"** / drag-drop option choose karo (ya "Import" screen ke neeche option milega)
4. Ye poora folder (`index.html`, `vercel.json`) drag-and-drop karo
5. **Deploy** dabao — 30 second mein live link mil jayega

### Option B — Vercel CLI se
```bash
npm install -g vercel
cd nova-store
vercel
```
Terminal mein sawalat aayenge (project name, etc.) — sab default rakh sakte ho. Deploy hote hi live URL milega.

### Option C — GitHub ke zariye (best for updates)
1. Ye folder GitHub repo mein push karo
2. Vercel dashboard mein **"Import Git Repository"** se us repo ko connect karo
3. Har baar jab GitHub pe code update karo, Vercel automatically re-deploy kar dega

---

## Important Notes
- Ye static HTML site hai — koi build step nahi chahiye (Framework Preset: "Other" select karna, agar Vercel poochay)
- Data (products/orders/customers) sirf **us browser** mein save hota hai jo site kholta hai — har visitor ka apna alag data hoga, kisi ke sath share nahi hota
- Real production store ke liye aap ko ek asal backend + database (jaise Node.js + PostgreSQL, ya Supabase/Firebase) chahiye hoga jahan sab orders ek jagah central store hon
