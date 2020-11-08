---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: ba82e1ddf8385f74b271feb9119280d48fc1b859
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116858"
---
# <span data-ttu-id="6317e-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="6317e-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="6317e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6317e-102">SYNOPSIS</span></span>
<span data-ttu-id="6317e-103">Esse comando lista os pontos de início e de término da cadeia de logs desfeitas do item de backup fornecido.</span><span class="sxs-lookup"><span data-stu-id="6317e-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="6317e-104">Use-o para determinar se o point-in-time, ao qual o usuário deseja que o banco de usuários seja restaurado, é válido ou não.</span><span class="sxs-lookup"><span data-stu-id="6317e-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="6317e-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6317e-105">SYNTAX</span></span>

### <span data-ttu-id="6317e-106">NoFilterParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6317e-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6317e-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="6317e-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6317e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6317e-108">DESCRIPTION</span></span>
<span data-ttu-id="6317e-109">O cmdlet **Get-AzRecoveryServicesBackupRecoveryLogChain** Obtém os pontos de recuperação de intervalo de tempo no tempo para um item de backup do Azure com backup.</span><span class="sxs-lookup"><span data-stu-id="6317e-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="6317e-110">Após o backup de um item, um objeto **AzRecoveryServicesBackupRecoveryLogChain** tem um ou mais intervalos de tempo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="6317e-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="6317e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6317e-111">EXAMPLES</span></span>

### <span data-ttu-id="6317e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6317e-112">Example 1</span></span>
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="6317e-113">O primeiro comando obtém a data de sete dias atrás e, em seguida, armazena-o na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="6317e-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="6317e-114">O segundo comando obtém a data de hoje e, em seguida, armazena-o na variável $EndDate.</span><span class="sxs-lookup"><span data-stu-id="6317e-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="6317e-115">O terceiro comando obtém contêineres de backup do AzureWorkload e os armazena na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="6317e-115">The third command gets AzureWorkload backup containers, and stores them in the $Container variable.</span></span>
<span data-ttu-id="6317e-116">O quarto comando obtém o item de backup e, em seguida, o compartilha pelo cmdlet canalizado como objeto de item de backup.</span><span class="sxs-lookup"><span data-stu-id="6317e-116">The fourth command gets the backup item, and then shares it across the piped cmdlet as backup item object.</span></span>
<span data-ttu-id="6317e-117">O último comando obtém uma matriz de intervalos de tempo de ponto de recuperação para o item em $BackupItem e, em seguida, armazena-os na variável $RP.</span><span class="sxs-lookup"><span data-stu-id="6317e-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

### <span data-ttu-id="6317e-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6317e-118">Example 2</span></span>

<span data-ttu-id="6317e-119">Esse comando lista os pontos de início e de término da cadeia de logs desfeitas do item de backup fornecido.</span><span class="sxs-lookup"><span data-stu-id="6317e-119">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="6317e-120">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="6317e-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="6317e-121">OS</span><span class="sxs-lookup"><span data-stu-id="6317e-121">PARAMETERS</span></span>

### <span data-ttu-id="6317e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6317e-122">-DefaultProfile</span></span>
<span data-ttu-id="6317e-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6317e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6317e-124">-EndDate</span><span class="sxs-lookup"><span data-stu-id="6317e-124">-EndDate</span></span>
<span data-ttu-id="6317e-125">Hora de término do intervalo de tempo para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="6317e-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="6317e-126">-Item</span><span class="sxs-lookup"><span data-stu-id="6317e-126">-Item</span></span>
<span data-ttu-id="6317e-127">Objeto de item protegido para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="6317e-127">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="6317e-128">-StartDate</span><span class="sxs-lookup"><span data-stu-id="6317e-128">-StartDate</span></span>
<span data-ttu-id="6317e-129">Hora de início do intervalo de tempo para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="6317e-129">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="6317e-130">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="6317e-130">-VaultId</span></span>
<span data-ttu-id="6317e-131">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="6317e-131">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6317e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6317e-132">CommonParameters</span></span>
<span data-ttu-id="6317e-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6317e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6317e-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6317e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6317e-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6317e-135">INPUTS</span></span>

### <span data-ttu-id="6317e-136">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="6317e-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="6317e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6317e-137">System.String</span></span>

## <span data-ttu-id="6317e-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6317e-138">OUTPUTS</span></span>

### <span data-ttu-id="6317e-139">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="6317e-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="6317e-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6317e-140">NOTES</span></span>

## <span data-ttu-id="6317e-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6317e-141">RELATED LINKS</span></span>
