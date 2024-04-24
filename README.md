# NETWORK-PERFORMANCE-ANALYZER
import speedtest

def run_speed_test():
    st = speedtest.Speedtest()
    st.get_best_server()

    print("Testing download speed...")
    download_speed = st.download() / 1024 / 1024  # Convert to Mbps
    print(f"Download speed: {download_speed:.2f} Mbps")

    print("\nTesting upload speed...")
    upload_speed = st.upload() / 1024 / 1024  # Convert to Mbps
    print(f"Upload speed: {upload_speed:.2f} Mbps")

if __name__ == "__main__":
    run_speed_test()
