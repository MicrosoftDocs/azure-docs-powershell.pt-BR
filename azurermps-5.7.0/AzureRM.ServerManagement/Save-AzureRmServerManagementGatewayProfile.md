---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: ECF85C07-2C9E-487D-A2ED-77875C380244
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/save-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 8dd9aeaaf987fba155ca80b0c8739d44c80945e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428770"
---
# Save-AzureRmServerManagementGatewayProfile

## Sinopse
Baixa o perfil de um gateway de gerenciamento de servidor e salva-o em um arquivo local.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ByName
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-ResourceGroupName] <String>
 [-GatewayName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-Gateway] <Gateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Save-AzureRmServerManagementGatewayProfile** faz o download do perfil de um gateway de gerenciamento do servidor do Azure e o armazena em um arquivo local.

## EXEMPLOS

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

### -Gateway
Especifica o gateway para o qual esse cmdlet obtém o perfil.

Pode ser usado em vez de especificar ResourceGroupName e GATEWAYNAME

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -GATEWAYNAME
Especifica o nome do gateway para o qual esse cmdlet obtém o perfil.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputFile
Especifica o arquivo local no qual os dados do perfil são salvos.

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos ao qual o gateway pertence.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Gateway
O parâmetro ' gateway ' aceita o valor do tipo ' gateway ' da pipeline

## EXIBE

### System. IO. FileInfo

## INFORMA

## LINKS RELACIONADOS

[Install-AzureRmServerManagementGatewayProfile](./Install-AzureRmServerManagementGatewayProfile.md)

[Reset-AzureRmServerManagementGatewayProfile](./Reset-AzureRmServerManagementGatewayProfile.md)


