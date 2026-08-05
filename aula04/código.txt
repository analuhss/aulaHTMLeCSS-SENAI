# pip install yt-dlp
import yt_dlp

url = input("Cole a URL do vídeo: ")

opcoes = {
    "format": "bestvideo+bestaudio/best",
    "merge_output_format": "mp4",
    "outtmpl": "%(title)s.%(ext)s",
}

with yt_dlp.YoutubeDL(opcoes) as ydl:
    ydl.download([url])

print("Download concluído!")