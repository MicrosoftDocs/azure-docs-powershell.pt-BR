---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: a0d79aa0d1699f6e6645f86475732c235447342f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775792"
---
# Get-AzKeyVaultKey

## Sinopse
Obtém chaves do cofre de chaves.

## SYNTAX

### ByVaultName (padrão)
```
Get-AzKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyName
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyVersions
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedKey
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzKeyVaultKey** Obtém as chaves do cofre de chaves do Azure.
Esse cmdlet obtém um determinado **Microsoft. Azure. Commands. subvault. Models. keybundle** ou uma lista de todos os objetos **keybundle** em um cofre de chaves ou por versão.

## EXEMPLOS

### Exemplo 1: obter todas as chaves em um cofre de chaves
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso'
```

Esse comando obtém todas as chaves no cofre de chaves chamado contoso.

### Exemplo 2: obter a versão atual de uma chave
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

Esse comando obtém a versão atual da chave chamada ITPfx no cofre de chaves chamado contoso.

### Exemplo 3: obter todas as versões de uma chave
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

Este comando obtém todas as versões a chave chamada ITPfx na chave vaultnamed contoso.

### Exemplo 4: obter uma versão específica de uma chave
```
PS C:\>$Key = Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

Esse comando obtém uma versão específica da chave chamada ITPfx no cofre de chaves chamado contoso.
Depois de executar esse comando, você pode inspecionar várias propriedades da chave navegando no objeto $Key.

### Exemplo 5: obter todas as chaves que foram excluídas, mas não eliminadas para este cofre de chaves.
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

Esse comando obtém todas as chaves que foram excluídas anteriormente, mas não foram limpas, no cofre de chaves chamado contoso.

### Exemplo 6: Obtém a chave ITPfx que foi excluída, mas não é eliminada para este cofre de chaves.
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

Esse comando obtém a chave ITPfx que foi excluída anteriormente, mas não foi eliminada, no cofre de chaves chamado contoso.
Esse comando retornará metadados como a data de exclusão e a data de descarte programada dessa chave excluída.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeVersions
Indica que esse cmdlet obtém todas as versões de uma chave.
A versão atual de uma chave é a primeira na lista.
Se você especificar esse parâmetro, também deverá especificar o *nome* e os parâmetros de *cofrename* .

Se você não especificar o parâmetro *IncludeVersions* , esse cmdlet obtém a versão atual da chave com o *nome* especificado.

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inremovestate
Especifica se as chaves excluídas anteriormente devem ser mostradas na saída

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome do pacote de chaves a obter.

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Cofrename
Especifica o nome do cofre de chaves do qual este cmdlet obtém chaves.
Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um cofre de chaves com base no nome especificado por esse parâmetro e no ambiente selecionado.

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

### -Versão
Especifica a versão da chave.
Esse cmdlet constrói o FQDN de uma chave com base no nome do cofre de chaves, no ambiente selecionado atualmente, no nome da chave e na versão de chave.

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### String

## EXIBE

### List<Microsoft. Azure. Commands. keyvault. Models. KeyIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. keybundle, List<Microsoft. Azure. Commands. keyvault. Models. DeletedKeyIdentityItem>, Microsoft. Azure. Commands. subvault. Models. DeletedKeyBundle

## INFORMA

## LINKS RELACIONADOS

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Desfazer-AzKeyVaultKeyRemoval](./Undo-AzKeyVaultKeyRemoval.md)

[Set-AzKeyVaultKeyAttribute](./Set-AzKeyVaultKeyAttribute.md)

