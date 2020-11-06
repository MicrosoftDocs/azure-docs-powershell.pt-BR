---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 7b04fc95af1ee340e87fa5ed46cbba9f1956d9e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425684"
---
# New-AzureRmDeploymentManagerStep

## Sinopse
Cria uma nova etapa de implantação.

## SYNTAX

```
New-AzureRmDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -Duration <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmDeploymentManagerStep** cria uma etapa de implantação que pode ser referenciada em implementações.
Especifique o *nome* , *ResourceGroupName* e propriedades necessárias.

Você pode modificar o objeto retornado localmente e, em seguida, aplicar as alterações à etapa usando o cmdlet Set-AzureRmDeploymentManagerStep.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

Cria uma etapa no ContosoResourceGroup com o nome ContosoService1WaitStep no centro dos EUA como o local do recurso. A Propriedade Duration fornece a duração que a distribuição aguardará antes de executar a próxima etapa.

## OS

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

### -Duração
A duração a ser esperada no formato ISO 8601.
Por exemplo: PT30M, PT1H

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Local
O local do recurso.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
O nome da etapa.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O grupo de recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Marca
Uma tabela de hash que representa as marcas de recursos.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.
Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. Collections. Hashtable

## EXIBE

### Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource

## INFORMA

## LINKS RELACIONADOS
