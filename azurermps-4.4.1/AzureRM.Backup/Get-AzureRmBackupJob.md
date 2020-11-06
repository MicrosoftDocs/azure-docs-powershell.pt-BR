---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 48c1a3c3b7422f76bfbea0fbff8c3df541764606
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427999"
---
# Get-AzureRmBackupJob

## Sinopse
Obtém trabalhos de backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Filterset (padrão)
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### JobsListFilter
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmBackupJob** Obtém trabalhos de backup do Azure para um cofre específico.

## EXEMPLOS

### Exemplo 1: obter todos os trabalhos em um cofre de backup
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .
O comando armazena esse objeto na variável $Vault.

O segundo comando obtém todos os trabalhos do cofre em $Vault.

### Exemplo 2: obter trabalhos concluídos
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

Este comando obtém trabalhos concluídos do cofre no $Vault.

### Exemplo 3: obter trabalhos com falha na semana passada
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

Esse comando obtém trabalhos com falha da semana passada do cofre em $Vault.
O parâmetro *from* especifica um período de sete dias no passado.
O comando não especifica um valor para o parâmetro *to* .
Portanto, ele usa o valor padrão do tempo atual.

### Exemplo 4: sondar o backup para um trabalho em andamento que é concluído
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

Este script sonda o primeiro trabalho que está em andamento até que o trabalho seja concluído.

A primeira linha do script Obtém todos os trabalhos em $Vault que estão em andamento e armazena esses trabalhos na $Jobs variável de matriz.

A segunda linha armazena o primeiro trabalho da matriz $Jobs na variável $Job.

A terceira linha iniciará um loop **while** que verifica o status atual do trabalho até que o trabalho seja concluído.
Para obter informações sobre a palavra-chave **while** , digite `Get-Help about_While` .

O loop **while** grava uma mensagem no console, dorme por dez segundos e, em seguida, atualiza a variável $Job.
O script atualiza a variável $Job usando o valor existente do $Job e o cmdlet atual para obter o status atual do trabalho.
Para obter informações sobre os cmdlets do Windows PowerShell, digite `Get-Help Write-Host` e `Get-Help Start-Sleep` .

A linha final do script informa que o script foi concluído.

## OS

### -De
Especifica o início, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.
Para obter um objeto **DateTime** , use o cmdlet Get-Date.
Para obter mais informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Trabalho
Especifica um trabalho que este cmdlet obtém.
Para obter um objeto **AzureRmBackupJob** , use o cmdlet Get-AzureRmBackupJob.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Especifica a ID de um trabalho que o cmdlet obtém.
A ID é a propriedade **InstanceId** de um objeto **AzureRmBackupJob** .
Para obter um objeto **AzureRmBackupJob** , use Get-AzureRmBackupJob.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Operação
Especifica uma operação dos trabalhos que este cmdlet obtém.
Os valores aceitáveis para esse parâmetro são:

- Fazer 
- ConfigureBackup 
- DeleteBackupData 
- Inscrição 
- Restaurar 
- Desproteger 
- Cancele

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Especifica um status dos trabalhos que este cmdlet obtém.
Os valores aceitáveis para esse parâmetro são:

- InProgress
- Conseguiu
- Cela
- Cancelamento
- Feito
- CompletedWithWarnings 

Você pode especificar esse parâmetro para localizar todos os trabalhos em andamento ou todos os trabalhos com falha.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -To
Especifica o fim, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.
O valor padrão é a hora atual do sistema.
Se você especificar esse parâmetro, também deverá especificar o parâmetro *from* .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Digite
Especifica o tipo de contêiner para o qual esse cmdlet obtém trabalhos de backup.
Atualmente, o único valor com suporte é AzureVM.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Cofre
Especifica o cofre de backup para o qual este cmdlet recebe trabalhos.
Para obter um objeto **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### AzureRmBackupVault

## EXIBE

### AzureRmBackupJob[]
Esse cmdlet retorna um ou mais trabalhos de backup.

## INFORMA
* Nenhuma

## LINKS RELACIONADOS

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Parar-AzureRmBackupJob](./Stop-AzureRmBackupJob.md)

[Wait-AzureRmBackupJob](./Wait-AzureRmBackupJob.md)


