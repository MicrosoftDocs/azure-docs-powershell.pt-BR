---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 505d2d81eefed3132cd693ea6cd989fde173b8b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440040"
---
# <span data-ttu-id="6fa76-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="6fa76-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="6fa76-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6fa76-102">SYNOPSIS</span></span>
<span data-ttu-id="6fa76-103">Remove o servidor do vCenter da malha ASR e interrompe a descoberta de máquinas virtuais a partir do servidor do vCenter.</span><span class="sxs-lookup"><span data-stu-id="6fa76-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fa76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fa76-104">SYNTAX</span></span>

### <span data-ttu-id="6fa76-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="6fa76-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fa76-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6fa76-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fa76-107">ByName</span><span class="sxs-lookup"><span data-stu-id="6fa76-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fa76-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6fa76-108">DESCRIPTION</span></span>
<span data-ttu-id="6fa76-109">O cmdlet **Remove-AzureRmRecoveryServicesAsrvCenter** remove o servidor vCenter da malha ASR e interrompe a descoberta de máquinas virtuais do servidor vCenter.</span><span class="sxs-lookup"><span data-stu-id="6fa76-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="6fa76-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6fa76-110">EXAMPLES</span></span>

### <span data-ttu-id="6fa76-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6fa76-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="6fa76-112">Remove o servidor do vCenter da malha ASR.</span><span class="sxs-lookup"><span data-stu-id="6fa76-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="6fa76-113">OS</span><span class="sxs-lookup"><span data-stu-id="6fa76-113">PARAMETERS</span></span>

### <span data-ttu-id="6fa76-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fa76-114">-DefaultProfile</span></span>
<span data-ttu-id="6fa76-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6fa76-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fa76-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="6fa76-116">-Fabric</span></span>
<span data-ttu-id="6fa76-117">Objeto de malha ASR que representa o servidor de configuração.</span><span class="sxs-lookup"><span data-stu-id="6fa76-117">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="6fa76-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fa76-118">-InputObject</span></span>
<span data-ttu-id="6fa76-119">Objeto ASR do vCenter que representa o servidor vCenter a ser removido.</span><span class="sxs-lookup"><span data-stu-id="6fa76-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

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

### <span data-ttu-id="6fa76-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6fa76-120">-Name</span></span>
<span data-ttu-id="6fa76-121">Nome do servidor do vCenter.</span><span class="sxs-lookup"><span data-stu-id="6fa76-121">Name of the vCenter Server.</span></span>

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

### <span data-ttu-id="6fa76-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fa76-122">-ResourceId</span></span>
<span data-ttu-id="6fa76-123">Especifica o ResourceId do vCenter a ser removido.</span><span class="sxs-lookup"><span data-stu-id="6fa76-123">Specifies the resourceId of vCenter to remove.</span></span>

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

### <span data-ttu-id="6fa76-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6fa76-124">-Confirm</span></span>
<span data-ttu-id="6fa76-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fa76-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fa76-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fa76-126">-WhatIf</span></span>
<span data-ttu-id="6fa76-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6fa76-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fa76-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6fa76-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fa76-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fa76-129">CommonParameters</span></span>
<span data-ttu-id="6fa76-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fa76-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fa76-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fa76-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fa76-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6fa76-132">INPUTS</span></span>

### <span data-ttu-id="6fa76-133">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="6fa76-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="6fa76-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6fa76-134">OUTPUTS</span></span>

### <span data-ttu-id="6fa76-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6fa76-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6fa76-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6fa76-136">NOTES</span></span>

## <span data-ttu-id="6fa76-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6fa76-137">RELATED LINKS</span></span>
