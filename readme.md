```ts
 const SingrelUrl = await getSignedUrl(
      r2,
      new PutObjectCommand({
        Bucket: "project-yt",
        Key: "video.mp4",
        ContentType: "video/mp4",
      }),
      { expiresIn: 600 }
    );
  // configlib 

  // npm i @aws-sdk/client-s3
  // npm i @aws-sdk/client-s3


import { S3Client } from "@aws-sdk/client-s3";

const endpoint = process.env.CLOUDFARE_URL;
const accessKeyId = process.env.CLOUDFARE_KEY_ID;
const secretAccessKey = process.env.CLOUDFARE_SECRET_KEY;

if (!endpoint || !accessKeyId || !secretAccessKey) {
  throw new Error("Missing necessary environment variables for S3Client");
}

export const r2 = new S3Client({
  region: 'auto',
  endpoint: endpoint,
  credentials: {
    accessKeyId,
    secretAccessKey,
  },
})
```

### Later request to URL

  
