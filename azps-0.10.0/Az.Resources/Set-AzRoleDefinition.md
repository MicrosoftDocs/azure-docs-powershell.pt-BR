---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: 79ff5a54da704e66895e280c8a2e8a93731d2083
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776310"
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
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Set-AzRoleDefinition atualiza uma função personalizada existente no controle de acesso do Azure Role-Based.
Forneça a definição de função atualizada como uma entrada para o comando como um arquivo JSON ou um objeto PSRoleDefinition.
A definição de função para a função personalizada atualizada deve conter a ID e todas as outras propriedades necessárias da função, mesmo que elas não sejam atualizadas: DisplayName, Description, Actions, AssignableScopes.
Não agir, dataactions, NotDataActions são opcionais.
Veja a seguir um exemplo de definição de função em JSON para Set-AzRoleDefinition {"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "nome": "função Updated", "Descrição": " \[ *Microsoft. ClassicCompute/VirtualMachines/Restart/Action", "/Read", "Microsoft.//Restart/Action", "Microsoft. ClassicCompute/VirtualMachines/Start/Action" \] , "isactions": \[ "* /Write" \] , "dataactions": \[ "Microsoft. Storage/storageAccounts/blobservices/containers/BLOBs/ \] \[ contêineres/BLOBs/gravação" \] , "Microsoft. Storage/NotDataActions/blobservices/contêineres/BLOBs/gravação \[ \]

## EXEMPLOS

### Atualizar usando PSRoleDefinitionObject
```
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### Criar usando um arquivo JSON
```
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition
Parâmetros: Role (ByValue)

## EXIBE

### Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition

## INFORMA
Palavras-chave: Azure, AZ, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação

## LINKS RELACIONADOS

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[New-AzRoleDefinition](./New-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

