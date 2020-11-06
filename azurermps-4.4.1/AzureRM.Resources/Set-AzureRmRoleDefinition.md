---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: 9f5927905e492fd93998e12f97a97a0380755905
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430663"
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
Ação é opcional.

Veja a seguir um exemplo de definição de função de JSON atualizado para Set-AzureRmRoleDefinition

{"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "nome": "função Updated", "Descrição": "pode monitorar todos os recursos e iniciar e reiniciar máquinas virtuais", "ações": \[ "*/Read", "Microsoft. ClassicCompute/VirtualMachines/Restart/Action", "Microsoft. ClassicCompute/VirtualMachines/Start/Action" \] "AssignableScopes": \[ "/subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f" \] }

## EXEMPLOS

### Atualização--------------------------usando PSRoleDefinitionObject--------------------------
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/eb910d4f-edbf-429b-94F6-d76bae7ff401", "/subscriptions/a846d197-5eac-45c7-b885-a6227fe6d388")

          PS C:\> New-AzureRmRoleDefinition -Role $roleDef
```

### --------------------------Criar usando o arquivo JSON--------------------------
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## OS

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### PSRoleDefinition
O parâmetro ' role ' aceita o valor do tipo ' PSRoleDefinition ' da pipeline

## EXIBE

### Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition

## INFORMA
Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação

## LINKS RELACIONADOS

[Get-AzureRmProviderOperation](./Get-AzureRmProviderOperation.md)

[Get-AzureRmRoleDefinition](./Get-AzureRmRoleDefinition.md)

[New-AzureRmRoleDefinition](./New-AzureRmRoleDefinition.md)

[Remove-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)

