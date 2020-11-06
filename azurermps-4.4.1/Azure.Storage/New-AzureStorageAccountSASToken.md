---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 8b280a13e7eb7a2e6ea3f52b4a121f313504b2ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427067"
---
# New-AzureStorageAccountSASToken

## Sinopse
Cria um token SAS no nível da conta.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureStorageSASToken** cria um token de assinatura de acesso compartilhado (SAS) de conta em nível de conta para uma conta de armazenamento do Azure.

Você pode usar o token SAS para delegar permissões para vários serviços ou para delegar permissões para serviços que não estão disponíveis com um token de SAS no nível do objeto.

## EXEMPLOS

### Exemplo 1: criar um token SAS em nível de conta com permissão completa
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

Esse comando cria um token SAS no nível da conta com permissão total.

### Exemplo 2: criar um token SAS em nível de conta para um intervalo de endereços IP
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

Esse comando cria um token SAS em nível de conta para solicitações somente HTTPS do intervalo de endereços IP especificado.

## OS

### -Contexto
Especifica o contexto de armazenamento do Azure.
Você pode usar o cmdlet New-AzureStorageContext para obter um objeto **AzureStorageContext** .

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ExpiryTime
Especifica o tempo em que a assinatura de acesso compartilhado se torna inválida.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddressOrRange
Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.
O intervalo é inclusivo.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Permissão
Especifica as permissões para a conta de armazenamento.
As permissões só serão válidas se corresponderem ao tipo de recurso especificado.
Para obter mais informações sobre valores de permissão aceitáveis, consulte construindo uma conta SAShttps://go.microsoft.com/fwlink/?LinkId=799514

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocolo
Especifica o protocolo permitido para uma solicitação feita com a SAS da conta.
Os valores aceitáveis para esse parâmetro são:

- HttpsOnly
- HttpsOrHttp

O valor padrão é HttpsOrHttp.

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
Especifica os tipos de recursos que estão disponíveis com o token SAS.
Os valores aceitáveis para esse parâmetro são:

- Nenhuma
- Atender
- Contêiner
- Objeto

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Serviço
Especifica o serviço.
Os valores aceitáveis para esse parâmetro são:

- Nenhuma
- Irregular
- Arquivos
- Coloca
- TableName

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Especifica o tempo, como um objeto **DateTime** , no qual a SAS se torna válida.
Para obter um objeto **DateTime** , use o cmdlet Get-Date.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### IStorageContext

O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline

## EXIBE

### System. String

## INFORMA

## LINKS RELACIONADOS

[New-AzureStorageBlobSASToken](./New-AzureStorageBlobSASToken.md)

[New-AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)

[New-AzureStorageFileSASToken](./New-AzureStorageFileSASToken.md)

[New-AzureStorageQueueSASToken](./New-AzureStorageQueueSASToken.md)

[New-AzureStorageShareSASToken](./New-AzureStorageShareSASToken.md)

[New-AzureStorageTableSASToken](./New-AzureStorageTableSASToken.md)


