# Codex için Yapay Zekâ Orkestrası

Rues Community'nin [Yapay Zekâ Orkestrası](https://github.com/ruesandora/RuesCommunity/tree/main/icerikler/01-yapay-zeka-orkestrasi) fikrinden esinlenen, bağımsız yazılmış Codex rehberi. Model eşlemesi kullanıcı isteğine göre hazırlanmıştır. Kaynak sayfanın HTML'i ve görselleri bu depoya alınmamıştır.

[Rehberi aç](index.html) — tek HTML dosyası, tarayıcıda doğrudan çalışır.

## Kurulum

1. Bu depodaki `AGENTS.md` ve `.codex/` klasörünü kendi projenizin köküne kopyalayın.
2. Codex'i proje kökünde açın. Proje ayarı şefi `gpt-6.1-sol` / `medium` olarak seçer.
3. Alt ajan istediğinizde rol adını açıkça belirtin. Örnek: “`gelistirici` ajanıyla form hatasını düzelt; ardından bağımsız `denetci` ajanıyla incele.”
4. Güvenlik, ödeme, mahremiyet veya veri kaybı riski için `denetci-riskli` kullanın.

| Rol | Model | Akıl yürütme |
|---|---|---|
| Şef | `gpt-6.1-sol` | `medium` |
| Denetçi | `gpt-6-luna` | `high` |
| Riskli iş denetçisi | `gpt-6.1-sol` | `medium` |
| Geliştirici, araştırmacı | `gpt-6-luna` | `medium` |
| Yükleyici | `gpt-6-luna` | `low` |
| Tasarımcı, video üreticisi | `gpt-6.1-sol` | `medium` |

Codex özel ajanları `.codex/agents/*.toml` dosyalarından yükler. Kalıcı proje yönergeleri `AGENTS.md` içindedir. Ajanların kullanılabilirliği ve model erişimi hesabınıza bağlıdır. [Codex alt ajan belgeleri](https://learn.chatgpt.com/docs/agent-configuration/subagents) · [AGENTS.md belgeleri](https://learn.chatgpt.com/docs/agent-configuration/agents-md)

## Kaynak

Fikir kaynağı: [RuesCommunity / 01-yapay-zeka-orkestrasi](https://github.com/ruesandora/RuesCommunity/tree/main/icerikler/01-yapay-zeka-orkestrasi). Kaynak bağlantısı rehber sayfasında da gösterilir.
