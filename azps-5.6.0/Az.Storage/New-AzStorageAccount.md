---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0a5ccfaec396f4dc79c877da38112a5bfa575e09
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890694"
---
# New-AzStorageAccount

## SYNOPSIS
Cria uma conta de armazenamento.

## SINTAXE

### AzureActiveDirectoryDomainServicesForFile (Padrão)
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
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
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **New-AzStorageAccount** cria uma conta de Armazenamento do Azure.

## EXEMPLOS

### Exemplo 1: Criar uma conta de armazenamento
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

Este comando cria uma conta de armazenamento para o nome do grupo de recursos MyResourceGroup.

### Exemplo 2: Criar uma conta de Armazenamento de Blob com o Tipo blobStorage e o AccessTier quente
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

Este comando cria uma conta de Armazenamento blob que com BlobStorage Kind e Hot AccessTier

### Exemplo 3: Criar uma conta de armazenamento com Kind StorageV2 e Gerar e Atribuir uma identidade para o Azure KeyVault.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

Este comando cria uma conta de armazenamento com Kind StorageV2.  Ele também gera e atribui uma identidade que pode ser usada para gerenciar chaves de conta por meio do Azure KeyVault.

### Exemplo 4: Criar uma conta de armazenamento com NetworkRuleSet a partir de JSON
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

Este comando cria uma conta de armazenamento que tem a propriedade NetworkRuleSet do JSON

### Exemplo 5: Criar uma conta de armazenamento com Namespace hierárquico habilitado.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

Este comando cria uma conta de Armazenamento com Namespace Hierárquico habilitado.

### Exemplo 6: criar uma conta de armazenamento com a autenticação AAD DS de arquivos do Azure e habilitar o compartilhamento de arquivos grande.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

Este comando cria uma conta de armazenamento com a Autenticação AAD DS de Arquivos do Azure e habilita o compartilhamento de arquivos grande.

### Exemplo 7: Criar uma conta de armazenamento com a autenticação de serviço de domínio active directory arquivos.
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

Este comando cria uma conta de armazenamento com autenticação de serviço de domínio active directory de arquivos reencíveis.

### Exemplo 8: Criar uma conta de armazenamento com o Serviço de Fila e Tabela use a chave de criptografia com escopo de conta e exigir criptografia de infraestrutura.
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

Este comando cria uma conta de Armazenamento com o Serviço de Fila e Tabela, usa a chave de criptografia com escopo de conta e Exige Criptografia de Infraestrutura, portanto, Queue e Table usarão a mesma chave de criptografia com Blob e serviço de arquivo, e o serviço aplicará uma camada secundária de criptografia com chaves gerenciadas da plataforma para dados em repouso.
Em seguida, obter as propriedades da conta de armazenamento e exibir o tipo de chave de criptografia do Queue and Table Service e o valor RequireInfrastructureEncryption.

### Exemplo 9: Criar conta MinimumTlsVersion e AllowBlobPublicAccess e desabilitar o SharedKey Access
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false -AllowSharedKeyAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False

