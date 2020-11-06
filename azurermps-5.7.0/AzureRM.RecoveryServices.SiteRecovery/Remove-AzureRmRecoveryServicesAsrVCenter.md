---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: eaa357e6dd216b62a2c8e8f1cd78ff15387be57a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429731"
---
# <span data-ttu-id="0d026-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="0d026-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="0d026-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d026-102">SYNOPSIS</span></span>
<span data-ttu-id="0d026-103">Remove o servidor do vCenter da malha ASR e interrompe a descoberta de máquinas virtuais a partir do servidor do vCenter.</span><span class="sxs-lookup"><span data-stu-id="0d026-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d026-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d026-104">SYNTAX</span></span>

### <span data-ttu-id="0d026-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="0d026-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d026-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0d026-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d026-107">ByName</span><span class="sxs-lookup"><span data-stu-id="0d026-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d026-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d026-108">DESCRIPTION</span></span>
<span data-ttu-id="0d026-109">O cmdlet **Remove-AzureRmRecoveryServicesAsrvCenter** remove o servidor vCenter da malha ASR e interrompe a descoberta de máquinas virtuais do servidor vCenter.</span><span class="sxs-lookup"><span data-stu-id="0d026-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="0d026-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d026-110">EXAMPLES</span></span>

### <span data-ttu-id="0d026-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0d026-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="0d026-112">Remove o servidor do vCenter da malha ASR.</span><span class="sxs-lookup"><span data-stu-id="0d026-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="0d026-113">OS</span><span class="sxs-lookup"><span data-stu-id="0d026-113">PARAMETERS</span></span>

### <span data-ttu-id="0d026-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0d026-114">-Confirm</span></span>
<span data-ttu-id="0d026-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d026-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d026-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d026-116">-DefaultProfile</span></span>
<span data-ttu-id="0d026-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d026-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d026-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="0d026-118">-Fabric</span></span>
<span data-ttu-id="0d026-119">Objeto de malha ASR que representa o servidor de configuração.</span><span class="sxs-lookup"><span data-stu-id="0d026-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d026-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d026-120">-InputObject</span></span>
<span data-ttu-id="0d026-121">Objeto ASR do vCenter que representa o servidor vCenter a ser removido.</span><span class="sxs-lookup"><span data-stu-id="0d026-121">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d026-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d026-122">-Name</span></span>
<span data-ttu-id="0d026-123">Nome do servidor do vCenter.</span><span class="sxs-lookup"><span data-stu-id="0d026-123">Name of the vCenter Server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d026-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d026-124">-ResourceId</span></span>
<span data-ttu-id="0d026-125">Especifica o ResourceId do vCenter a ser removido.</span><span class="sxs-lookup"><span data-stu-id="0d026-125">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d026-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d026-126">-WhatIf</span></span>
<span data-ttu-id="0d026-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0d026-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d026-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0d026-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d026-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d026-129">CommonParameters</span></span>
<span data-ttu-id="0d026-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d026-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d026-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d026-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d026-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d026-132">INPUTS</span></span>

### <span data-ttu-id="0d026-133">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="0d026-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="0d026-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d026-134">OUTPUTS</span></span>

### <span data-ttu-id="0d026-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0d026-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0d026-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d026-136">NOTES</span></span>

## <span data-ttu-id="0d026-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d026-137">RELATED LINKS</span></span>
