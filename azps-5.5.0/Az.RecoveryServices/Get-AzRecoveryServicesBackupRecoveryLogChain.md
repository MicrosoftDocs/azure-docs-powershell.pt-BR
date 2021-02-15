---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: ba82e1ddf8385f74b271feb9119280d48fc1b859
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111465"
---
# <span data-ttu-id="d2a03-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="d2a03-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="d2a03-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2a03-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a03-103">Esse comando lista os pontos de início e de término da cadeia de log não quebrada do item de backup determinado.</span><span class="sxs-lookup"><span data-stu-id="d2a03-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="d2a03-104">Use-o para determinar se o ponto de tempo, para o qual o usuário quer que o BD seja restaurado, é válido ou não.</span><span class="sxs-lookup"><span data-stu-id="d2a03-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="d2a03-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2a03-105">SYNTAX</span></span>

### <span data-ttu-id="d2a03-106">NoFilterParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d2a03-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2a03-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="d2a03-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2a03-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2a03-108">DESCRIPTION</span></span>
<span data-ttu-id="d2a03-109">O cmdlet **Get-AzRecoveryServicesBackupRecoveryLogChain** obtém os pontos de recuperação de intervalo de tempo no tempo de um item de backup do Azure em backup.</span><span class="sxs-lookup"><span data-stu-id="d2a03-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="d2a03-110">Depois que um item é feito backup, um objeto **AzRecoveryServicesBackupRecoveryLogChain** tem um ou mais intervalos de tempo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d2a03-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="d2a03-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d2a03-111">EXAMPLES</span></span>

### <span data-ttu-id="d2a03-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2a03-112">Example 1</span></span>
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="d2a03-113">O primeiro comando obtém a data de sete dias atrás e a armazena na variável $StartDate dados.</span><span class="sxs-lookup"><span data-stu-id="d2a03-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="d2a03-114">O segundo comando obtém a data de hoje e o armazena na variável $EndDate dados.</span><span class="sxs-lookup"><span data-stu-id="d2a03-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="d2a03-115">O terceiro comando obtém contêineres de backup do AzureWorkload e os armazena na variável $Container dados.</span><span class="sxs-lookup"><span data-stu-id="d2a03-115">The third command gets AzureWorkload backup containers, and stores them in the $Container variable.</span></span>
<span data-ttu-id="d2a03-116">O quarto comando obtém o item de backup e o compartilha no cmdlet encadeado como objeto de item de backup.</span><span class="sxs-lookup"><span data-stu-id="d2a03-116">The fourth command gets the backup item, and then shares it across the piped cmdlet as backup item object.</span></span>
<span data-ttu-id="d2a03-117">O último comando obtém uma matriz de intervalos de tempo de ponto de recuperação para o item no $BackupItem e os armazena na variável $RP de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d2a03-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

### <span data-ttu-id="d2a03-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d2a03-118">Example 2</span></span>

<span data-ttu-id="d2a03-119">Esse comando lista os pontos de início e de término da cadeia de log não quebrada do item de backup determinado.</span><span class="sxs-lookup"><span data-stu-id="d2a03-119">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="d2a03-120">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="d2a03-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="d2a03-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2a03-121">PARAMETERS</span></span>

### <span data-ttu-id="d2a03-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a03-122">-DefaultProfile</span></span>
<span data-ttu-id="d2a03-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2a03-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2a03-124">-EndDate</span><span class="sxs-lookup"><span data-stu-id="d2a03-124">-EndDate</span></span>
<span data-ttu-id="d2a03-125">Hora de término do intervalo de tempo para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="d2a03-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="d2a03-126">-Item</span><span class="sxs-lookup"><span data-stu-id="d2a03-126">-Item</span></span>
<span data-ttu-id="d2a03-127">Objeto Item Protegido para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="d2a03-127">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="d2a03-128">-Data Inicial</span><span class="sxs-lookup"><span data-stu-id="d2a03-128">-StartDate</span></span>
<span data-ttu-id="d2a03-129">Hora de início do intervalo de tempo para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="d2a03-129">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="d2a03-130">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d2a03-130">-VaultId</span></span>
<span data-ttu-id="d2a03-131">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="d2a03-131">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d2a03-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a03-132">CommonParameters</span></span>
<span data-ttu-id="d2a03-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2a03-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a03-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2a03-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a03-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="d2a03-135">INPUTS</span></span>

### <span data-ttu-id="d2a03-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="d2a03-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="d2a03-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d2a03-137">System.String</span></span>

## <span data-ttu-id="d2a03-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="d2a03-138">OUTPUTS</span></span>

### <span data-ttu-id="d2a03-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="d2a03-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="d2a03-140">Notas</span><span class="sxs-lookup"><span data-stu-id="d2a03-140">NOTES</span></span>

## <span data-ttu-id="d2a03-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2a03-141">RELATED LINKS</span></span>
