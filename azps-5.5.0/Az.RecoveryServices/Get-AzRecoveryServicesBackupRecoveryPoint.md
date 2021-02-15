---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 8e102b6542e2e9b262224e73af7b0eb0ed49236a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114960"
---
# <span data-ttu-id="fea5e-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="fea5e-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="fea5e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fea5e-102">SYNOPSIS</span></span>

<span data-ttu-id="fea5e-103">Obtém os pontos de recuperação de um item em backup.</span><span class="sxs-lookup"><span data-stu-id="fea5e-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="fea5e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fea5e-104">SYNTAX</span></span>

### <span data-ttu-id="fea5e-105">NoFilterParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fea5e-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-UseSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fea5e-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="fea5e-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fea5e-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="fea5e-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fea5e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fea5e-108">DESCRIPTION</span></span>

<span data-ttu-id="fea5e-109">O cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** obtém os pontos de recuperação de um item de backup do Azure em backup.</span><span class="sxs-lookup"><span data-stu-id="fea5e-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="fea5e-110">Depois que um item é feito backup, um objeto **AzureRmRecoveryServicesBackupRecoveryPoint** tem um ou mais pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fea5e-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="fea5e-111">De definir o contexto do cofre usando o parâmetro -VaultId.</span><span class="sxs-lookup"><span data-stu-id="fea5e-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="fea5e-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fea5e-112">EXAMPLES</span></span>

### <span data-ttu-id="fea5e-113">Exemplo 1: Obter pontos de recuperação da semana passada para um item</span><span class="sxs-lookup"><span data-stu-id="fea5e-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="fea5e-114">O primeiro comando obtém o objeto do cofre com base no vaultName.</span><span class="sxs-lookup"><span data-stu-id="fea5e-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="fea5e-115">O segundo comando obtém a data de sete dias atrás e a armazena na variável $StartDate dados.</span><span class="sxs-lookup"><span data-stu-id="fea5e-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="fea5e-116">O terceiro comando obtém a data de hoje e o armazena na variável $EndDate dados.</span><span class="sxs-lookup"><span data-stu-id="fea5e-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="fea5e-117">O quarto comando obtém contêineres de backup do AzureVM e os armazena na variável $Container dados.</span><span class="sxs-lookup"><span data-stu-id="fea5e-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="fea5e-118">O quinto comando obtém o item de backup com base em workloadType, vaultId e o armazena na variável $BackupItem trabalho.</span><span class="sxs-lookup"><span data-stu-id="fea5e-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="fea5e-119">O último comando obtém uma matriz de pontos de recuperação para o item no $BackupItem e os armazena na variável $RP dados.</span><span class="sxs-lookup"><span data-stu-id="fea5e-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="fea5e-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fea5e-120">PARAMETERS</span></span>

### <span data-ttu-id="fea5e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea5e-121">-DefaultProfile</span></span>

<span data-ttu-id="fea5e-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fea5e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fea5e-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="fea5e-123">-EndDate</span></span>

<span data-ttu-id="fea5e-124">Especifica o final do intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="fea5e-124">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="fea5e-125">-Item</span><span class="sxs-lookup"><span data-stu-id="fea5e-125">-Item</span></span>

<span data-ttu-id="fea5e-126">Especifica o item para o qual este cmdlet obtém pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fea5e-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="fea5e-127">Para obter um **objeto AzureRmRecoveryServicesBackupItem,** use o cmdlet **Get-AzRecoveryServicesBackupItem.**</span><span class="sxs-lookup"><span data-stu-id="fea5e-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

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

### <span data-ttu-id="fea5e-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="fea5e-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="fea5e-129">Especifica o local para baixar o arquivo de entrada para restaurar a tecla KeyVault de uma máquina virtual criptografada.</span><span class="sxs-lookup"><span data-stu-id="fea5e-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="fea5e-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="fea5e-130">-RecoveryPointId</span></span>

<span data-ttu-id="fea5e-131">Especifica a ID do ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fea5e-131">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="fea5e-132">-Data Inicial</span><span class="sxs-lookup"><span data-stu-id="fea5e-132">-StartDate</span></span>

<span data-ttu-id="fea5e-133">Especifica o início do intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="fea5e-133">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="fea5e-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="fea5e-134">-VaultId</span></span>

<span data-ttu-id="fea5e-135">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="fea5e-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="fea5e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea5e-136">CommonParameters</span></span>
<span data-ttu-id="fea5e-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fea5e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea5e-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fea5e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea5e-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="fea5e-139">INPUTS</span></span>

### <span data-ttu-id="fea5e-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="fea5e-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="fea5e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="fea5e-141">System.String</span></span>

## <span data-ttu-id="fea5e-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="fea5e-142">OUTPUTS</span></span>

### <span data-ttu-id="fea5e-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="fea5e-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="fea5e-144">Notas</span><span class="sxs-lookup"><span data-stu-id="fea5e-144">NOTES</span></span>

## <span data-ttu-id="fea5e-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fea5e-145">RELATED LINKS</span></span>

[<span data-ttu-id="fea5e-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="fea5e-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="fea5e-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="fea5e-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
