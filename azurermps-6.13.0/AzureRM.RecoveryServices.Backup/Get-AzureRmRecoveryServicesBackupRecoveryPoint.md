---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: d9c53d550f64b17a7ee821b43322dd974b7b5676
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431300"
---
# <span data-ttu-id="f3f8d-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f3f8d-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="f3f8d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3f8d-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f8d-103">Obtém os pontos de recuperação para um item de backup.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3f8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3f8d-104">SYNTAX</span></span>

### <span data-ttu-id="f3f8d-105">NoFilterParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f3f8d-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3f8d-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="f3f8d-106">DateTimeFilter</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3f8d-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="f3f8d-107">RecoveryPointId</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3f8d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f3f8d-108">DESCRIPTION</span></span>
<span data-ttu-id="f3f8d-109">O cmdlet **Get-AzureRmRecoveryServicesBackupRecoveryPoint** Obtém os pontos de recuperação para um item do Azure backup em backup.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-109">The **Get-AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="f3f8d-110">Após o backup de um item, um objeto **AzureRmRecoveryServicesBackupRecoveryPoint** tem um ou mais pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="f3f8d-111">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f3f8d-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3f8d-112">EXAMPLES</span></span>

### <span data-ttu-id="f3f8d-113">Exemplo 1: obter pontos de recuperação da última semana para um item</span><span class="sxs-lookup"><span data-stu-id="f3f8d-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="f3f8d-114">O primeiro comando obtém a data de sete dias atrás e, em seguida, armazena-o na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="f3f8d-115">O segundo comando obtém a data de hoje e, em seguida, armazena-o na variável $EndDate.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="f3f8d-116">O terceiro comando obtém contêineres de backup do AzureVM e os armazena na variável $Containers.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="f3f8d-117">O quarto comando obtém o item de backup chamado V2VM e, em seguida, armazena-o na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="f3f8d-118">O último comando obtém uma matriz de pontos de recuperação para o item em $BackupItem e, em seguida, os armazena na variável $RP.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="f3f8d-119">OS</span><span class="sxs-lookup"><span data-stu-id="f3f8d-119">PARAMETERS</span></span>

### <span data-ttu-id="f3f8d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f8d-120">-DefaultProfile</span></span>
<span data-ttu-id="f3f8d-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3f8d-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="f3f8d-122">-EndDate</span></span>
<span data-ttu-id="f3f8d-123">Especifica o final do intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-123">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="f3f8d-124">-Item</span><span class="sxs-lookup"><span data-stu-id="f3f8d-124">-Item</span></span>
<span data-ttu-id="f3f8d-125">Especifica o item para o qual esse cmdlet recebe pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="f3f8d-126">Para obter um objeto **AzureRmRecoveryServicesBackupItem** , use o cmdlet Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="f3f8d-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="f3f8d-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="f3f8d-128">Especifica o local para baixar o arquivo de entrada para restaurar a chave do keyvault para uma máquina virtual criptografada.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="f3f8d-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="f3f8d-129">-RecoveryPointId</span></span>
<span data-ttu-id="f3f8d-130">Especifica a ID do ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-130">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="f3f8d-131">-StartDate</span><span class="sxs-lookup"><span data-stu-id="f3f8d-131">-StartDate</span></span>
<span data-ttu-id="f3f8d-132">Especifica o início do intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-132">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="f3f8d-133">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="f3f8d-133">-VaultId</span></span>
<span data-ttu-id="f3f8d-134">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-134">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f3f8d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f8d-135">CommonParameters</span></span>
<span data-ttu-id="f3f8d-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3f8d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f8d-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3f8d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f8d-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f3f8d-138">INPUTS</span></span>

### <span data-ttu-id="f3f8d-139">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="f3f8d-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="f3f8d-140">Parâmetros: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f3f8d-140">Parameters: Item (ByValue)</span></span>

### <span data-ttu-id="f3f8d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f3f8d-141">System.String</span></span>
<span data-ttu-id="f3f8d-142">Parâmetros: Vaultid (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f3f8d-142">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="f3f8d-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f3f8d-143">OUTPUTS</span></span>

### <span data-ttu-id="f3f8d-144">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="f3f8d-144">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="f3f8d-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f3f8d-145">NOTES</span></span>

## <span data-ttu-id="f3f8d-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3f8d-146">RELATED LINKS</span></span>

[<span data-ttu-id="f3f8d-147">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f3f8d-147">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="f3f8d-148">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="f3f8d-148">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

