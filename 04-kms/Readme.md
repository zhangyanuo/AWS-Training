# KMS

## Basic

注意⚠️⚠️⚠️：尽量使用一个 KMS 进行练习

AC:

1. 回答下列问题
    1. KMS 是什么服务？能解决什么问题？

        答：KMS是创建和控制客户CMK用于加密时的主密钥；即用于加密您的数据的加密密钥

    2. 使用 KMS key 的方式有哪些？

        答：加密和解密，签名和验证

    3. 可以对 KMS key 进行哪些操作？（至少 5 个）

        答：创建，查看，编辑，启用、禁用和标记

2. 使用 CLI 进行练习
    1. 创建对称加密的 KMS key

        ```aws --profile tw-yanuo-account kms create-key```


       
        ``aws —profile tw-yanuo-account kms get-key-policy --key-id 3acb99c7-d25f-48e6-bc02-f4e401722ec9 --policy-name default --output text``

       

    2. 加密一段字符串

       ```

        aws --profile tw-yanuo-account kms encrypt \
            --key-id 3acb99c7-d25f-48e6-bc02-f4e401722ec9 \
            --plaintext fileb://encryptTest \
            --output text \
            --query CiphertextBlob | base64 \
            --decode > encryptTestResult
        ```

       

    3. 使用同一个 Key 重新加密同一段字符串，观察结果

      

    4. 将加密后的字符串进行解密

        ```
        aws --profile tw-yanuo-account kms decrypt \
            --ciphertext-blob fileb://encryptTestResult \
            --key-id 3acb99c7-d25f-48e6-bc02-f4e401722ec9 \
            --output text \
            --query Plaintext | base64 \
            --decode > decryptTestResult
        ```

      

## Advanced

注意⚠️⚠️⚠️：尽量使用一个 KMS 进行练习

AC:

1. 练习
    1. 使用 CloudFormation 创建 KMS RSA_4096 的 key
    2. 加密并解密一段字符串
    3. 将 KMS Key 与其他服务一同使用（Basic 里的对称加密 Key），如
        1. 加密 S3 文件
        2. 加密 parameter store 里的值
2. 回答下列问题
    1. 如何进行 Key rotation？
    2. AWS 如何进行自动 Key rotation？
    3. 自动 Key rotation 之后收费有什么变化？

## Reference

- Kick Off 录屏：[https://drive.google.com/file/d/1W7YvwUBsxtGmIcA5xCxubErMQh8UpMRV/view?usp=sharing](https://drive.google.com/file/d/1W7YvwUBsxtGmIcA5xCxubErMQh8UpMRV/view?usp=sharing)
- [https://docs.aws.amazon.com/kms/latest/developerguide/overview.html](https://docs.aws.amazon.com/kms/latest/developerguide/overview.html)
- [https://docs.aws.amazon.com/crypto/latest/userguide/awscryp-choose-kms.html](https://docs.aws.amazon.com/crypto/latest/userguide/awscryp-choose-kms.html)
- [https://awscli.amazonaws.com/v2/documentation/api/latest/reference/kms/index.html](https://awscli.amazonaws.com/v2/documentation/api/latest/reference/kms/index.html)
- [https://docs.aws.amazon.com/kms/latest/developerguide/getting-started.html](https://docs.aws.amazon.com/kms/latest/developerguide/getting-started.html)
- [https://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html](https://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html)
- [https://aws.amazon.com/kms/pricing/](https://aws.amazon.com/kms/pricing/)
- [https://docs.aws.amazon.com/kms/latest/developerguide/symm-asymm-choose.html](https://docs.aws.amazon.com/kms/latest/developerguide/symm-asymm-choose.html)

[Copy of KMS](https://www.notion.so/Copy-of-KMS-5897b4036fb1428fb4e780b847d80c58)