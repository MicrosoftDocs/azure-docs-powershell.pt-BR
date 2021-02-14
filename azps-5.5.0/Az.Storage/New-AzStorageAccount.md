---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0e1243765064717c6e0030b437c07a176a232f44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115660"
---
# New-AzStorageAccount

## Sinopse
Cria uma conta de armazenamento.

## Sintaxe

### AzureActiveDirectoryDomainServicesForFile (Padrão)
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

### ActiveDirectoryDomainServicesForFile
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] [-EnableActiveDirectoryDomainServicesForFile <Boolean>]
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## Descrição
O **cmdlet New-AzStorageAccount cria** uma conta de Armazenamento do Azure.

## Exemplos

### Exemplo 1: Criar uma conta de armazenamento
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

Esse comando cria uma conta de Armazenamento para o grupo de recursos MyResourceGroup.

### Exemplo 2: Criar uma conta de Armazenamento de Blob com o BlobStorage Kind e o AccessTier hot
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

Esse comando cria uma conta de Armazenamento de Blob que, com o BlobStorage Kind e o AccessTier

### Exemplo 3: Criar uma conta de armazenamento com Kind StorageV2 e gerar e atribuir uma identidade para o Azure KeyVault.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

Esse comando cria uma conta de armazenamento com Kind StorageV2.  Ele também gera e atribui uma identidade que pode ser usada para gerenciar chaves de conta por meio do Azure KeyVault.

### Exemplo 4: Criar uma conta de armazenamento com NetworkRuleSet a partir de JSON
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

Esse comando cria uma conta de armazenamento que tem a propriedade NetworkRuleSet do JSON

### Exemplo 5: Criar uma conta de Armazenamento com Namespace Hierárquico habilitado.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

Esse comando cria uma conta de Armazenamento com Namespace Hierárquico habilitado.

### Exemplo 6: Criar uma conta de armazenamento com a Autenticação DS do Azure Files AAD e habilitar o compartilhamento de arquivos grande.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

Esse comando cria uma conta de armazenamento com a Autenticação DS do Azure Files AAD e habilita o compartilhamento de arquivos grande.

### Exemplo 7: Criar uma conta de armazenamento com a autenticação de serviço de domínio arquivos active directory.
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

Esse comando cria uma conta de armazenamento com a Autenticação de Serviço de Domínio do Active Directory para Arquivos Do Active Directory.

### Exemplo 8: Criar uma conta de Armazenamento com o Serviço de Tabela e Fila usam a chave de criptografia com escopo de conta e exigem criptografia de infraestrutura.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account -RequireInfrastructureEncryption

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\> $account.Encryption.RequireInfrastructureEncryption
True
```

Esse comando cria uma conta de armazenamento com a chave de criptografia de fila e de tabela com escopo de conta e exigir criptografia de infraestrutura; portanto, a fila e a tabela usarão a mesma chave de criptografia com o serviço Blob e Arquivo, e o serviço aplicará uma camada secundária de criptografia com chaves gerenciadas da plataforma para os dados em repouso.
Em seguida, obter as propriedades da conta de armazenamento e exibir o tipo de chave de criptografia de Fila e Serviço de Tabela e o valor RequireInfrastructureEncryption.

### Exemplo 9: Criar conta MinimumTlsVersion e AllowBpublicAccesss
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

O comando criar conta com MinimumTlsVersion e AllowBpublicAccess e mostrar as 2 propriedades da conta criada 

### Exemplo 10: Criar uma conta de armazenamento com a configuração RoutingPreference
```powershell
PS C:\>$account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -PublishMicrosoftEndpoint $true -PublishInternetEndpoint $true -RoutingChoice MicrosoftRouting

PS C:\>$account.RoutingPreference

