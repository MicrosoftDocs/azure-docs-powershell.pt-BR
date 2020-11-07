---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 6ca98bc3a459fada4c9ec7c48c216571fb038ba4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785845"
---
# Set-AzureRmRoleDefinition

## Sinopse
Modifica uma função personalizada no Azure RBAC.
Forneça a definição de função modificada como um arquivo JSON ou como um PSRoleDefinition.
Primeiro, use o comando Get-AzureRmRoleDefinition para recuperar a função personalizada que você deseja modificar.
Em seguida, modifique as propriedades que você deseja alterar.
Por fim, salve a definição de função usando este comando.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### InputFileParameterSet
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Set-AzureRmRoleDefinition atualiza uma função personalizada existente no controle de acesso do Azure Role-Based.
Forneça a definição de função atualizada como uma entrada para o comando como um arquivo JSON ou um objeto PSRoleDefinition.
A definição de função para a função personalizada atualizada deve conter a ID e todas as outras propriedades necessárias da função, mesmo que elas não sejam atualizadas: DisplayName, Description, Actions, AssignableScopes.
Não agir, dataactions, NotDataActions são opcionais.
Veja a seguir um exemplo de definição de função em JSON para Set-AzureRmRoleDefinition {"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "nome": "função Updated", "Descrição": " \[ *Microsoft. ClassicCompute/VirtualMachines/Restart/Action", "/Read", "Microsoft.//Restart/Action", "Microsoft. ClassicCompute/VirtualMachines/Start/Action" \] , "isactions": \[ "* /Write" \] , "dataactions": \[ "Microsoft. Storage/storageAccounts/blobservices/containers/BLOBs/ \] \[ contêineres/BLOBs/gravação" \] , "Microsoft. Storage/NotDataActions/blobservices/contêineres/BLOBs/gravação \[ \]

## EXEMPLOS

### Atualizar usando PSRoleDefinitionObject
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### Criar usando um arquivo JSON
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## OS

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition
Parâmetros: Role (ByValue)

## EXIBE

### Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition

## INFORMA
Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação

## LINKS RELACIONADOS

[Get-AzureRmProviderOperation](./Get-AzureRmProviderOperation.md)

[Get-AzureRmRoleDefinition](./Get-AzureRmRoleDefinition.md)

[New-AzureRmRoleDefinition](./New-AzureRmRoleDefinition.md)

[Remove-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)

