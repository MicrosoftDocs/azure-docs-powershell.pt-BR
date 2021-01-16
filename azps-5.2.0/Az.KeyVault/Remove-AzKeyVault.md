---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 69a1155b99d054699c41cc0b26cd78ef4445f931
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259153"
---
# Remove-AzKeyVault

## Sinopse
Exclui um cofre de chaves.

## SYNTAX

### ByAvailableVault (padrão)
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDeletedVault
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectByAvailableVault
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectByDeletedVault
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdByAvailableVault
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdByDeletedVault
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzKeyVault** exclui o cofre de chaves especificado.
Ele também exclui todas as chaves e segredos contidos nessa instância.
Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet, você deve fazê-lo para melhorar o desempenho.

## EXEMPLOS

### Exemplo 1: remover um cofre de chaves
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

Esse comando Remove o cofre de chaves denominado Contoso03Vault da sua assinatura atual.

### Exemplo 2: remover um cofre de chaves de um grupo de recursos especificado
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

Esse comando Remove o cofre de chaves chamado Contoso03Vault do grupo de recursos nomeado.
Se você não especificar o nome do grupo de recursos, o cmdlet pesquisará o cofre de chaves nomeados para excluir na sua assinatura atual.

### Exemplo 3: remover um HSM gerenciado
```powershell
PS C:\>  Remove-AzKeyVault -Name "testManagedHsm" -Hsm -PassThru

True
```

Esse comando Remove o HSM gerenciado chamado testManagedHsm da sua assinatura atual.

## OS

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -Force
Indica que o cmdlet não solicita confirmação.
Por padrão, esse cmdlet solicita que você confirme que deseja excluir o cofre de chaves.

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
Objeto do cofre de chaves a ser excluído.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Inremovestate
Remova permanentemente o cofre excluído anteriormente.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Local
O local do cofre excluído.

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ResourceIdByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Esse cmdlet não retorna um objeto por padrão. Se essa opção for especificada, retornará true se for bem-sucedida.

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
Especifica o nome de um grupo de recursos.

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID do recurso do keyvault.

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Cofrename
Especifica o nome do cofre de chaves a ser removido.

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases: Name

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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVault

### System. String

## EXIBE

### System. Boolean

## INFORMA

## LINKS RELACIONADOS

[Get-AzKeyVault](./Get-AzKeyVault.md)

[New-AzKeyVault](./New-AzKeyVault.md)
