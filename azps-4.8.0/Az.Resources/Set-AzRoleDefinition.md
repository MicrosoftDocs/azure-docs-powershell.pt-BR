---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: c68ad7def1b94796a020ffd29495e2b4c0b15a60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954705"
---
# Set-AzRoleDefinition

## Sinopse
Modifica uma função personalizada no Azure RBAC.
Forneça a definição de função modificada como um arquivo JSON ou como um PSRoleDefinition.
Primeiro, use o comando Get-AzRoleDefinition para recuperar a função personalizada que você deseja modificar.
Em seguida, modifique as propriedades que você deseja alterar.
Por fim, salve a definição de função usando este comando.

## SYNTAX

### InputFileParameterSet
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Set-AzRoleDefinition atualiza uma função personalizada existente no controle de acesso do Azure Role-Based.
Forneça a definição de função atualizada como uma entrada para o comando como um arquivo JSON ou um objeto PSRoleDefinition.
A definição de função para a função personalizada atualizada deve conter a ID e todas as outras propriedades necessárias da função, mesmo que elas não sejam atualizadas: DisplayName, Description, Actions, AssignableScopes.
Não agir, dataactions, NotDataActions são opcionais.
Veja a seguir um exemplo de definição de função em JSON para Set-AzRoleDefinition {"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "nome": "função Updated", "Descrição": " \[ *Microsoft. ClassicCompute/VirtualMachines/Restart/Action", "/Read", "Microsoft.//Restart/Action", "Microsoft. ClassicCompute/VirtualMachines/Start/Action" \] , "isactions": \[ "* /Write" \] , "dataactions": \[ "Microsoft. Storage/storageAccounts/blobservices/containers/BLOBs/ \] \[ contêineres/BLOBs/gravação" \] , "Microsoft. Storage/NotDataActions/blobservices/contêineres/BLOBs/gravação \[ \]

## EXEMPLOS

### Exemplo 1: atualizar usando PSRoleDefinitionObject
```powershell
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### Exemplo 2: criar usando um arquivo JSON
```powershell
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## OS

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

### -InputFile
Nome do arquivo que contém uma única definição de função JSON a ser atualizada.
Inclua apenas as propriedades que serão atualizadas no JSON.
A propriedade ID é necessária.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Função
Objeto de definição de função a ser atualizado

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition

## EXIBE

### Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition

## INFORMA
Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação

## LINKS RELACIONADOS

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[New-AzRoleDefinition](./New-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