RoutingChoice    PublishMicrosoftEndpoints PublishInternetEndpoints
-------------    ------------------------- ------------------------
MicrosoftRouting                     True                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : {"Blob":"https://mystorageaccount-microsoftrouting.blob.core.windows.net/","Queue":"https://mystorageaccount-microsoftrouting.queue.core.windows.net/","Table":"https://mystorageaccount-microsoftrouting.table.core.windows.net/","File":"ht
                     tps://mystorageaccount-microsoftrouting.file.core.windows.net/","Web":"https://mystorageaccount-microsoftrouting.z2.web.core.windows.net/","Dfs":"https://mystorageaccount-microsoftrouting.dfs.core.windows.net/"}
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

Esse comando cria uma conta de Armazenamento com a configuração RoutingPreference: PublishMicrosoftEndpoint e PublishInternetEndpoint como true e RoutingChoice como MicrosoftRouting.

## Parâmetros

### -AccessTier
Especifica o nível de acesso da conta de Armazenamento que este cmdlet cria.
Os valores aceitáveis para este parâmetro são: Hot e Cool.
Se você especificar um valor de BlobStorage para o parâmetro *Kind,* deverá especificar um valor para o parâmetro *AccessTier.* Se você especificar um valor de Armazenamento para este parâmetro *Kind,* não especifique o parâmetro *AccessTier.*

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryAzureStorageSid
Especifica o identificador de segurança (SID) para Armazenamento do Azure. Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainGuid
Especifica o GUID do domínio. Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainName
Especifica o domínio principal para o que o servidor DNS do AD é autoritativo. Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainSid
Especifica o identificador de segurança (SID). Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryForestName
Especifica a floresta do Active Directory para obter. Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryNetBiosDomainName
Especifica o nome de domínio do NetBIOS. Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowBpublicAccess
Permitir o acesso público a todos os blobs ou contêineres na conta de armazenamento. A interpretação padrão é verdadeira para esta propriedade.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Executar cmdlet em segundo plano

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignIdentity
Gere e atribua uma nova identidade de conta de armazenamento para esta conta de Armazenamento para ser usada com os principais serviços de gerenciamento, como o Azure KeyVault.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomDomainName
Especifica o nome do domínio personalizado da conta de Armazenamento.
O valor padrão é Armazenamento.

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableActiveDirectoryDomainServicesForFile
Habilitar a Autenticação de Serviço de Domínio do Azure Files Active Directory para a conta de armazenamento.

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAzureActiveDirectoryDomainServicesForFile
Habilitar a Autenticação de Serviço de Domínio do Azure Files Azure Active Directory para a conta de armazenamento.

```yaml
Type: System.Boolean
Parameter Sets: AzureActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHierarchicalNamespace
Indica se a conta de armazenamento habilita ou não o Namespace Hierárquico.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHttpsTrafficOnly
Indica se a conta de armazenamento só habilita o tráfego HTTPS.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableLargeFileShare
Indica se a conta de armazenamento pode ou não dar suporte a compartilhamentos de arquivos grandes com mais de 5 capacidade tib. Depois que a conta for habilitada, o recurso não poderá ser desabilitado. Atualmente, só há suporte para tipos de replicação LRS e ZRS, portanto, as conversões de contas em contas redundantes geográficas não seriam possíveis. Saiba mais em https://go.microsoft.com/fwlink/?linkid=2086047

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionKeyTypeForQueue
Definir o KeyType de Criptografia para Fila. O valor padrão é Serviço.
-Conta: a fila será criptografada com a chave de criptografia com escopo de conta. -Serviço: a fila sempre será criptografada com Service-Managed teclas. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionKeyTypeForTable
De definir o Tipo de Chave de Criptografia para Tabela. O valor padrão é Serviço.
- Conta: A tabela será criptografada com a chave de criptografia com escopo de conta. 
- Serviço: A tabela sempre será criptografada com Service-Managed teclas. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tipo
Especifica o tipo de conta de Armazenamento que este cmdlet cria.
Os valores aceitáveis para este parâmetro são:
- Armazenamento. Conta de Armazenamento de finalidade geral que oferece suporte ao armazenamento de Blobs, Tabelas, Filas, Arquivos e Discos.
- StorageV2. Conta de armazenamento GPv2 (General Purpose Version 2) que oferece suporte a Blobs, Tabelas, Filas, Arquivos e Discos, com recursos avançados como a camada de dados.
- BlobStorage. Conta de Armazenamento de Blob que oferece suporte somente ao armazenamento de Blobs.
- BlockBtrucStorage. Blob Storage account which supports storage of Block Blobs only.
- FileStorage. Conta de Armazenamento de Arquivos que oferece suporte apenas ao armazenamento de Arquivos.
O valor padrão é StorageV2.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: StorageV2
Accept pipeline input: False
Accept wildcard characters: False
```

### -Local
Especifica o local da conta de armazenamento a ser criado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MinimumTlsVersion
A versão TLS mínima a ser permitida em solicitações de armazenamento. A interpretação padrão é TLS 1.0 para esta propriedade.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome da conta de armazenamento a ser criado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkRuleSet
O NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como serviços permitidos para ignorar as regras e como lidar com solicitações que não corresponderem a nenhuma das regras definidas.

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublishInternetEndpoint
Indica se os pontos de extremidade de armazenamento de roteamento da Internet devem ser publicados

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublishMicrosoftEndpoint
Indica se os pontos de extremidade de armazenamento de roteamento da Microsoft devem ser publicados

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos no qual adicionar a conta de Armazenamento.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RoutingChoice
A Opção de Roteamento define o tipo de roteamento de rede escolhido pelo usuário. Os valores possíveis incluem: 'MicrosoftRouting', 'InternetRouting'

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftRouting, InternetRouting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuName
Especifica o nome da SKU da conta de armazenamento que este cmdlet cria.
Os valores aceitáveis para este parâmetro são:
- Standard_LRS. Armazenamento localmente redundante.
- Standard_ZRS. Armazenamento redundante de zona.
- Standard_GRS. Armazenamento geo redundante.
- Standard_RAGRS. Ler o armazenamento geo redundante do acesso.
- Premium_LRS. Armazenamento localmente redundante premium.
- Premium_ZRS. Armazenamento redundante de zona premium.
- Standard_GZRS - Armazenamento redundante de zona geo redundante.
- Standard_RAGZRS - Armazenamento redundante de zona de acesso de leitura.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Pares de valor-chave na forma de uma tabela hash definida como marcas no servidor. Por exemplo: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseSubDomain
Indica se é possível habilitar a validação indireta de CName.

```yaml
Type: System.Nullable`1[System.Boolean]
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

### System.String

## Saídas

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

## Notas

## LINKS RELACIONADOS

[Get-AzStorageAccount](./Get-AzStorageAccount.md)

[Remove-AzStorageAccount](./Remove-AzStorageAccount.md)

[Set-AzStorageAccount](./Set-AzStorageAccount.md)
