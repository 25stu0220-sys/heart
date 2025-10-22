import numpy as np
import matplotlib.pyplot as plt

# t 값 생성 (0~2pi 범위)
t = np.linspace(0, 2 * np.pi, 1000)

# 하트 곡선 공식
x = 16 * np.sin(t)**3
y = 13 * np.cos(t) - 5 * np.cos(2*t) - 2 * np.cos(3*t) - np.cos(4*t)

plt.figure(figsize=(6,6))
plt.plot(x, y, color='red', linewidth=3)
plt.fill_between(x, y, color='pink')  # 하트 내부 색칠
plt.title("Heart Shape with Matplotlib", fontsize=16)
plt.axis('equal')  # x, y 비율 같게
plt.axis('off')    # 축 제거
plt.show()
