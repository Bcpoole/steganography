# trithemius
Stenography library written in rust. Supports using both Alpha and full RGBA channels. Also takes in a start index for where to write and will wrap around.

## Load Image
    let img = load_img(IMG_PATH);

## Cyphers
Cyphers are used to encode and decode messages and images.

### Encode

    CYPHER::encode(img, msg.as_bytes(), start_index)

### Decode

    CYPHER::decode(alpha_encoded_img, start_index);

### AlphaCypher
Encodes message in Alpha channel of pixels.

Decoding goes until alpha = 255 or end.

### RGBACypher
Encodes message in RGBA channels of pixels.

Decoding goes until reading a byte value 0.