PS C:\> $a.AllowSharedKeyAccess
False
```

O comando cria conta com MinimumTlsVersion, AllowBlobPublicAccess e desabilita o acesso SharedKey à conta e mostra as 3 propriedades da conta criada 

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

Este comando cria uma conta de armazenamento com a configuração RoutingPreference: PublishMicrosoftEndpoint e PublishInternetEndpoint como true e RoutingChoice como MicrosoftRouting.

## PARÂMETROS

### -AccessTier
Especifica a camada de acesso da conta de armazenamento que este cmdlet cria.
Os valores aceitáveis para este parâmetro são: Hot e Cool.
Se você especificar um valor blobStorage para o parâmetro *Kind,* deverá especificar um valor para o *parâmetro AccessTier.* Se você especificar um valor de Armazenamento para este *parâmetro Kind,* não especifique o *parâmetro AccessTier.*

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
Especifica o identificador de segurança (SID) para Armazenamento do Azure. Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile for definido como true.

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
Especifica o GUID do domínio. Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile for definido como true.

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
Especifica o domínio principal para o que o servidor DNS do AD é autoritativo. Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile for definido como true.

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
Especifica o identificador de segurança (SID). Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile for definido como true.

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
Especifica a floresta do Active Directory a ser obter. Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile for definido como true.

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
Especifica o nome de domínio NetBIOS. Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile for definido como true.

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

### -AllowBlobPublicAccess
Permitir acesso público a todos os blobs ou contêineres na conta de armazenamento. A interpretação padrão é verdadeira para essa propriedade.

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

### -AllowSharedKeyAccess
Indica se a conta de armazenamento permite que as solicitações sejam autorizadas com a chave de acesso à conta por meio da Chave Compartilhada. Se false, todas as solicitações, incluindo assinaturas de acesso compartilhado, devem ser autorizadas com o Azure Active Directory (Azure AD). O valor padrão é nulo, que é equivalente a true.

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
Gere e atribua uma nova Identidade de conta de armazenamento para essa conta de Armazenamento para uso com serviços de gerenciamento de chaves, como o Azure KeyVault.

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
Especifica o nome do domínio personalizado da conta de armazenamento.
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
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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
Habilitar a Autenticação de Serviço de Domínio do Active Directory arquivos do Azure para a conta de armazenamento.

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
Habilitar a Autenticação de Serviço de Domínio do Azure Arquivos do Azure Active Directory para a conta de armazenamento.

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
Indica se a conta de armazenamento habilita ou não Namespace Hierárquico.

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
Indica se a conta de armazenamento só habilita o tráfego HTTPS ou não.

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
Indica se a conta de armazenamento pode ou não suportar compartilhamentos de arquivos grandes com mais de 5 TiB. Depois que a conta for habilitada, o recurso não poderá ser desabilitado. Atualmente, só há suporte para tipos de replicação LRS e ZRS, portanto, as conversões de contas em contas redundantes geográficas não seriam possíveis. Saiba mais em https://go.microsoft.com/fwlink/?linkid=2086047

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
De definir o Encryption KeyType for Queue. O valor padrão é Service.
-Conta: a fila será criptografada com chave de criptografia com escopo de conta. -Service: a fila sempre será criptografada com Service-Managed chaves. 

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
De definir o Encryption KeyType for Table. O valor padrão é Service.
- Conta: a tabela será criptografada com chave de criptografia com escopo de conta. 
- Serviço: a tabela sempre será criptografada com Service-Managed chaves. 

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

### -Kind
Especifica o tipo de conta de Armazenamento que esse cmdlet cria.
Os valores aceitáveis para este parâmetro são:
- Armazenamento. Conta de armazenamento de finalidade geral que oferece suporte ao armazenamento de Blobs, Tabelas, Filas, Arquivos e Discos.
- StorageV2. Conta de armazenamento de finalidade geral versão 2 (GPv2) que dá suporte a Blobs, Tabelas, Filas, Arquivos e Discos, com recursos avançados, como a camada de dados.
- BlobStorage. Conta de Armazenamento de Blob que dá suporte apenas ao armazenamento de Blobs.
- BlockBlobStorage. Blob Storage account which supports storage of Block Blobs only.
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

### -Location
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
A versão TLS mínima a ser permitida em solicitações de armazenamento. A interpretação padrão é TLS 1.0 para essa propriedade.

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

### -Name
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
NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como serviços permitidos para ignorar as regras e como lidar com solicitações que não corresponderem a nenhuma das regras definidas.

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

### -RequireInfrastructureEncryption
O serviço aplicará uma camada secundária de criptografia com chaves gerenciadas da plataforma para dados em repouso.

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

### -ResourceGroupName
Especifica o nome do grupo de recursos no qual adicionar a conta de armazenamento.

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
A Opção de Roteamento define o tipo de roteamento de rede optado pelo usuário. Os valores possíveis incluem: 'MicrosoftRouting', 'InternetRouting'

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
Especifica o nome SKU da conta de armazenamento que este cmdlet cria.
Os valores aceitáveis para este parâmetro são:
- Standard_LRS. Armazenamento localmente redundante.
- Standard_ZRS. Armazenamento redundante de zona.
- Standard_GRS. Armazenamento geo-redundante.
- Standard_RAGRS. Ler o armazenamento geo-redundante de acesso.
- Premium_LRS. Armazenamento localmente redundante premium.
- Premium_ZRS. Armazenamento redundante de zona premium.
- Standard_GZRS - Armazenamento redundante de zona geo-redundante.
- Standard_RAGZRS - Ler o armazenamento redundante de zona de acesso geo-redundante.

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
Pares de valores-chave na forma de um conjunto de tabelas de hash como marcas no servidor. Por exemplo: @{key0="value0";key1=$null;key2="value2"}

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

## INPUTS

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

## NOTES

## LINKS RELACIONADOS

[Get-AzStorageAccount](./Get-AzStorageAccount.md)

[Remove-AzStorageAccount](./Remove-AzStorageAccount.md)

[Set-AzStorageAccount](./Set-AzStorageAccount.md)
