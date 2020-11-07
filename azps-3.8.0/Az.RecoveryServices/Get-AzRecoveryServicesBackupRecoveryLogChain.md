---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: 8a0fbc09f9c46bea6ac09d75911ac83b68f0e296
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944733"
---
# <span data-ttu-id="d03d3-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="d03d3-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="d03d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d03d3-102">SYNOPSIS</span></span>
<span data-ttu-id="d03d3-103">Esse comando lista os pontos de início e de término da cadeia de logs desfeitas do item de backup fornecido.</span><span class="sxs-lookup"><span data-stu-id="d03d3-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="d03d3-104">Use-o para determinar se o point-in-time, ao qual o usuário deseja que o banco de usuários seja restaurado, é válido ou não.</span><span class="sxs-lookup"><span data-stu-id="d03d3-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="d03d3-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d03d3-105">SYNTAX</span></span>

### <span data-ttu-id="d03d3-106">NoFilterParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d03d3-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d03d3-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="d03d3-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d03d3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d03d3-108">DESCRIPTION</span></span>
<span data-ttu-id="d03d3-109">O cmdlet **Get-AzRecoveryServicesBackupRecoveryLogChain** Obtém os pontos de recuperação de intervalo de tempo no tempo para um item de backup do Azure com backup.</span><span class="sxs-lookup"><span data-stu-id="d03d3-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="d03d3-110">Após o backup de um item, um objeto **AzRecoveryServicesBackupRecoveryLogChain** tem um ou mais intervalos de tempo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d03d3-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="d03d3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d03d3-111">EXAMPLES</span></span>

### <span data-ttu-id="d03d3-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d03d3-112">Example 1</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="d03d3-113">O primeiro comando obtém a data de sete dias atrás e, em seguida, armazena-o na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="d03d3-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="d03d3-114">O segundo comando obtém a data de hoje e, em seguida, armazena-o na variável $EndDate.</span><span class="sxs-lookup"><span data-stu-id="d03d3-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="d03d3-115">O terceiro comando obtém contêineres de backup do AzureWorkload e os armazena na variável $Containers.</span><span class="sxs-lookup"><span data-stu-id="d03d3-115">The third command gets AzureWorkload backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="d03d3-116">O quarto comando obtém o item de backup e, em seguida, armazena-o na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="d03d3-116">The fourth command gets the backup item, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="d03d3-117">O último comando obtém uma matriz de intervalos de tempo de ponto de recuperação para o item em $BackupItem e, em seguida, armazena-os na variável $RP.</span><span class="sxs-lookup"><span data-stu-id="d03d3-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="d03d3-118">OS</span><span class="sxs-lookup"><span data-stu-id="d03d3-118">PARAMETERS</span></span>

### <span data-ttu-id="d03d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d03d3-119">-DefaultProfile</span></span>
<span data-ttu-id="d03d3-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d03d3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d03d3-121">-EndDate</span><span class="sxs-lookup"><span data-stu-id="d03d3-121">-EndDate</span></span>
<span data-ttu-id="d03d3-122">Hora de término do intervalo de tempo para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="d03d3-122">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="d03d3-123">-Item</span><span class="sxs-lookup"><span data-stu-id="d03d3-123">-Item</span></span>
<span data-ttu-id="d03d3-124">Objeto de item protegido para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="d03d3-124">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="d03d3-125">-StartDate</span><span class="sxs-lookup"><span data-stu-id="d03d3-125">-StartDate</span></span>
<span data-ttu-id="d03d3-126">Hora de início do intervalo de tempo para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="d03d3-126">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="d03d3-127">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="d03d3-127">-VaultId</span></span>
<span data-ttu-id="d03d3-128">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d03d3-128">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d03d3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d03d3-129">CommonParameters</span></span>
<span data-ttu-id="d03d3-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d03d3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d03d3-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d03d3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d03d3-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d03d3-132">INPUTS</span></span>

### <span data-ttu-id="d03d3-133">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="d03d3-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="d03d3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d03d3-134">System.String</span></span>

## <span data-ttu-id="d03d3-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d03d3-135">OUTPUTS</span></span>

### <span data-ttu-id="d03d3-136">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="d03d3-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="d03d3-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d03d3-137">NOTES</span></span>

## <span data-ttu-id="d03d3-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d03d3-138">RELATED LINKS</span></span>
