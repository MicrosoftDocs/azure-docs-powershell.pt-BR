---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
ms.openlocfilehash: 119dec74416b8447d04aef7ae101016490408b5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885332"
---
# <span data-ttu-id="512ca-101">Update-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="512ca-101">Update-AzVirtualRouter</span></span>

## <span data-ttu-id="512ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="512ca-102">SYNOPSIS</span></span>
<span data-ttu-id="512ca-103">Atualiza um Roteador Virtual.</span><span class="sxs-lookup"><span data-stu-id="512ca-103">Updates a Virtual Router.</span></span> 

## <span data-ttu-id="512ca-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="512ca-104">SYNTAX</span></span>

### <span data-ttu-id="512ca-105">VirtualRouterNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="512ca-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="512ca-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="512ca-106">VirtualRouterResourceIdParameterSet</span></span>
```
Update-AzVirtualRouter [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="512ca-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="512ca-107">DESCRIPTION</span></span>
<span data-ttu-id="512ca-108">Atualiza o Roteador Virtual para habilitar ou desabilitar o branch para o tráfego de filial.</span><span class="sxs-lookup"><span data-stu-id="512ca-108">Updates Virtual Router to enable or disable branch to branch traffic.</span></span>

## <span data-ttu-id="512ca-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="512ca-109">EXAMPLES</span></span>

### <span data-ttu-id="512ca-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="512ca-110">Example 1</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName -AllowBranchToBranchTraffic
```

<span data-ttu-id="512ca-111">Atualiza o Roteador Virtual para permitir ramificação para ramificar o tráfego</span><span class="sxs-lookup"><span data-stu-id="512ca-111">Updates the Virtual Router to allow branch to branch traffic</span></span>

### <span data-ttu-id="512ca-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="512ca-112">Example 2</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName
```

<span data-ttu-id="512ca-113">Atualiza o Roteador Virtual para bloquear o branch para o tráfego de filial</span><span class="sxs-lookup"><span data-stu-id="512ca-113">Updates the Virtual Router to block branch to branch traffic</span></span>

## <span data-ttu-id="512ca-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="512ca-114">PARAMETERS</span></span>

### <span data-ttu-id="512ca-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="512ca-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="512ca-116">Sinalizador para permitir ramificação de tráfego para roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="512ca-116">Flag to allow branch to branch traffic for virtual router.</span></span>

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

### <span data-ttu-id="512ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="512ca-117">-DefaultProfile</span></span>
<span data-ttu-id="512ca-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="512ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="512ca-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="512ca-119">-ResourceGroupName</span></span>
<span data-ttu-id="512ca-120">O nome do grupo de recursos do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="512ca-120">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512ca-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="512ca-121">-ResourceId</span></span>
<span data-ttu-id="512ca-122">ResourceId do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="512ca-122">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512ca-123">-RouterName</span><span class="sxs-lookup"><span data-stu-id="512ca-123">-RouterName</span></span>
<span data-ttu-id="512ca-124">O nome do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="512ca-124">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512ca-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="512ca-125">CommonParameters</span></span>
<span data-ttu-id="512ca-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="512ca-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="512ca-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="512ca-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="512ca-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="512ca-128">INPUTS</span></span>

### <span data-ttu-id="512ca-129">System.String</span><span class="sxs-lookup"><span data-stu-id="512ca-129">System.String</span></span>

## <span data-ttu-id="512ca-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="512ca-130">OUTPUTS</span></span>

### <span data-ttu-id="512ca-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="512ca-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="512ca-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="512ca-132">NOTES</span></span>

## <span data-ttu-id="512ca-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="512ca-133">RELATED LINKS</span></span>
