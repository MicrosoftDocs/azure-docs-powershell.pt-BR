---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/test-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: ae4a6d72fcb44406773234b6de55cec7ccef8eb9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786548"
---
# Test-AzureRmVMAEMExtension

## Sinopse
Verifica a configuração da extensão do AEM.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Test-AzureRmVMAEMExtension** verifica a configuração da extensão do Azure Enhanced Monitoring (AEM).
A extensão do AEM coleta os dados de desempenho.
Este cmdlet verifica se os dados de desempenho estão disponíveis.

## EXEMPLOS

### Exemplo 1: verificar a configuração da extensão do AEM
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

Esse comando verifica a configuração da extensão do AEM para a máquina virtual nomeada contoso-Server.

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

### -OSType
Especifica o tipo de sistema operacional do disco do sistema operacional.
Se o disco do sistema operacional não tiver um tipo, você deve especificar esse parâmetro.
Os valores aceitáveis para esse parâmetro são: Windows e Linux.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos da máquina virtual que este cmdlet verifica.

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

### -SkipStorageCheck
Indica que esse cmdlet ignora a verificação de configuração de armazenamento.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
Especifica o nome de uma máquina virtual.
Esse cmdlet testa a extensão do AEM para a máquina virtual que esse parâmetro especifica.

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

### -WaitTimeInMinutes
Especifica um período de tempo limite, em minutos, para a verificação da configuração de armazenamento.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Extension. AEM. AEMTestResult

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVMAEMExtension](./Get-AzureRmVMAEMExtension.md)

[Remove-AzureRmVMAEMExtension](./Remove-AzureRmVMAEMExtension.md)

[Set-AzureRmVMAEMExtension](./Set-AzureRmVMAEMExtension.md)


