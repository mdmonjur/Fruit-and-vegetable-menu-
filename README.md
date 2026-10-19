# MR MONJUR Retailer Admin Package

Contains a Super Admin account-provisioning page, Supabase multi-tenant schema foundation, and Edge Function to create retailer-admin credentials. The previous management HTML is included as a preserved copy.

**Not yet a complete replacement for the legacy management app.** The legacy HTML still uses a single shared `hr_shared_data` row. Do not let multiple retailers use that legacy cloud data until its modules have been migrated to tenant-scoped tables and verified with RLS. See `বাংলা-নির্দেশনা.txt`.
