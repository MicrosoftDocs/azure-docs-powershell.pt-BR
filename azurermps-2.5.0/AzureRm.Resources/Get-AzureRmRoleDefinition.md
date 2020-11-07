---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 219ff64309cc11fd5e65d614f67d2d531737c8b1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786062"
---
# Get-AzureRmRoleDefinition

## Sinopse
Lista todas as funções RBAC do Azure que estão disponíveis para atribuição.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### RoleDefinitionNameParameterSet
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### RoleDefinitionIdParameterSet
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### RoleDefinitionCustomParameterSet
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
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

### -Personalizado
Se especificado, exibe somente as funções criadas personalizadas no diretório.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
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
Type: System.Guid
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
Type: System.String
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
Type: System.String
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

### System. String
Parâmetros: Scope (ByValue)

### System. GUID

### System. Management. Automation. SwitchParameter

## EXIBE

### Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition

## INFORMA
Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação

## LINKS RELACIONADOS

[New-AzureRmRoleAssignment](./New-AzureRmRoleAssignment.md)

[Get-AzureRmRoleAssignment](./Get-AzureRmRoleAssignment.md)

[New-AzureRmRoleDefinition](./New-AzureRmRoleDefinition.md)

[Remove-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)

