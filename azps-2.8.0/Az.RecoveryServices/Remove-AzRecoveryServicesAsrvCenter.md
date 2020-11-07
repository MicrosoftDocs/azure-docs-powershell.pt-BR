---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: c1ac3ae34e92feb2b356d5946a7b9f0a30a0a2aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772968"
---
# <span data-ttu-id="e48e7-101">Remove-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="e48e7-101">Remove-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="e48e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e48e7-102">SYNOPSIS</span></span>
<span data-ttu-id="e48e7-103">Remove o servidor do vCenter da malha ASR e interrompe a descoberta de máquinas virtuais a partir do servidor do vCenter.</span><span class="sxs-lookup"><span data-stu-id="e48e7-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="e48e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e48e7-104">SYNTAX</span></span>

### <span data-ttu-id="e48e7-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="e48e7-105">Default (Default)</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e48e7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e48e7-106">ByResourceId</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e48e7-107">ByName</span><span class="sxs-lookup"><span data-stu-id="e48e7-107">ByName</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e48e7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e48e7-108">DESCRIPTION</span></span>
<span data-ttu-id="e48e7-109">O cmdlet **Remove-AzRecoveryServicesAsrvCenter** remove o servidor vCenter da malha ASR e interrompe a descoberta de máquinas virtuais do servidor vCenter.</span><span class="sxs-lookup"><span data-stu-id="e48e7-109">The **Remove-AzRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="e48e7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e48e7-110">EXAMPLES</span></span>

### <span data-ttu-id="e48e7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e48e7-111">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="e48e7-112">Remove o servidor do vCenter da malha ASR.</span><span class="sxs-lookup"><span data-stu-id="e48e7-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="e48e7-113">OS</span><span class="sxs-lookup"><span data-stu-id="e48e7-113">PARAMETERS</span></span>

### <span data-ttu-id="e48e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e48e7-114">-DefaultProfile</span></span>
<span data-ttu-id="e48e7-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e48e7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e48e7-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="e48e7-116">-Fabric</span></span>
<span data-ttu-id="e48e7-117">Objeto de malha ASR que representa o servidor de configuração.</span><span class="sxs-lookup"><span data-stu-id="e48e7-117">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e48e7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e48e7-118">-InputObject</span></span>
<span data-ttu-id="e48e7-119">Objeto ASR do vCenter que representa o servidor vCenter a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e48e7-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e48e7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e48e7-120">-Name</span></span>
<span data-ttu-id="e48e7-121">Nome do servidor do vCenter.</span><span class="sxs-lookup"><span data-stu-id="e48e7-121">Name of the vCenter Server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e48e7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e48e7-122">-ResourceId</span></span>
<span data-ttu-id="e48e7-123">Especifica o ResourceId do vCenter a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e48e7-123">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e48e7-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e48e7-124">-Confirm</span></span>
<span data-ttu-id="e48e7-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e48e7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e48e7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e48e7-126">-WhatIf</span></span>
<span data-ttu-id="e48e7-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e48e7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e48e7-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e48e7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e48e7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e48e7-129">CommonParameters</span></span>
<span data-ttu-id="e48e7-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e48e7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e48e7-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e48e7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e48e7-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e48e7-132">INPUTS</span></span>

### <span data-ttu-id="e48e7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e48e7-133">System.String</span></span>

### <span data-ttu-id="e48e7-134">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="e48e7-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

### <span data-ttu-id="e48e7-135">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e48e7-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="e48e7-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e48e7-136">OUTPUTS</span></span>

### <span data-ttu-id="e48e7-137">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e48e7-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e48e7-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e48e7-138">NOTES</span></span>

## <span data-ttu-id="e48e7-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e48e7-139">RELATED LINKS</span></span>
