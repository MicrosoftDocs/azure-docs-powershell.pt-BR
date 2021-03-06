---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae22e6923a03864b9371ccdf5379ef9b6bf5189d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776227"
---
# New-AzStorageContext

## Sinopse
Cria um contexto de armazenamento do Azure.

## SYNTAX

### AccountNameAndKey (padrão)
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### ConnectionString
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzStorageContext** cria um contexto de armazenamento do Azure.

## EXEMPLOS

### Exemplo 1: criar um contexto especificando um nome e uma chave de conta de armazenamento
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Esse comando cria um contexto para a conta chamada ContosoGeneral que usa a chave especificada.

### Exemplo 2: criar um contexto especificando uma cadeia de conexão
```
C:\PS>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

Esse comando cria um contexto com base na cadeia de conexão especificada para a conta ContosoGeneral.

### Exemplo 3: criar um contexto para uma conta de armazenamento anônimo
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Esse comando cria um contexto para uso anônimo para a conta chamada ContosoGeneral.
O comando especifica HTTP como um protocolo de conexão.

### Exemplo 4: criar um contexto usando a conta de armazenamento de desenvolvimento local
```
C:\PS>New-AzStorageContext -Local
```

Esse comando cria um contexto usando a conta de armazenamento de desenvolvimento local.
O comando especifica o parâmetro *local* .

### Exemplo 5: obter o contêiner para a conta de armazenamento do desenvolvedor local
```
C:\PS>New-AzStorageContext -Local | Get-AzStorageContainer
```

Esse comando cria um contexto usando a conta de armazenamento de desenvolvimento local e, em seguida, passa o novo contexto para o cmdlet **Get-AzStorageContainer** usando o operador pipeline.
O comando obtém o contêiner de armazenamento do Azure para a conta de armazenamento do desenvolvedor local.

### Exemplo 6: obter vários contêineres
```
C:\PS>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

O primeiro comando cria um contexto usando a conta de armazenamento de desenvolvimento local e, em seguida, armazena esse contexto na variável $Context 01.
O segundo comando cria um contexto para a conta chamada ContosoGeneral que usa a chave especificada e, em seguida, armazena esse contexto na variável $Context 02.
O comando final Obtém os contêineres para os contextos armazenados em $Context 01 e $Context 02 usando **Get-AzStorageContainer**.

### Exemplo 7: criar um contexto com um ponto de extremidade
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

Esse comando cria um contexto de armazenamento do Azure que tem o ponto de extremidade de armazenamento especificado.
O comando cria o contexto da conta chamada ContosoGeneral que usa a chave especificada.

### Exemplo 8: criar um contexto com um ambiente especificado
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Esse comando cria um contexto de armazenamento do Azure que tem o ambiente do Azure especificado.
O comando cria o contexto da conta chamada ContosoGeneral que usa a chave especificada.

### Exemplo 9: criar um contexto usando um token SAS
```
C:\PS>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

O primeiro comando gera um token SAS usando o cmdlet **New-AzStorageContainerSASToken** para o contêiner chamado ContosoMain e, em seguida, armazena esse token na variável $SasToken.
Esse token é para permissões de leitura, adição, atualização e exclusão.
O segundo comando cria um contexto para a conta chamada ContosoGeneral que usa o token SAS armazenado no $SasToken e, em seguida, armazena esse contexto na variável $Context.
O comando final lista todos os BLOBs associados ao contêiner nomeado ContosoMain usando o contexto armazenado em $Context.

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
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
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
Parameter Sets: SasTokenWithAzureEnvironment
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
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
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
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. WindowsAzure. Commands. Storage. AzureStorageContext

## INFORMA

## LINKS RELACIONADOS

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[New-AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)


