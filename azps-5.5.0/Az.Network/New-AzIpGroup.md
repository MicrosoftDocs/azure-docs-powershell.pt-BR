---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: 6ae61090f98cbb9929cc5ad1b2745fbf88f21a2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113480"
---
# <span data-ttu-id="b5974-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="b5974-101">New-AzIpGroup</span></span>

## <span data-ttu-id="b5974-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5974-102">SYNOPSIS</span></span>
<span data-ttu-id="b5974-103">Cria um Azure IpGroup.</span><span class="sxs-lookup"><span data-stu-id="b5974-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="b5974-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5974-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5974-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5974-105">DESCRIPTION</span></span>
<span data-ttu-id="b5974-106">O **cmdlet New-AzIpGroup** cria um Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="b5974-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="b5974-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b5974-107">EXAMPLES</span></span>

### <span data-ttu-id="b5974-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b5974-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="b5974-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b5974-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="b5974-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5974-110">PARAMETERS</span></span>

### <span data-ttu-id="b5974-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5974-111">-AsJob</span></span>
<span data-ttu-id="b5974-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b5974-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5974-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5974-113">-DefaultProfile</span></span>
<span data-ttu-id="b5974-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b5974-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5974-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="b5974-115">-Force</span></span>
<span data-ttu-id="b5974-116">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="b5974-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b5974-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="b5974-117">-IpAddress</span></span>
<span data-ttu-id="b5974-118">Endereços Ip definidos no IpGroup</span><span class="sxs-lookup"><span data-stu-id="b5974-118">IpAddresses defined in the IpGroup</span></span>

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

### <span data-ttu-id="b5974-119">-Local</span><span class="sxs-lookup"><span data-stu-id="b5974-119">-Location</span></span>
<span data-ttu-id="b5974-120">O local.</span><span class="sxs-lookup"><span data-stu-id="b5974-120">The location.</span></span>

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

### <span data-ttu-id="b5974-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5974-121">-Name</span></span>
<span data-ttu-id="b5974-122">O nome do grupo ip.</span><span class="sxs-lookup"><span data-stu-id="b5974-122">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="b5974-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5974-123">-ResourceGroupName</span></span>
<span data-ttu-id="b5974-124">O nome do grupo de recursos do grupo ip.</span><span class="sxs-lookup"><span data-stu-id="b5974-124">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="b5974-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="b5974-125">-Tag</span></span>
<span data-ttu-id="b5974-126">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="b5974-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b5974-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b5974-127">-Confirm</span></span>
<span data-ttu-id="b5974-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5974-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5974-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5974-129">-WhatIf</span></span>
<span data-ttu-id="b5974-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b5974-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5974-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b5974-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5974-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5974-132">CommonParameters</span></span>
<span data-ttu-id="b5974-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5974-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5974-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5974-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5974-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="b5974-135">INPUTS</span></span>

### <span data-ttu-id="b5974-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b5974-136">System.String</span></span>

### <span data-ttu-id="b5974-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b5974-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="b5974-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b5974-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b5974-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="b5974-139">OUTPUTS</span></span>

### <span data-ttu-id="b5974-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="b5974-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="b5974-141">Notas</span><span class="sxs-lookup"><span data-stu-id="b5974-141">NOTES</span></span>

## <span data-ttu-id="b5974-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5974-142">RELATED LINKS</span></span>
