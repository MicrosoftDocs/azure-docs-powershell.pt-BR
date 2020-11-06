---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupcontainerreregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: f64453995418df572480426e7c2c63e497cf000f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432960"
---
# Enable-AzureRmBackupContainerReregistration

## Sinopse
Registra novamente um servidor para se conectar a um cofre de backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Enable-AzureRmBackupContainerReregistration** registra novamente um servidor para se conectar a um cofre de backup do Azure e continuar a cadeia de pontos de recuperação de backup.

Se você destruir um servidor, todos os pontos de backup na nuvem permanecerão no cofre de backup.
Se você criar um servidor de substituição e atribuí-lo ao mesmo nome de domínio totalmente qualificado, você poderá conectar o servidor de volta ao mesmo cofre.
Este cmdlet habilita o backup para fazer backups e adicionar novos pontos de backup ao conjunto existente.
O novo servidor continua na cadeia de backup.

## EXEMPLOS

## OS

### -Contêiner
Especifica o contêiner em que este cmdlet se registra novamente.
Para obter um **AzureRmBackupContainer** , use o cmdlet Get-AzureRmBackupContainer.

```yaml
Type: AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### AzureBackupContainer

## EXIBE

### Nenhuma

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Register-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)


