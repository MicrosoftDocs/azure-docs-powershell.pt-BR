---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: 6ae61090f98cbb9929cc5ad1b2745fbf88f21a2a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429583"
---
# <span data-ttu-id="3d728-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="3d728-101">New-AzIpGroup</span></span>

## <span data-ttu-id="3d728-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d728-102">SYNOPSIS</span></span>
<span data-ttu-id="3d728-103">Cria um IpGroup do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d728-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="3d728-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d728-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d728-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d728-105">DESCRIPTION</span></span>
<span data-ttu-id="3d728-106">O cmdlet **New-AzIpGroup** cria um Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="3d728-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="3d728-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d728-107">EXAMPLES</span></span>

### <span data-ttu-id="3d728-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3d728-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="3d728-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3d728-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="3d728-110">OS</span><span class="sxs-lookup"><span data-stu-id="3d728-110">PARAMETERS</span></span>

### <span data-ttu-id="3d728-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d728-111">-AsJob</span></span>
<span data-ttu-id="3d728-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3d728-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d728-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d728-113">-DefaultProfile</span></span>
<span data-ttu-id="3d728-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d728-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d728-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3d728-115">-Force</span></span>
<span data-ttu-id="3d728-116">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="3d728-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3d728-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="3d728-117">-IpAddress</span></span>
<span data-ttu-id="3d728-118">IpAddresses definidos no IpGroup</span><span class="sxs-lookup"><span data-stu-id="3d728-118">IpAddresses defined in the IpGroup</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d728-119">-Local</span><span class="sxs-lookup"><span data-stu-id="3d728-119">-Location</span></span>
<span data-ttu-id="3d728-120">O local.</span><span class="sxs-lookup"><span data-stu-id="3d728-120">The location.</span></span>

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

### <span data-ttu-id="3d728-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d728-121">-Name</span></span>
<span data-ttu-id="3d728-122">O nome do ipgroup.</span><span class="sxs-lookup"><span data-stu-id="3d728-122">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="3d728-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d728-123">-ResourceGroupName</span></span>
<span data-ttu-id="3d728-124">O nome do grupo de recursos do ipgroup.</span><span class="sxs-lookup"><span data-stu-id="3d728-124">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="3d728-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="3d728-125">-Tag</span></span>
<span data-ttu-id="3d728-126">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d728-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3d728-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d728-127">-Confirm</span></span>
<span data-ttu-id="3d728-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d728-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d728-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d728-129">-WhatIf</span></span>
<span data-ttu-id="3d728-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d728-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d728-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d728-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d728-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d728-132">CommonParameters</span></span>
<span data-ttu-id="3d728-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d728-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d728-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d728-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d728-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d728-135">INPUTS</span></span>

### <span data-ttu-id="3d728-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3d728-136">System.String</span></span>

### <span data-ttu-id="3d728-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3d728-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="3d728-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3d728-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3d728-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d728-139">OUTPUTS</span></span>

### <span data-ttu-id="3d728-140">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="3d728-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="3d728-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d728-141">NOTES</span></span>

## <span data-ttu-id="3d728-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d728-142">RELATED LINKS</span></span>
