---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 3c79266c6f6e9b5200e2224f463ac12fe409bf0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115653"
---
# New-AzStorageAccountSASToken

## Sinopse
Cria um token SAS no nível da conta.

## Sintaxe

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **New-AzStorageSASToken** cria um token SAS (assinatura de acesso compartilhado) no nível da conta para uma conta de Armazenamento do Azure.
Você pode usar o token SAS para delegar permissões para vários serviços ou para delegar permissões para serviços não disponíveis com um token SAS no nível de objeto.

## Exemplos

### Exemplo 1: Criar um token SAS no nível da conta com permissão total
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

Esse comando cria um token SAS no nível da conta com permissão total.

### Exemplo 2: Criar um token SAS no nível da conta para um intervalo de endereços IP
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

Esse comando cria um token SAS no nível da conta para solicitações somente HTTPS do intervalo especificado de endereços IP.

## Parâmetros

### -Contexto
Especifica o contexto de armazenamento do Azure.
Você pode usar o cmdlet New-AzStorageContext para obter um **objeto AzureStorageContext.**

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryTime
Especifica o momento em que a assinatura de acesso compartilhado se torna inválida.

```yaml
Type: System.Nullable`1[System.DateTime]
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
Type: System.String
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
É importante observar que essa é uma cadeia de caracteres, como `rwd` (para Leitura, Gravação e Exclusão).
Para obter mais informações sobre valores de permissão aceitáveis, consulte Construir um SAS de Conta http://go.microsoft.com/fwlink/?LinkId=799514

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocolo
Especifica o protocolo permitido para uma solicitação feita com o SAS da conta.
Os valores aceitáveis para este parâmetro são:
- HttpsOnly
- HttpsOrHttp O valor padrão é httpsOrHttp.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
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
Especifica os tipos de recursos disponíveis com o token SAS.
Os valores aceitáveis para este parâmetro são:
- Nenhum
- Serviço
- Recipiente
- Objeto

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountResourceTypes
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
Os valores aceitáveis para este parâmetro são:
- Nenhum
- Blob
- Arquivo
- Fila
- Tabela

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountServices
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
Especifica a hora, como um objeto **DateTime,** no qual o SAS se torna válido.
Para obter um **objeto DateTime,** use o cmdlet Get-Date dados.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## Saídas

### System.String

## Notas

## LINKS RELACIONADOS

[New-AzStorageBtrucSASToken](./New-AzStorageBlobSASToken.md)

[New-AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)

[New-AzStorageFileSASToken](./New-AzStorageFileSASToken.md)

[New-AzStorageQueueSASToken](./New-AzStorageQueueSASToken.md)

[New-AzStorageShareSASToken](./New-AzStorageShareSASToken.md)

[New-AzStorageTableSASToken](./New-AzStorageTableSASToken.md)


