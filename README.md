- 👋 Hi, I’m @noyancafe
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
noyancafe/noyancafe is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import streamlit as st
import pandas as pd
from PIL import Image

st.set_page_config(page_title="Hoghoogh App", layout="wide")

st.title("🛠️ Hoghoogh App")
st.markdown("ثبت آگهی‌های کاری برای کارگران ساختمانی")

with st.form("worker_form"):
    name = st.text_input("نام کارگر")
    skill = st.text_input("مهارت")
    wage = st.number_input("حقوق پیشنهادی (تومان)", min_value=0)
    location = st.text_input("موقعیت مکانی")
    image_file = st.file_uploader("آپلود عکس", type=["jpg", "png", "jpeg"])
    submitted = st.form_submit_button("ثبت آگهی")

    if submitted:
        st.success(f"آگهی برای {name} با مهارت {skill} ثبت شد.")

st.markdown("---")
st.header("📋 لیست آگهی‌ها")
st.info("در نسخه اولیه، آگهی‌ها به صورت موقت نمایش داده می‌شوند.")
