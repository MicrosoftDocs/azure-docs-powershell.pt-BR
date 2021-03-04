---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: 1f69ba390d0cdf3184b876147984c10e79ed423a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889895"
---
# <span data-ttu-id="43e12-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="43e12-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="43e12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43e12-102">SYNOPSIS</span></span>
<span data-ttu-id="43e12-103">Adicione o disco para proteção para a máquina virtual do azure já protegida.</span><span class="sxs-lookup"><span data-stu-id="43e12-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="43e12-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="43e12-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43e12-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="43e12-105">DESCRIPTION</span></span>
<span data-ttu-id="43e12-106">O cmdlet **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** adiciona o disco para proteção para a máquina virtual do azure já protegida.</span><span class="sxs-lookup"><span data-stu-id="43e12-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="43e12-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43e12-107">EXAMPLES</span></span>

### <span data-ttu-id="43e12-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="43e12-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="43e12-109">Inicie a operação para adicionar a configuração de disco especificada para proteção.</span><span class="sxs-lookup"><span data-stu-id="43e12-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="43e12-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="43e12-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="43e12-111">Inicie a operação para adicionar a configuração de disco especificada para proteção. Canalização de item protegido de replicação de entrada.</span><span class="sxs-lookup"><span data-stu-id="43e12-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="43e12-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="43e12-112">PARAMETERS</span></span>

### <span data-ttu-id="43e12-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="43e12-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="43e12-114">Especifica a configuração de disco a ser usada para proteção de disco do Azure para o cenário de recuperação de desastres do Azure.</span><span class="sxs-lookup"><span data-stu-id="43e12-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e12-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43e12-115">-DefaultProfile</span></span>
<span data-ttu-id="43e12-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43e12-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43e12-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43e12-117">-InputObject</span></span>
<span data-ttu-id="43e12-118">O objeto de entrada para o cmdlet: o objeto de item protegido de replicação ASR correspondente ao qual o novo disco deve ser protegido.</span><span class="sxs-lookup"><span data-stu-id="43e12-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43e12-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="43e12-119">-WaitForCompletion</span></span>
<span data-ttu-id="43e12-120">Aguardar conclusão</span><span class="sxs-lookup"><span data-stu-id="43e12-120">Wait For Completion</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e12-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43e12-121">-Confirm</span></span>
<span data-ttu-id="43e12-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43e12-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e12-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43e12-123">-WhatIf</span></span>
<span data-ttu-id="43e12-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="43e12-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43e12-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="43e12-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e12-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43e12-126">CommonParameters</span></span>
<span data-ttu-id="43e12-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43e12-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43e12-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43e12-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43e12-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43e12-129">INPUTS</span></span>

### <span data-ttu-id="43e12-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="43e12-130">None</span></span>

## <span data-ttu-id="43e12-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="43e12-131">OUTPUTS</span></span>

### <span data-ttu-id="43e12-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="43e12-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="43e12-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="43e12-133">NOTES</span></span>

## <span data-ttu-id="43e12-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43e12-134">RELATED LINKS</span></span>
