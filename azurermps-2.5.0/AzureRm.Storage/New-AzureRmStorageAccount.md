---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccount
schema: 2.0.0
ms.openlocfilehash: 83afe8e0857ec401af213f029a9af0cef7321416
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785293"
---
# New-AzureRmStorageAccount

## Sinopse
Cria uma conta de armazenamento.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>]
 [-UseSubDomain <Boolean>] [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmStorageAccount** cria uma conta de armazenamento do Azure.

## EXEMPLOS

### Exemplo 1: criar uma conta de armazenamento
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

Esse comando cria uma conta de armazenamento para o nome do grupo de recursos MyResource.

### Exemplo 2: criar uma conta de armazenamento blob com BlobStorage Kind e Hot AccessTier
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

Esse comando cria uma conta de armazenamento BLOB que tem o tipo BlobStorage e Hot AccessTier

### Exemplo 3: criar uma conta de armazenamento com o tipo StorageV2 e gerar e atribuir uma identidade para o repositório de senhas do Azure.
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

Esse comando cria uma conta de armazenamento com o tipo StorageV2.  Ele também gera e atribui uma identidade que pode ser usada para gerenciar as chaves de conta por meio do Azure keyvault.

### Exemplo 4: criar uma conta de armazenamento com o NetworkRuleSet da JSON
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

Esse comando cria uma conta de armazenamento que tem uma propriedade NetworkRuleSet do JSON

## OS

### -AccessTier
Especifica a camada de acesso da conta de armazenamento que este cmdlet cria.
Os valores aceitáveis para esse parâmetro são: quente e legal.
Se você especificar um valor de BlobStorage para o parâmetro *Kind* , você deve especificar um valor para o parâmetro *AccessTier* . Se você especificar um valor de armazenamento para esse parâmetro de *tipo* , não especifique o parâmetro *AccessTier* .

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

### -AsJob
Executar o cmdlet em segundo plano

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
Gerar e atribuir uma nova identidade de conta de armazenamento para esta conta de armazenamento para uso com serviços de gerenciamento de chaves como o repositório de chaves do Azure.

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
O valor padrão é armazenamento.

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
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHttpsTrafficOnly
Indica se a conta de armazenamento habilita ou não somente o tráfego HTTPS.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kind
Especifica o tipo de conta de armazenamento que este cmdlet cria.
Os valores aceitáveis para esse parâmetro são:
- SPS. Conta de armazenamento de finalidade geral que dá suporte ao armazenamento de BLOBs, tabelas, filas, arquivos e discos.
- StorageV2. Conta de armazenamento do GPv2 (general purpose Version 2) que oferece suporte a BLOBs, tabelas, filas, arquivos e discos, com recursos avançados, como hierarquização de dados.
- BlobStorage. Conta de armazenamento de BLOB que dá suporte somente ao armazenamento de BLOBs.
O valor padrão é armazenamento.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Local
Especifica o local da conta de armazenamento a ser criada.

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

### -Nome
Especifica o nome da conta de armazenamento a ser criada.

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
NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como os serviços permitidos para ignorar as regras e como lidar com as solicitações que não correspondem a nenhuma das regras definidas.

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

### -ResourceGroupName
Especifica o nome do grupo de recursos no qual a conta de armazenamento será adicionada.

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

### -SkuName
Especifica o nome do SKU da conta de armazenamento que este cmdlet cria.
Os valores aceitáveis para esse parâmetro são:
- Standard_LRS. Armazenamento redundante localmente.
- Standard_ZRS. Armazenamento redundante na zona.
- Standard_GRS. Armazenamento com redundância geográfica.
- Standard_RAGRS. Acesso de leitura com armazenamento redundante geográfico.
- Premium_LRS. Premium-armazenamento redundante local.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Marca
Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor. Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}

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
Indica se a validação de CName indireto deve ser habilitada.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### System. Boolean

## EXIBE

### Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmStorageAccount](./Get-AzureRmStorageAccount.md)

[Remove-AzureRmStorageAccount](./Remove-AzureRmStorageAccount.md)

[Set-AzureRmStorageAccount](./Set-AzureRmStorageAccount.md)
