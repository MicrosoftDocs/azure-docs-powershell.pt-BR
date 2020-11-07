---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsslbinding
schema: 2.0.0
ms.openlocfilehash: 103c5e75b433fcb585113e8ef6bc89aab1f82d7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785408"
---
# Get-AzureRmWebAppSSLBinding

## Sinopse
Obtém uma associação SSL do certificado do aplicativo Web do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Eles
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmWebAppSSLBinding** Obtém uma associação SSL (Secure Sockets Layer) para um aplicativo Web do Azure.
Associações SSL são usadas para associar um aplicativo Web a um certificado carregado.
Os aplicativos Web podem ser associados a vários certificados.

## EXEMPLOS

### Exemplo 1: obter associações SSL para um aplicativo Web
```
PS C:\>Get-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

Esse comando recupera as associações SSL para o aplicativo Web ContosoWebApp, que está associado à ContosoResourceGroup do grupo de recursos.

### Exemplo 2: usar uma referência de objeto para obter associações SSL para um aplicativo Web
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Get-AzureRmWebAppSSLBinding -WebApp $WebApp
```

Os comandos neste exemplo também obtêm associações SSL para o aplicativo Web ContosoWebApp; Nesse caso, no entanto, uma referência de objeto é usada em vez do nome do aplicativo Web e o nome do grupo de recursos associado.
Essa referência de objeto é criada pelo primeiro comando no exemplo, que usa **Get-AzureRmWebApp** para criar uma referência de objeto para o aplicativo Web chamado ContosoWebApp.
Essa referência de objeto é armazenada em uma variável chamada $WebApp.

Essa variável, e o cmdlet **Get-AzureRmWebAppSSLBinding** , são então usadas pelo segundo comando para obter as associações SSL.

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
Especifica o nome da Associação SSL.

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
Especifica o nome do grupo de recursos ao qual o certificado está atribuído.

Não é possível usar o parâmetro *ResourceGroupName* e o parâmetro *webapp* no mesmo comando.

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Especifica um slot de implantação do aplicativo Web.
Para obter um slot de implantação, use o cmdlet Get-AzureRMWebAppSlot.

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Especifica um aplicativo Web.
Para obter um aplicativo Web, use o cmdlet Get-AzureRmWebApp.

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppname
Especifica o nome do aplicativo Web do qual este cmdlet obtém associações SSL.

Não é possível usar o parâmetro *webappname* e o parâmetro *webapp* no mesmo comando.

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Instalação
O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmWebAppSSLBinding](./New-AzureRmWebAppSSLBinding.md)

[Remove-AzureRmWebAppSSLBinding](./Remove-AzureRmWebAppSSLBinding.md)

[Get-AzureRmWebApp](./Get-AzureRmWebApp.md)


