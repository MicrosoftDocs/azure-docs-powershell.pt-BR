---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 047d0c7c9b141f10ee3f1be2ba1e739960f2e5bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259307"
---
# Wait-AzDataLakeAnalyticsJob

## Sinopse
Aguarda um trabalho ser concluído.

## SYNTAX

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Wait-AzDataLakeAnalyticsJob** aguarda a conclusão de um trabalho do Azure data Lake Analytics.

## EXEMPLOS

### Exemplo 1: Aguarde a conclusão do trabalho
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

O comando a seguir aguarda o trabalho com a ID especificada ser concluída.

## OS

### -Conta
Especifica o nome da conta do data Lake Analytics.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -JobId
Especifica a ID do trabalho a ser aguardado.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -TimeoutInSeconds
Especifica o número de segundos a aguardar antes de sair da operação de espera.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WaitIntervalInSeconds
Especifique o número de segundos que decorrem entre cada verificação do estado do trabalho.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### System. GUID

### System. Int32

## EXIBE

### Microsoft. Azure. Management. datalake. Analytics. Models. JobInformation

## INFORMA

## LINKS RELACIONADOS

[Get-AzDataLakeAnalyticsJob](./Get-AzDataLakeAnalyticsJob.md)

[Parar-AzDataLakeAnalyticsJob](./Stop-AzDataLakeAnalyticsJob.md)

[Enviar-AzDataLakeAnalyticsJob](./Submit-AzDataLakeAnalyticsJob.md)


