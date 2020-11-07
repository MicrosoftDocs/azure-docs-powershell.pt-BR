---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 51e7b941e5dbb4d07b48444196f6e3d3aa830452
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785933"
---
# Get-AzureKeyVaultManagedStorageAccount

## Sinopse
Obtém contas de armazenamento do Azure gerenciadas do Key Vault.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ByVaultName (padrão)
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByAccountName
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
Obtém uma conta de armazenamento gerenciada do Key Vault, se o nome da conta for especificado e as chaves da conta forem gerenciadas pelo cofre especificado. Se o nome da conta não for especificado, todas as contas cujas chaves são gerenciadas pelo cofre especificado são listadas.

## EXEMPLOS

### Exemplo 1: lista todas as contas de armazenamento gerenciado do cofre de chaves
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault'
```

Lista todas as contas cujas chaves são gerenciadas pelo cofre ' myvault '

### Exemplo 2: obter uma conta de armazenamento gerenciado do Key Vault
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

Obtém os detalhes da conta de armazenamento gerenciado do Key Vault de ' mystorageaccount ' se suas chaves forem gerenciadas pelo cofre ' myvault '

## OS

### -AccountName
Nome da conta de armazenamento gerenciado do cofre de chaves. O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.

```yaml
Type: String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Cofrename
Nome do cofre.
O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount, Microsoft. Azure. Commands. keyvault, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]
Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount

## INFORMA

## LINKS RELACIONADOS

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

