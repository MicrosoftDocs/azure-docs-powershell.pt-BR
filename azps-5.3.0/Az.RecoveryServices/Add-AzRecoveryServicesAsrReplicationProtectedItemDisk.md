---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427470"
---
# <span data-ttu-id="fd527-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="fd527-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="fd527-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd527-102">SYNOPSIS</span></span>
<span data-ttu-id="fd527-103">Adicione o disco para proteção para a máquina virtual do Azure já protegida.</span><span class="sxs-lookup"><span data-stu-id="fd527-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="fd527-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd527-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd527-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd527-105">DESCRIPTION</span></span>
<span data-ttu-id="fd527-106">O cmdlet **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** adiciona o disco para proteção para a máquina virtual do Azure já protegida.</span><span class="sxs-lookup"><span data-stu-id="fd527-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="fd527-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd527-107">EXAMPLES</span></span>

### <span data-ttu-id="fd527-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fd527-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="fd527-109">Inicie a operação para adicionar a configuração de disco especificada para proteção.</span><span class="sxs-lookup"><span data-stu-id="fd527-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="fd527-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fd527-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="fd527-111">Inicie a operação para adicionar a configuração de disco especificada para proteção. Item protegido de replicação de entrada de encanamento.</span><span class="sxs-lookup"><span data-stu-id="fd527-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="fd527-112">OS</span><span class="sxs-lookup"><span data-stu-id="fd527-112">PARAMETERS</span></span>

### <span data-ttu-id="fd527-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd527-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="fd527-114">Especifica a configuração de disco a ser usada para o cenário proteção de disco do Azure para recuperação de desastres do Azure.</span><span class="sxs-lookup"><span data-stu-id="fd527-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="fd527-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd527-115">-DefaultProfile</span></span>
<span data-ttu-id="fd527-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd527-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd527-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd527-117">-InputObject</span></span>
<span data-ttu-id="fd527-118">O objeto de entrada para o cmdlet: o objeto de item protegido da replicação ASR correspondente ao novo disco que deve ser protegido.</span><span class="sxs-lookup"><span data-stu-id="fd527-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

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

### <span data-ttu-id="fd527-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="fd527-119">-WaitForCompletion</span></span>
<span data-ttu-id="fd527-120">Aguardar conclusão</span><span class="sxs-lookup"><span data-stu-id="fd527-120">Wait For Completion</span></span>

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

### <span data-ttu-id="fd527-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fd527-121">-Confirm</span></span>
<span data-ttu-id="fd527-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd527-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd527-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd527-123">-WhatIf</span></span>
<span data-ttu-id="fd527-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fd527-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd527-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd527-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd527-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd527-126">CommonParameters</span></span>
<span data-ttu-id="fd527-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd527-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd527-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd527-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd527-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd527-129">INPUTS</span></span>

### <span data-ttu-id="fd527-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fd527-130">None</span></span>

## <span data-ttu-id="fd527-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd527-131">OUTPUTS</span></span>

### <span data-ttu-id="fd527-132">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fd527-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fd527-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd527-133">NOTES</span></span>

## <span data-ttu-id="fd527-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd527-134">RELATED LINKS</span></span>
