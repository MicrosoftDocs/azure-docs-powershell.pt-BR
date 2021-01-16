---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: e97e89c1ab7160f1eb06c9c94cd5620a48b0463e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271338"
---
# Enable-AzStorageStaticWebsite

## Sinopse
Habilite o site estático para a conta de armazenamento do Azure.

## SYNTAX

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Enable-AzStorageStaticWebsite** habilita o site estático para a conta de armazenamento do Azure.

## EXEMPLOS

### Exemplo 1: habilitar o site estático para a conta de armazenamento do Azure
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

Esse comando habilita o site estático para a conta de armazenamento do Azure.

## OS

### -Contexto
Objeto de contexto de armazenamento do Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ErrorDocument404Path
O caminho para o documento de erro que deve ser mostrado quando um 404 é emitido (ou seja, quando um navegador solicita uma página que não existe.)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IndexDocument
O nome do documento de índice em cada diretório.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Exiba a configuração estática de site em Serviceproperties.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext

## EXIBE

### Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSStaticWebsiteProperties

## INFORMA

## LINKS RELACIONADOS
