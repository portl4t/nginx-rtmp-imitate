# nginx-rtmp-imitate

### Description
Based on nginx-rtmp-module, flush the rtmp stream which is read from file to the player.

### Example

    rtmp {
        chunk_size 40960;

        server {
            listen 1935;

            application myapp {
                live on;
                imitate_fname /xxx/1.rtmp;      # raw rtmp data, start from onMetaData
            }
        }
    }

