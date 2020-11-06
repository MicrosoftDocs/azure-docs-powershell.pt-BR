---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
ms.openlocfilehash: c1850cdc410df064a97950bb38f3734657649467
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432903"
---
# Get-AzureRmRoleDefinition

## Sinopse
Lista todas as funções RBAC do Azure que estão disponíveis para atribuição.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### RoleDefinitionNameParameterSet
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionIdParameterSet
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### RoleDefinitionCustomParameterSet
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
Use o comando Get-AzureRmRoleDefinition com um nome de função específico para exibir os detalhes.
Para inspecionar as operações individuais às quais uma função concede acesso, examine as propriedades Actions e não-Actions da função.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

Obter a definição da função do leitor

### Exemplo 2
```
PS C:\> Get-AzureRmRoleDefinition
```

Lista todas as definições de função RBAC

## OS

### -AtScopeAndBelow
Se especificado, exibe todas as definições de função.

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionNameParameterSet, RoleDefinitionCustomParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Personalizado
Se especificado, exibe somente as funções criadas personalizadas no diretório.

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
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

### -ID
ID da definição da função.

```yaml
Type: Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Nome da definição de função.
Por exemplo, leitor, colaborador, colaborador da máquina virtual.

```yaml
Type: String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Escopo
Escopo da definição de função.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### String
O parâmetro ' Scope ' aceita o valor do tipo ' String ' do pipeline

## EXIBE

### System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition]

## INFORMA
Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação

## LINKS RELACIONADOS

[New-AzureRmRoleAssignment](./New-AzureRmRoleAssignment.md)

[Get-AzureRmRoleAssignment](./Get-AzureRmRoleAssignment.md)

[New-AzureRmRoleDefinition](./New-AzureRmRoleDefinition.md)

[Remove-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)

