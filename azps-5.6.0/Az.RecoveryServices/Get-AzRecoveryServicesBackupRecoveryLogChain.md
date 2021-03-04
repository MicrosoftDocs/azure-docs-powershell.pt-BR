---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: c0080985637e58232e2f7eea37344ab291d5d594
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888663"
---
# <span data-ttu-id="15658-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="15658-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="15658-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15658-102">SYNOPSIS</span></span>
<span data-ttu-id="15658-103">Este comando lista os pontos de início e fim da cadeia de log não quebrada do item de backup determinado.</span><span class="sxs-lookup"><span data-stu-id="15658-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="15658-104">Use-o para determinar se o point-in-time, ao qual o usuário deseja que o DB seja restaurado, é válido ou não.</span><span class="sxs-lookup"><span data-stu-id="15658-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="15658-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="15658-105">SYNTAX</span></span>

### <span data-ttu-id="15658-106">NoFilterParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="15658-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15658-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="15658-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15658-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="15658-108">DESCRIPTION</span></span>
<span data-ttu-id="15658-109">O cmdlet **Get-AzRecoveryServicesBackupRecoveryLogChain** obtém os pontos de recuperação de intervalo de tempo no tempo para um item backup do Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="15658-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="15658-110">Depois que um item é feito backup, um **objeto AzRecoveryServicesBackupRecoveryLogChain** tem um ou mais intervalos de tempo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="15658-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="15658-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15658-111">EXAMPLES</span></span>

### <span data-ttu-id="15658-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="15658-112">Example 1</span></span>
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="15658-113">O primeiro comando obtém a data de sete dias atrás e, em seguida, armazena-a na variável $StartDate de dados.</span><span class="sxs-lookup"><span data-stu-id="15658-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="15658-114">O segundo comando obtém a data de hoje e, em seguida, o armazena na variável $EndDate de dados.</span><span class="sxs-lookup"><span data-stu-id="15658-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="15658-115">O terceiro comando obtém contêineres de backup do AzureWorkload e os armazena na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="15658-115">The third command gets AzureWorkload backup containers, and stores them in the $Container variable.</span></span>
<span data-ttu-id="15658-116">O quarto comando obtém o item de backup e o compartilha no cmdlet canalado como objeto de item de backup.</span><span class="sxs-lookup"><span data-stu-id="15658-116">The fourth command gets the backup item, and then shares it across the piped cmdlet as backup item object.</span></span>
<span data-ttu-id="15658-117">O último comando obtém uma matriz de intervalos de tempo de ponto de recuperação para o item no $BackupItem e os armazena na variável $RP de recuperação.</span><span class="sxs-lookup"><span data-stu-id="15658-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

### <span data-ttu-id="15658-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="15658-118">Example 2</span></span>

<span data-ttu-id="15658-119">Este comando lista os pontos de início e fim da cadeia de log não quebrada do item de backup determinado.</span><span class="sxs-lookup"><span data-stu-id="15658-119">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="15658-120">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="15658-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="15658-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="15658-121">PARAMETERS</span></span>

### <span data-ttu-id="15658-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15658-122">-DefaultProfile</span></span>
<span data-ttu-id="15658-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15658-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15658-124">-EndDate</span><span class="sxs-lookup"><span data-stu-id="15658-124">-EndDate</span></span>
<span data-ttu-id="15658-125">Tempo de término do intervalo de tempo para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="15658-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="15658-126">-Item</span><span class="sxs-lookup"><span data-stu-id="15658-126">-Item</span></span>
<span data-ttu-id="15658-127">Objeto Item Protegido para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="15658-127">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="15658-128">-StartDate</span><span class="sxs-lookup"><span data-stu-id="15658-128">-StartDate</span></span>
<span data-ttu-id="15658-129">Hora de início do intervalo de tempo para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="15658-129">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="15658-130">-VaultId</span><span class="sxs-lookup"><span data-stu-id="15658-130">-VaultId</span></span>
<span data-ttu-id="15658-131">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="15658-131">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="15658-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15658-132">CommonParameters</span></span>
<span data-ttu-id="15658-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15658-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15658-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15658-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15658-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15658-135">INPUTS</span></span>

### <span data-ttu-id="15658-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="15658-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="15658-137">System.String</span><span class="sxs-lookup"><span data-stu-id="15658-137">System.String</span></span>

## <span data-ttu-id="15658-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="15658-138">OUTPUTS</span></span>

### <span data-ttu-id="15658-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="15658-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="15658-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="15658-140">NOTES</span></span>

## <span data-ttu-id="15658-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15658-141">RELATED LINKS</span></span>
