---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: cf70191c47f3778268b0087ea542a6812155ebbb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786137"
---
# Remove-AzureRmVMAEMExtension

## Sinopse
Remove a extensão do AEM de uma máquina virtual.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmVMAEMExtension** remove a extensão do Azure Enhanced Monitoring (AEM) de uma máquina virtual.

## EXEMPLOS

### Exemplo 1: remover a extensão do AEM
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

Esse comando Remove a extensão do AEM para a máquina virtual nomeada contoso-Server.

## OS

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
Especifica o nome da máquina virtual a partir da qual esse cmdlet Remove a extensão do AEM.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OSType
Especifica o tipo de sistema operacional do disco do sistema operacional.
Se o disco do sistema operacional não tiver um tipo, você deve especificar esse parâmetro.
Os valores aceitáveis para esse parâmetro são: Windows e Linux.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos de uma máquina virtual.
Esse cmdlet Remove a extensão do AEM da máquina virtual.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Especifica o nome de uma máquina virtual.
Esse cmdlet Remove a extensão do AEM para a máquina virtual que esse parâmetro especifica.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVMAEMExtension](./Get-AzureRmVMAEMExtension.md)

[Set-AzureRmVMAEMExtension](./Set-AzureRmVMAEMExtension.md)

[Test-AzureRmVMAEMExtension](./Test-AzureRmVMAEMExtension.md)


