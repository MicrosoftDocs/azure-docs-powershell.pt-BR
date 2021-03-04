---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 4cb66f01b8ce61edf9a5399119aa5e6318617db7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885616"
---
# <span data-ttu-id="2d433-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2d433-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="2d433-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d433-102">SYNOPSIS</span></span>
<span data-ttu-id="2d433-103">Cria um Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="2d433-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="2d433-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2d433-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d433-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2d433-105">DESCRIPTION</span></span>
<span data-ttu-id="2d433-106">O cmdlet **New-AzSecurityPartnerProvider** cria um Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2d433-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="2d433-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d433-107">EXAMPLES</span></span>

### <span data-ttu-id="2d433-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2d433-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="2d433-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2d433-109">PARAMETERS</span></span>

### <span data-ttu-id="2d433-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d433-110">-AsJob</span></span>
<span data-ttu-id="2d433-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2d433-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d433-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d433-112">-DefaultProfile</span></span>
<span data-ttu-id="2d433-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d433-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d433-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2d433-114">-Force</span></span>
<span data-ttu-id="2d433-115">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="2d433-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2d433-116">-Location</span><span class="sxs-lookup"><span data-stu-id="2d433-116">-Location</span></span>
<span data-ttu-id="2d433-117">location.</span><span class="sxs-lookup"><span data-stu-id="2d433-117">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d433-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2d433-118">-Name</span></span>
<span data-ttu-id="2d433-119">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="2d433-119">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d433-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d433-120">-ResourceGroupName</span></span>
<span data-ttu-id="2d433-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2d433-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d433-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="2d433-122">-SecurityProviderName</span></span>
<span data-ttu-id="2d433-123">O nome do Provedor de Segurança</span><span class="sxs-lookup"><span data-stu-id="2d433-123">The Security Provider name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ZScaler, IBoss, Checkpoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d433-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="2d433-124">-Tag</span></span>
<span data-ttu-id="2d433-125">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="2d433-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d433-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="2d433-126">-VirtualHub</span></span>
<span data-ttu-id="2d433-127">A ID do hub virtual ao que o provedor de parceiros de segurança está anexado</span><span class="sxs-lookup"><span data-stu-id="2d433-127">The virtual hub Id that the security partner provider is attached to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d433-128">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="2d433-128">-VirtualHubId</span></span>
<span data-ttu-id="2d433-129">A ID do VirtualHub a que o VpnGateway precisa ser associado.</span><span class="sxs-lookup"><span data-stu-id="2d433-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d433-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="2d433-130">-VirtualHubName</span></span>
<span data-ttu-id="2d433-131">A ID do VirtualHub a que o VpnGateway precisa ser associado.</span><span class="sxs-lookup"><span data-stu-id="2d433-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d433-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d433-132">-Confirm</span></span>
<span data-ttu-id="2d433-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d433-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d433-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d433-134">-WhatIf</span></span>
<span data-ttu-id="2d433-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2d433-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d433-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d433-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d433-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d433-137">CommonParameters</span></span>
<span data-ttu-id="2d433-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d433-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d433-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d433-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d433-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d433-140">INPUTS</span></span>

### <span data-ttu-id="2d433-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2d433-141">System.String</span></span>

### <span data-ttu-id="2d433-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2d433-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="2d433-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2d433-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2d433-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2d433-144">OUTPUTS</span></span>

### <span data-ttu-id="2d433-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2d433-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="2d433-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="2d433-146">NOTES</span></span>

## <span data-ttu-id="2d433-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d433-147">RELATED LINKS</span></span>
