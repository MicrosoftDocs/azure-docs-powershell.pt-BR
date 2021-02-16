---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118583"
---
# New-AzStorageContext

## Sinopse
Cria um contexto de Armazenamento do Azure.

## Sintaxe

### OAuthAccount (Padrão)
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKey
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

### OAuthAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### Connectionstring
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## Descrição
O **cmdlet New-AzStorageContext cria** um contexto de Armazenamento do Azure.
A Autenticação padrão de um Contexto de Armazenamento é o OAuth (Azure AD), se apenas o nome da conta de armazenamento for de entrada.
Ver detalhes da autenticação do Serviço de Armazenamento em https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services .

## Exemplos

### Exemplo 1: Criar um contexto especificando o nome e a chave de uma conta de armazenamento
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Esse comando cria um contexto para a conta chamada ContosoGeneral que usa a chave especificada.

### Exemplo 2: Criar um contexto especificando uma cadeia de conexão
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

Esse comando cria um contexto com base na cadeia de conexão especificada da conta ContosoGeneral.

### Exemplo 3: Criar um contexto para uma conta de armazenamento anônimo
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Esse comando cria um contexto para uso anônimo para a conta chamada ContosoGeneral.
O comando especifica HTTP como um protocolo de conexão.

### Exemplo 4: Criar um contexto usando a conta de armazenamento de desenvolvimento local
```
PS C:\>New-AzStorageContext -Local
```

Esse comando cria um contexto usando a conta de armazenamento de desenvolvimento local.
O comando especifica o parâmetro *Local.*

### Exemplo 5: Obter o contêiner da conta de armazenamento do desenvolvedor local
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

Esse comando cria um contexto usando a conta de armazenamento de desenvolvimento local e passa o novo contexto para o cmdlet **Get-AzStorageContainer** usando o operador de pipeline.
O comando obtém o contêiner de Armazenamento do Azure para a conta de armazenamento do desenvolvedor local.

### Exemplo 6: Obter vários contêineres
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

O primeiro comando cria um contexto usando a conta de armazenamento de desenvolvimento local e armazena esse contexto na variável $Context 01.
O segundo comando cria um contexto para a conta chamada ContosoGeneral que usa a chave especificada e armazena esse contexto na variável $Context 02.
O comando final obtém os contêineres dos contextos armazenados no $Context 01 e $Context 02 usando **Get-AzStorageContainer.**

### Exemplo 7: Criar um contexto com um ponto de extremidade
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

Esse comando cria um contexto de Armazenamento do Azure que tem o ponto de extremidade de armazenamento especificado.
O comando cria o contexto para a conta chamada ContosoGeneral que usa a chave especificada.

### Exemplo 8: Criar um contexto com um ambiente especificado
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Esse comando cria um contexto de armazenamento do Azure que tem o ambiente do Azure especificado.
O comando cria o contexto para a conta chamada ContosoGeneral que usa a chave especificada.

### Exemplo 9: Criar um contexto usando um token SAS
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

O primeiro comando gera um token SAS usando o cmdlet **New-AzStorageContainerSASToken** para o contêiner chamado ContosoMain e armazena esse token na variável $SasToken.
Esse token é para permissões de leitura, adoção, atualização e exclusão.
O segundo comando cria um contexto para a conta chamada ContosoGeneral que usa o token SAS armazenado no $SasToken e armazena esse contexto na variável $Context dados.
O comando final lista todos os blobs associados ao contêiner chamado ContosoMain usando o contexto armazenado em $Context.

### Exemplo 10: Criar um contexto usando a Autenticação OAuth
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

Esse comando cria um contexto usando a Autenticação OAuth (Azure AD).

## Parâmetros

### -Anônimo
Indica que esse cmdlet cria um contexto de Armazenamento do Azure para logon anônimo.

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
Especifica uma cadeia de conexão para o contexto de Armazenamento do Azure.

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
Especifica o ponto de extremidade para o contexto de Armazenamento do Azure.

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
Os valores aceitáveis para este parâmetro são: AzureCloud e AzureChinaCloud.
Para obter mais informações, digite `Get-Help Get-AzEnvironment` .

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
Protocolo de Transferência (https/http).

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
Especifica um token SAS (Assinatura de Acesso Compartilhado) para o contexto.

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
Esse cmdlet cria um contexto para a chave especificada por esse parâmetro.

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
Especifica o nome de uma conta de armazenamento do Azure.
Esse cmdlet cria um contexto para a conta especificada por esse parâmetro.

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
Indica que esse cmdlet cria um contexto de Armazenamento do Azure com Autenticação do OAuth (Azure AD).
O cmdlet usará a Autenticação OAuth por padrão, quando outra autenticação não for especificada.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
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

### System.String

## Saídas

### Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext

## Notas

## LINKS RELACIONADOS

[Get-AzStorageB ltd](./Get-AzStorageBlob.md)

[New-AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)


