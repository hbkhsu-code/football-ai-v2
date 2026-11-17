
mkdir -p extracted

ZIP_FILE=$(find . -maxdepth 1 -type f -iname "*.zip" | head -n 1)

unzip -o "$ZIP_FILE" -d extracted

echo "===== 專案檔案清單 ====="
find extracted -maxdepth 4 -type f | sort
