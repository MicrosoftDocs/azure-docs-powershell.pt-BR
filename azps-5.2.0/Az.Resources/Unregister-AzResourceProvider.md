---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: be32315e62770de7075f89fc1390063d4c516211
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260217"
---
# Unregister-AzResourceProvider

## Sinopse
Cancela o registro de um provedor de recursos.

## SYNTAX

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Unregister-AzResourceProvider** cancela o registro de um provedor de recursos do Azure.

## EXEMPLOS

### Exemplo 1: cancelar o registro do provedor de recursos com ProviderNamespace

```powershell
PS C:\>Unregister-AzResourceProvider -ProviderNamespace "Microsoft.support"
```

Esse comando cancela o registro do provedor de recursos "Microsoft. support".

## OS

### -ApiVersion
Especifica a versão da API que é suportada pelo provedor de recursos.
Você pode especificar uma versão diferente da versão padrão.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.

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

### -ProviderNamespace
Especifica o namespace do provedor de recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceProvider

## INFORMA

## LINKS RELACIONADOS

[Get-AzResourceProvider](./Get-AzResourceProvider.md)

[Register-AzResourceProvider](./Register-AzResourceProvider.md)


