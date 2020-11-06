---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 131fec8efa9075640d367726e5178caa54b9402a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426407"
---
# Start-AzureRmVmss

## Sinopse
Inicia o VMSS ou um conjunto de máquinas virtuais dentro do VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Start-AzureRmVmss** inicia todas as máquinas virtuais dentro do VMSS (conjunto de dimensionamento de máquina virtual) ou um conjunto de máquinas virtuais.
Você pode usar o parâmetro *InstanceId* para selecionar um conjunto de máquinas virtuais.

## EXEMPLOS

### Exemplo 1: iniciar um conjunto específico de máquinas virtuais dentro do VMSS
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

Esse comando inicia um conjunto específico de máquinas virtuais especificadas pela matriz de cadeia de caracteres de ID de instância que pertence à VMSS chamada ContosoVMSS.

### Exemplo 2: iniciar todas as máquinas virtuais dentro do VMSS
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

Esse comando inicia todas as máquinas virtuais que pertencem ao VMSS chamado ContosoVMSS.

## OS

### -AsJob
Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.

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

### -InstanceId
Especifica, como uma matriz de cadeia de caracteres, a ID ou IDs das instâncias que o cmdlet inicia.
Por exemplo: `-InstanceId "0", "3"`

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos do VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Especifica o nome do VMSS que este cmdlet inicia nas máquinas virtuais.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
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
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### System. String []

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[New-AzureRmVmss](./New-AzureRmVmss.md)

[Remove-AzureRmVmss](./Remove-AzureRmVmss.md)

[Restart-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[Parar-AzureRmVmss](./Stop-AzureRmVmss.md)

[Update-AzureRmVmss](./Update-AzureRmVmss.md)


