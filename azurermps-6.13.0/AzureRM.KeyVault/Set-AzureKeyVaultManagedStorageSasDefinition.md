---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: a71aed4703158c68d3b156ff1e37d438e5413782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429522"
---
# Set-AzureKeyVaultManagedStorageSasDefinition

## Sinopse
Define uma definição de assinatura de acesso compartilhado (SAS) com o cofre de chaves para uma determinada conta de armazenamento do Azure, gerenciada pela chave.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Padrão (padrão)
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Set-AzureKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
Define uma definição de assinatura de acesso compartilhado (SAS) com uma determinada conta de armazenamento do Azure do cofre de chaves. Isso também define um segredo que pode ser usado para obter o token SAS por essa definição de SAS.
O token SAS é gerado usando esses parâmetros e a chave ativa da conta de armazenamento gerenciada do cofre do repositório de chaves.

## EXEMPLOS

### Exemplo 1: definir uma definição de tipo de conta SAS e obter um token SAS atual baseado nela
```powershell
PS C:\> $sa = Get-AzureRmStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzureRmKeyVault -VaultName mykv
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod 180
PS C:\> $sctx = New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzureStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzureKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

Define uma definição de SAS de conta ' contasas ' em um keyvault-conta de armazenamento gerenciado ' Mysa ' no cofre ' mykv '. Especificamente, a sequência acima executa o seguinte:
  - Obtém uma conta de armazenamento (pré-existente)
  - Obtém um cofre de chaves (pré-existente)
  - Adiciona uma conta de armazenamento gerenciada do keyvault ao cofre, definindo key1 como a chave ativa e com um período de regeneração de 180 dias
  - define um contexto de armazenamento para a conta de armazenamento especificada, com a key1
  - Cria um token SAS de conta para blob de serviços, arquivo, tabela e fila, para o serviço de tipos de recursos, contêiner e objeto, com todas as permissões, via HTTPS e com as datas de início e término especificadas
  - define uma definição de SAS de armazenamento gerenciado no cofre no cofre, com o URI de modelo como o token SAS criado acima, do tipo SAS ' conta ' e válido por 30 dias
  - Recupera o token de acesso real do segredo do keyvault correspondente à definição de SAS

## OS

### -AccountName
Nome da conta de armazenamento gerenciado do cofre de chaves. O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -Disable
Desabilita o uso da definição de SAS para a geração de token SAS.

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

### -InputObject
Objeto ManagedStorageAccount.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome da definição de SAS de armazenamento. O cmdlet constrói o FQDN de uma definição de SAS de armazenamento do nome do cofre, ambiente selecionado atualmente, nome da conta de armazenamento e nome da definição da SAS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasType
Tipo de SAS de armazenamento.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Marca
Pares de valores chave na forma de uma tabela de hash. Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}

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

### -TemplateUri
URI do modelo de definição de SAS de armazenamento.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValidityPeriod
Período de validade que será usado para definir o tempo de expiração do token SAS no momento da geração

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Cofrename
Nome do cofre.
O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem
Parâmetros: inputobject (ByValue)

## EXIBE

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageSasDefinition

## INFORMA

## LINKS RELACIONADOS

[Azureâ € ‹ RM. â € ‹ Keyâ € ‹ Vault](/powershell/module/azurerm.keyvault/)
