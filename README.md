# Bikin Explorer Axelar

Pushkan Lava Jalur Explorer :
- Akun Github
- Akun Vercel (Tinggal Konek Pake Github)

1. Fork ni github, tulisannya sebelah kanan (https://github.com/ping-pub/explorer/)
   
2. Setelah itu cari file package.json , paste ja kode ini

```json
{
  "name": "ping.pub",
  "version": "3.0.0",
  "private": true,
  "target": "",
  "scripts": {
    "dev": "vite",
    "serve": "vite",
    "build": "run-p type-check build-only",
    "preview": "vite preview",
    "build-only": "vite build",
    "type-check": "vue-tsc --noEmit"
  },
  "dependencies": {
    "@chenfengyuan/vue-countdown": "2",
    "@cosmjs/crypto": "^0.32.3",
    "@cosmjs/amino": "^0.32.3",
    "@cosmjs/encoding": "^0.32.3",
    "@cosmjs/stargate": "^0.32.3",
    "@iconify/vue": "^4.1.0",
    "@intlify/unplugin-vue-i18n": "^0.8.2",
    "@leapwallet/cosmos-snap-provider": "^0.1.20",
    "@leapwallet/name-matcha": "^1.1.0",
    "@osmonauts/lcd": "^0.8.0",
    "@personaxyz/ad-sdk": "0.0.21",
    "@ping-pub/chain-registry-client": "^0.0.25",
    "@vitejs/plugin-vue-jsx": "^3.0.0",
    "@vueuse/core": "^9.12.0",
    "@vueuse/integrations": "^10.1.2",
    "@vueuse/math": "^9.12.0",
    "apexcharts": "^3.37.1",
    "autoprefixer": "^10.4.14",
    "axios": "^1.3.2",
    "buffer": "^6.0.3",
    "build": "^0.1.4",
    "cross-fetch": "^3.1.5",
    "daisyui": "^3.1.0",
    "dayjs": "^1.11.7",
    "lazy-load-vue3": "^1.3.0",
    "long": "^5.2.1",
    "md-editor-v3": "^2.8.1",
    "numeral": "^2.0.6",
    "osmojs": "^14.0.0-rc.0",
    "pinia": "^2.0.28",
    "postcss": "^8.4.23",
    "qrcode": "^1.5.3",
    "tailwindcss": "^3.3.1",
    "theme-change": "^2.5.0",
    "vite-plugin-vue-layouts": "^0.7.0",
    "vue": "^3.2.45",
    "vue-i18n": "^9.2.2",
    "vue-prism-component": "^2.0.0",
    "vue-router": "^4.1.6",
    "vue3-apexcharts": "^1.4.1",
    "vue3-json-viewer": "^2.2.2",
    "vue3-perfect-scrollbar": "^1.6.1"
  },
  "devDependencies": {
    "@osmonauts/telescope": "^0.88.2",
    "@types/marked": "^4.0.8",
    "@types/node": "^18.11.12",
    "@types/numeral": "^2.0.2",
    "@types/semver": "7.5.0",
    "@vitejs/plugin-vue": "^4.0.0",
    "@vue/tsconfig": "^0.1.3",
    "npm-run-all": "^4.1.5",
    "prettier": "^2.7.1",
    "sass": "^1.58.0",
    "shiki": "^1.0.0-beta.0",
    "typescript": "~4.9.5",
    "unplugin-auto-import": "^0.13.0",
    "unplugin-vue-components": "^0.23.0",
    "unplugin-vue-define-options": "1.1.4",
    "vite": "^4.4.9",
    "vite-plugin-pages": "^0.28.0",
    "vue-json-viewer": "3",
    "vue-tsc": "^1.0.12"
  }
}
```

3. Setelah tu masuk ke folder chains/mainnet , add file baru namanya axelar.json

Pastiin diakhir rpc gak ada ini "/"

```json
{
    "chain_name": "axelar",
    "api": [
        "ini-isi-pake-rpc-mainnet-lcd-axelar"
    ],
    "rpc": [
        "ini-isi-pake-rpc-mainnet-rpc-axelar"
    ],
    "snapshot_provider": "",
    "sdk_version": "0.45.6",
    "coin_type": "118",
    "min_tx_fee": "800",
    "addr_prefix": "axelar",
    "logo": "/logos/axelar.svg",
    "theme_color": "#161723",
    "assets": [
        {
            "base": "uaxl",
            "symbol": "AXL",
            "exponent": "6",
            "coingecko_id": "axelar",
            "logo": "/logos/axelar.svg"
        },
        {
            "base": "uusdc",
            "symbol": "axlUSDC",
            "exponent": "6",
            "coingecko_id": "usd-coin",
            "logo": "/logos/usdc.svg"
        },
        {
            "base": "uusdt",
            "symbol": "axlUSDT",
            "exponent": "6",
            "coingecko_id": "tether",
            "logo": "/logos/usdt.svg"
        },
        {
            "base": "dai-wei",
            "symbol": "axlDAI",
            "exponent": "18",
            "coingecko_id": "dai",
            "logo": "/logos/dai.svg"
        },
        {
            "base": "weth-wei",
            "symbol": "axlWETH",
            "exponent": "18",
            "coingecko_id": "ethereum",
            "logo": "/logos/weth.svg"
        },
        {
            "base": "wmatic-wei",
            "symbol": "axlWMATIC",
            "exponent": "18",
            "coingecko_id": "matic-network",
            "logo": "/logos/wmatic.svg"
        },
        {
            "base": "wavax-wei",
            "symbol": "axlWAVAX",
            "exponent": "18",
            "coingecko_id": "avalanche-2",
            "logo": "/logos/wavax.svg"
        },
        {
            "base": "dot-planck",
            "symbol": "axlDOT",
            "exponent": "10",
            "coingecko_id": "polkadot",
            "logo": "/logos/dot.svg"
        }
    ]
}
```

4. Kalo udah masuk ke vercel.com , login pake github
   
6. Add new project, ntar pilih repo github hasil fork
   
7. Deploy


Thanks to
@KatouMegumii
