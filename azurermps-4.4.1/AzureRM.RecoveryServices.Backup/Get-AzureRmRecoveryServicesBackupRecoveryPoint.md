---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 43ad564f261c423882b144d3fd9fbceba1273bcf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610472"
---
# <span data-ttu-id="ed6e1-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ed6e1-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="ed6e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed6e1-102">SYNOPSIS</span></span>
<span data-ttu-id="ed6e1-103">Obtém os pontos de recuperação para um item de backup.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed6e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed6e1-104">SYNTAX</span></span>

### <span data-ttu-id="ed6e1-105">NoFilterParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ed6e1-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed6e1-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="ed6e1-106">DateTimeFilter</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed6e1-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="ed6e1-107">RecoveryPointId</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed6e1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed6e1-108">DESCRIPTION</span></span>
<span data-ttu-id="ed6e1-109">O cmdlet **Get-AzureRmRecoveryServicesBackupRecoveryPoint** Obtém os pontos de recuperação para um item do Azure backup em backup.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-109">The **Get-AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="ed6e1-110">Após o backup de um item, um objeto **AzureRmRecoveryServicesBackupRecoveryPoint** tem um ou mais pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>

<span data-ttu-id="ed6e1-111">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ed6e1-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed6e1-112">EXAMPLES</span></span>

### <span data-ttu-id="ed6e1-113">Exemplo 1: obter pontos de recuperação da última semana para um item</span><span class="sxs-lookup"><span data-stu-id="ed6e1-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="ed6e1-114">O primeiro comando obtém a data de sete dias atrás e, em seguida, armazena-o na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="ed6e1-115">O segundo comando obtém a data de hoje e, em seguida, armazena-o na variável $EndDate.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="ed6e1-116">O terceiro comando obtém contêineres de backup do AzureVM e os armazena na variável $Containers.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>

<span data-ttu-id="ed6e1-117">O quarto comando obtém o item de backup chamado V2VM e, em seguida, armazena-o na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="ed6e1-118">O último comando obtém uma matriz de pontos de recuperação para o item em $BackupItem e, em seguida, os armazena na variável $RP.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="ed6e1-119">OS</span><span class="sxs-lookup"><span data-stu-id="ed6e1-119">PARAMETERS</span></span>

### <span data-ttu-id="ed6e1-120">-EndDate</span><span class="sxs-lookup"><span data-stu-id="ed6e1-120">-EndDate</span></span>
<span data-ttu-id="ed6e1-121">Especifica o final do intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-121">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="ed6e1-122">-Item</span><span class="sxs-lookup"><span data-stu-id="ed6e1-122">-Item</span></span>
<span data-ttu-id="ed6e1-123">Especifica o item para o qual esse cmdlet recebe pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-123">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="ed6e1-124">Para obter um objeto **AzureRmRecoveryServicesBackupItem** , use o cmdlet Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-124">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="ed6e1-125">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="ed6e1-125">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="ed6e1-126">Especifica o local para baixar o arquivo de entrada para restaurar a chave do keyvault para uma máquina virtual criptografada.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-126">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="ed6e1-127">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="ed6e1-127">-RecoveryPointId</span></span>
<span data-ttu-id="ed6e1-128">Especifica a ID do ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-128">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="ed6e1-129">-StartDate</span><span class="sxs-lookup"><span data-stu-id="ed6e1-129">-StartDate</span></span>
<span data-ttu-id="ed6e1-130">Especifica o início do intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-130">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="ed6e1-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed6e1-131">-DefaultProfile</span></span>
<span data-ttu-id="ed6e1-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed6e1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed6e1-133">CommonParameters</span></span>
<span data-ttu-id="ed6e1-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed6e1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed6e1-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed6e1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed6e1-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed6e1-136">INPUTS</span></span>

### <span data-ttu-id="ed6e1-137">Dobase</span><span class="sxs-lookup"><span data-stu-id="ed6e1-137">ItemBase</span></span>
<span data-ttu-id="ed6e1-138">O parâmetro ' item ' aceita o valor do tipo ' database ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ed6e1-138">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="ed6e1-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed6e1-139">OUTPUTS</span></span>

### <span data-ttu-id="ed6e1-140">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="ed6e1-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="ed6e1-141">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase]</span><span class="sxs-lookup"><span data-stu-id="ed6e1-141">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase]</span></span>

## <span data-ttu-id="ed6e1-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed6e1-142">NOTES</span></span>

## <span data-ttu-id="ed6e1-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed6e1-143">RELATED LINKS</span></span>

[<span data-ttu-id="ed6e1-144">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ed6e1-144">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="ed6e1-145">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ed6e1-145">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


