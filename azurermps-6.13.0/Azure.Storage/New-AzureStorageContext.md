---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
ms.openlocfilehash: 9de6b2b52205bdf80de9c57e3e338f4b7216c5ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431515"
---
# New-AzureStorageContext

## Sinopse
Cria um contexto de armazenamento do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### OAuthAccount (padrão)
```
New-AzureStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKey
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### OAuthAccountEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### ConnectionString
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureStorageContext** cria um contexto de armazenamento do Azure.

## EXEMPLOS

### Exemplo 1: criar um contexto especificando um nome e uma chave de conta de armazenamento
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Esse comando cria um contexto para a conta chamada ContosoGeneral que usa a chave especificada.

### Exemplo 2: criar um contexto especificando uma cadeia de conexão
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

Esse comando cria um contexto com base na cadeia de conexão especificada para a conta ContosoGeneral.

### Exemplo 3: criar um contexto para uma conta de armazenamento anônimo
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Esse comando cria um contexto para uso anônimo para a conta chamada ContosoGeneral.
O comando especifica HTTP como um protocolo de conexão.

### Exemplo 4: criar um contexto usando a conta de armazenamento de desenvolvimento local
```
C:\PS>New-AzureStorageContext -Local
```

Esse comando cria um contexto usando a conta de armazenamento de desenvolvimento local.
O comando especifica o parâmetro *local* .

### Exemplo 5: obter o contêiner para a conta de armazenamento do desenvolvedor local
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

Esse comando cria um contexto usando a conta de armazenamento de desenvolvimento local e, em seguida, passa o novo contexto para o cmdlet **Get-AzureStorageContainer** usando o operador pipeline.
O comando obtém o contêiner de armazenamento do Azure para a conta de armazenamento do desenvolvedor local.

### Exemplo 6: obter vários contêineres
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

O primeiro comando cria um contexto usando a conta de armazenamento de desenvolvimento local e, em seguida, armazena esse contexto na variável $Context 01.
O segundo comando cria um contexto para a conta chamada ContosoGeneral que usa a chave especificada e, em seguida, armazena esse contexto na variável $Context 02.
O comando final Obtém os contêineres para os contextos armazenados em $Context 01 e $Context 02 usando **Get-AzureStorageContainer**.

### Exemplo 7: criar um contexto com um ponto de extremidade
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

Esse comando cria um contexto de armazenamento do Azure que tem o ponto de extremidade de armazenamento especificado.
O comando cria o contexto da conta chamada ContosoGeneral que usa a chave especificada.

### Exemplo 8: criar um contexto com um ambiente especificado
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Esse comando cria um contexto de armazenamento do Azure que tem o ambiente do Azure especificado.
O comando cria o contexto da conta chamada ContosoGeneral que usa a chave especificada.

### Exemplo 9: criar um contexto usando um token SAS
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

O primeiro comando gera um token SAS usando o cmdlet **New-AzureStorageContainerSASToken** para o contêiner chamado ContosoMain e, em seguida, armazena esse token na variável $SasToken.
Esse token é para permissões de leitura, adição, atualização e exclusão.
O segundo comando cria um contexto para a conta chamada ContosoGeneral que usa o token SAS armazenado no $SasToken e, em seguida, armazena esse contexto na variável $Context.
O comando final lista todos os BLOBs associados ao contêiner nomeado ContosoMain usando o contexto armazenado em $Context.

### Exemplo 10: criar um contexto usando a autenticação OAuth
```
C:\PS>Connect-AzureRmAccount
C:\PS> $Context = New-AzureStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

Esse comando cria um contexto usando a autenticação OAuth.

## OS

### -Anônimo
Indica que esse cmdlet cria um contexto de armazenamento do Azure para logon anônimo.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
Especifica uma cadeia de conexão para o contexto de armazenamento do Azure.

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ponto de extremidade
Especifica o ponto de extremidade para o contexto de armazenamento do Azure.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ambiente
Especifica o ambiente do Azure.
Os valores aceitáveis para esse parâmetro são: AzureCloud e AzureChinaCloud.
Para obter mais informações, digite `Get-Help Get-AzureEnvironment` .

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
Indica que esse cmdlet cria um contexto usando a conta de armazenamento de desenvolvimento local.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocolo
Protocolo de transferência (HTTPS/HTTP).

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasToken
Especifica um token de assinatura de acesso compartilhado (SAS) para o contexto.

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
Especifica uma chave de conta de armazenamento do Azure.
Esse cmdlet cria um contexto para a chave que esse parâmetro especifica.

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Especifica um nome de conta de armazenamento do Azure.
Esse cmdlet cria um contexto para a conta que esse parâmetro especifica.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseConnectedAccount
Indica que esse cmdlet cria um contexto de armazenamento do Azure com Autenticação OAuth.
O cmdlet usará a autenticação OAuth por padrão, quando outros anthentication não forem especificados.

```yaml
Type: SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseConnectedAccount
Indica que esse cmdlet cria um contexto de armazenamento do Azure com Autenticação OAuth.
O cmdlet usará a autenticação OAuth por padrão, quando outros anthentication não forem especificados.

```yaml
Type: SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
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

### System. String

## EXIBE

### Microsoft. WindowsAzure. Commands. Storage. AzureStorageContext

## INFORMA

## LINKS RELACIONADOS

[Get-AzureStorageBlob](./Get-AzureStorageBlob.md)

[New-AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)


