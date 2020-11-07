---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 6d1a891dbef40a6556e3a8f2ca122f2c3b46cb28
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785370"
---
# New-AzureRmContainerService

## Sinopse
Cria um serviço de contêiner.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmContainerService** cria um serviço de contêiner.
Especifique um objeto de serviço de contêiner que você possa criar usando o cmdlet New-AzureRmContainerServiceConfig.

## EXEMPLOS

### Exemplo 1: criar um serviço de contêiner
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

O primeiro comando cria um grupo de recursos chamado ResourceGroup17 no local especificado.
Para obter mais informações, consulte o cmdlet New-AzureRmResourceGroup.

O segundo comando cria um contêiner e, em seguida, armazena-o na variável $Container.
Para obter mais informações, consulte o cmdlet New-AzureRmContainerServiceConfig.

O comando final cria um serviço de contêiner para o contêiner armazenado em $Container.
O serviço é chamado csResourceGroup17.

## OS

### -AsJob
RRun cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerService
Especifica um objeto de serviço de contêiner que contém as propriedades do novo serviço.
Para obter um objeto **ContainerService** , use o cmdlet New-AzureRmContainerServiceConfig.

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -Nome
Especifica o nome do serviço de contêiner que este cmdlet cria.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o grupo de recursos no qual esse cmdlet implanta o serviço de contêiner.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
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

O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### ContainerService
O parâmetro ' ContainerService ' aceita o valor do tipo ' ContainerService ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmContainerService](./Get-AzureRmContainerService.md)

[New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md)

[Remove-AzureRmContainerService](./Remove-AzureRmContainerService.md)

[Update-AzureRmContainerService](./Update-AzureRmContainerService.md)


