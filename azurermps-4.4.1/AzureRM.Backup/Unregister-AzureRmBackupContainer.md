---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 922BEA08-6619-4D4C-86EC-58279C9E1D93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
ms.openlocfilehash: 41209f3790b7520c50e3105f9ca7c4a5a0e79dfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610850"
---
# Unregister-AzureRmBackupContainer

## Sinopse
Cancela o registro de um contêiner de um cofre de backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Unregister-AzureRmBackupContainer [-Force] [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Unregister-AzureRmBackupContainer** cancela o registro do Windows Server ou da máquina virtual do Azure a partir de um cofre de backup do Azure.
Este cmdlet Remove referências a um contêiner do cofre de backup.
Antes de cancelar o registro de um contêiner, você deve excluir todos os dados protegidos associados a esse contêiner.

## EXEMPLOS

### Exemplo 1: cancelar o registro de um servidor Windows
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type Windows -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmBackupContainer -Container $Container[0]
Unregister Server
This operation will delete all data in the backup vault that is associated with the server. Are you sure you want to unregister the server? 
[] Yes  [] No  [?] Help (default is "No"): Yes
```

O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet Get-AzureRmBackupVault.
O comando armazena esse objeto na variável $Vault.

O segundo comando obtém um contêiner que tem o nome especificado no cofre no $Vault usando o cmdlet Get-AzureRmBackupContainer.
O comando armazena esse objeto na variável $Container.

O comando final cancela o registro do Windows Server especificado do cofre de backup do Azure.

### Exemplo 2: cancelar o registro de um servidor Windows sem confirmação
```
PS C:\>Unregister-AzureRmBackupContainer -Container $Container[0] -Force
```

Esse comando cancela o registro do Windows Server especificado do cofre de backup do Azure, exatamente como no primeiro exemplo.
Esse comando especifica o parâmetro *Force* .
Portanto, o comando não solicita confirmação.

## OS

### -Contêiner
Especifica o Windows Server ou a máquina virtual do Azure que este cmdlet cancela o registro.
Para obter um **AzureRmBackupContainer** , use o cmdlet Get-AzureRmBackupContainer.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Força o comando a ser executado sem pedir confirmação do usuário.
Esse parâmetro é relevante somente para objetos **AzureBackupContainer** do tipo Windows.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### AzureBackupContainer

## EXIBE

### AzureBackupJob
Esse cmdlet retorna $Null se o tipo de contêiner for Windows Server.

## INFORMA
* Nenhuma

## LINKS RELACIONADOS

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Register-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)


