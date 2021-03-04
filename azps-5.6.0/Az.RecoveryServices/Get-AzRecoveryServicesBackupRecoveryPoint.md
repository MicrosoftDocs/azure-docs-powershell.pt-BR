---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 9e9aab3a71e976d9c41694702dae7a8087da9a36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887683"
---
# <span data-ttu-id="17b86-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="17b86-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="17b86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17b86-102">SYNOPSIS</span></span>

<span data-ttu-id="17b86-103">Obtém os pontos de recuperação de um item com backup.</span><span class="sxs-lookup"><span data-stu-id="17b86-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="17b86-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="17b86-104">SYNTAX</span></span>

### <span data-ttu-id="17b86-105">NoFilterParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="17b86-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-UseSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17b86-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="17b86-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17b86-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="17b86-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17b86-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="17b86-108">DESCRIPTION</span></span>

<span data-ttu-id="17b86-109">O cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** obtém os pontos de recuperação de um item backup do Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="17b86-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="17b86-110">Depois que um item é feito backup, um **objeto AzureRmRecoveryServicesBackupRecoveryPoint** tem um ou mais pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="17b86-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="17b86-111">De definir o contexto do cofre usando o parâmetro -VaultId.</span><span class="sxs-lookup"><span data-stu-id="17b86-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="17b86-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17b86-112">EXAMPLES</span></span>

### <span data-ttu-id="17b86-113">Exemplo 1: Obter pontos de recuperação da última semana para um item</span><span class="sxs-lookup"><span data-stu-id="17b86-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="17b86-114">O primeiro comando obtém o objeto vault com base em vaultName.</span><span class="sxs-lookup"><span data-stu-id="17b86-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="17b86-115">O segundo comando obtém a data de sete dias atrás e armazena-a na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="17b86-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="17b86-116">O terceiro comando obtém a data de hoje e o armazena na variável $EndDate.</span><span class="sxs-lookup"><span data-stu-id="17b86-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="17b86-117">O quarto comando obtém contêineres de backup do AzureVM e os armazena na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="17b86-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="17b86-118">O quinto comando obtém o item de backup com base em workloadType, vaultId e o armazena na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="17b86-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="17b86-119">O último comando obtém uma matriz de pontos de recuperação do item no $BackupItem e os armazena na variável $RP.</span><span class="sxs-lookup"><span data-stu-id="17b86-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="17b86-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="17b86-120">PARAMETERS</span></span>

### <span data-ttu-id="17b86-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b86-121">-DefaultProfile</span></span>

<span data-ttu-id="17b86-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="17b86-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17b86-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="17b86-123">-EndDate</span></span>

<span data-ttu-id="17b86-124">Especifica o final do intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="17b86-124">Specifies the end of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b86-125">-Item</span><span class="sxs-lookup"><span data-stu-id="17b86-125">-Item</span></span>

<span data-ttu-id="17b86-126">Especifica o item para o qual este cmdlet obtém pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="17b86-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="17b86-127">Para obter um **objeto AzureRmRecoveryServicesBackupItem,** use o cmdlet **Get-AzRecoveryServicesBackupItem.**</span><span class="sxs-lookup"><span data-stu-id="17b86-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17b86-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="17b86-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="17b86-129">Especifica o local para baixar o arquivo de entrada para restaurar a chave KeyVault de uma máquina virtual criptografada.</span><span class="sxs-lookup"><span data-stu-id="17b86-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b86-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="17b86-130">-RecoveryPointId</span></span>

<span data-ttu-id="17b86-131">Especifica a ID do ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="17b86-131">Specifies the recovery point ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b86-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="17b86-132">-StartDate</span></span>

<span data-ttu-id="17b86-133">Especifica o início do intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="17b86-133">Specifies the start of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b86-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="17b86-134">-VaultId</span></span>

<span data-ttu-id="17b86-135">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="17b86-135">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17b86-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b86-136">CommonParameters</span></span>
<span data-ttu-id="17b86-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17b86-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b86-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17b86-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b86-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17b86-139">INPUTS</span></span>

### <span data-ttu-id="17b86-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="17b86-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="17b86-141">System.String</span><span class="sxs-lookup"><span data-stu-id="17b86-141">System.String</span></span>

## <span data-ttu-id="17b86-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="17b86-142">OUTPUTS</span></span>

### <span data-ttu-id="17b86-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="17b86-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="17b86-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="17b86-144">NOTES</span></span>

## <span data-ttu-id="17b86-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17b86-145">RELATED LINKS</span></span>

[<span data-ttu-id="17b86-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="17b86-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="17b86-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="17b86-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
