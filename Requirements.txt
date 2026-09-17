import streamlit as st
import pandas as pd
from datetime import datetime

# ==============================
# CẤU HÌNH TRANG
# ==============================
st.set_page_config(
    page_title="Restaurant Order",
    page_icon="🍴",
    layout="wide"
)

# ==============================
# TIÊU ĐỀ
# ==============================
st.title("🍴 NHÀ HÀNG FOOD SUPPORT")
st.caption("Hệ thống gọi món và quản lý hóa đơn")

# ==============================
# KHỞI TẠO SESSION
# ==============================
if "cart" not in st.session_state:
    st.session_state.cart = []

if "invoices" not in st.session_state:
    st.session_state.invoices = []

# ==============================
# DANH SÁCH MENU
# ==============================
foods = {
    "Pizza Hải Sản": 120000,
    "Mì Ý Bò Bằm": 50000,
    "Burger Gà": 65000,
    "Salad Trộn": 50000,
    "Bít Tết Bò Mỹ": 250000,
    "Sườn Nướng BBQ": 180000,
    "Cánh Gà Chiên Mắm": 75000
