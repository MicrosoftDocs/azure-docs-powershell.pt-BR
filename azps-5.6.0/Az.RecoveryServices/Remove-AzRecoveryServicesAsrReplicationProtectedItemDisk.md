---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: bee3d9ff2f3e13397afba0cc85ecbb148aedc0cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885530"
---
# <span data-ttu-id="408e6-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="408e6-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="408e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="408e6-102">SYNOPSIS</span></span>
<span data-ttu-id="408e6-103">Remove discos para o item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="408e6-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="408e6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="408e6-104">SYNTAX</span></span>

### <span data-ttu-id="408e6-105">AzureToAzure (Padrão)</span><span class="sxs-lookup"><span data-stu-id="408e6-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="408e6-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="408e6-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="408e6-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="408e6-107">DESCRIPTION</span></span>
<span data-ttu-id="408e6-108">O cmdlet **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** remove o disco do item protegido por replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="408e6-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="408e6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="408e6-109">EXAMPLES</span></span>

### <span data-ttu-id="408e6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="408e6-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="408e6-111">Inicie a operação para remover o disco especificado da VM de proteção para disco nãomanageado.</span><span class="sxs-lookup"><span data-stu-id="408e6-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="408e6-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="408e6-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="408e6-113">Inicie a operação para remover o disco especificado da VM de proteção para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="408e6-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="408e6-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="408e6-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="408e6-115">Inicia a operação para remover o disco especificado e retorna o trabalho ASR usado para rastrear a operação remover disco protegido.</span><span class="sxs-lookup"><span data-stu-id="408e6-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="408e6-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="408e6-116">PARAMETERS</span></span>

### <span data-ttu-id="408e6-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="408e6-117">-Confirm</span></span>
<span data-ttu-id="408e6-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="408e6-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408e6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="408e6-119">-DefaultProfile</span></span>
<span data-ttu-id="408e6-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="408e6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408e6-121">-DiskId</span><span class="sxs-lookup"><span data-stu-id="408e6-121">-DiskId</span></span>
<span data-ttu-id="408e6-122">Especifica a lista de IDs de disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="408e6-122">Specifies the list of managed disk Ids.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408e6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="408e6-123">-InputObject</span></span>
<span data-ttu-id="408e6-124">O objeto de entrada para o cmdlet: o objeto de item protegido de replicação ASR correspondente ao disco a ser removido.</span><span class="sxs-lookup"><span data-stu-id="408e6-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="408e6-125">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="408e6-125">-VhdUri</span></span>
<span data-ttu-id="408e6-126">Especifica a lista de vhd Uri.</span><span class="sxs-lookup"><span data-stu-id="408e6-126">Specifies the list of vhd Uri's.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408e6-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="408e6-127">-WaitForCompletion</span></span>
<span data-ttu-id="408e6-128">Aguardar conclusão</span><span class="sxs-lookup"><span data-stu-id="408e6-128">Wait For Completion</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408e6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="408e6-129">-WhatIf</span></span>
<span data-ttu-id="408e6-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="408e6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="408e6-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="408e6-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408e6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="408e6-132">CommonParameters</span></span>
<span data-ttu-id="408e6-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="408e6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="408e6-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="408e6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="408e6-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="408e6-135">INPUTS</span></span>

### <span data-ttu-id="408e6-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="408e6-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="408e6-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="408e6-137">OUTPUTS</span></span>

### <span data-ttu-id="408e6-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="408e6-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="408e6-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="408e6-139">NOTES</span></span>

## <span data-ttu-id="408e6-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="408e6-140">RELATED LINKS</span></span>
