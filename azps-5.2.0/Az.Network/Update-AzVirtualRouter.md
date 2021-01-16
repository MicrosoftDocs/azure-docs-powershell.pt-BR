---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
ms.openlocfilehash: d7f52ded01ce5b785c1e935ba8d3ebf4b1c0a5fa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261168"
---
# <span data-ttu-id="e3107-101">Update-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e3107-101">Update-AzVirtualRouter</span></span>

## <span data-ttu-id="e3107-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3107-102">SYNOPSIS</span></span>
<span data-ttu-id="e3107-103">Atualiza um roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="e3107-103">Updates a Virtual Router.</span></span> 

## <span data-ttu-id="e3107-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3107-104">SYNTAX</span></span>

### <span data-ttu-id="e3107-105">VirtualRouterNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e3107-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3107-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3107-106">VirtualRouterResourceIdParameterSet</span></span>
```
Update-AzVirtualRouter [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3107-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3107-107">DESCRIPTION</span></span>
<span data-ttu-id="e3107-108">Atualiza o roteador virtual para habilitar ou desabilitar o tráfego de ramificação para ramificação.</span><span class="sxs-lookup"><span data-stu-id="e3107-108">Updates Virtual Router to enable or disable branch to branch traffic.</span></span>

## <span data-ttu-id="e3107-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3107-109">EXAMPLES</span></span>

### <span data-ttu-id="e3107-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3107-110">Example 1</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName -AllowBranchToBranchTraffic
```

<span data-ttu-id="e3107-111">Atualiza o roteador virtual para permitir o tráfego de ramificação para ramificação</span><span class="sxs-lookup"><span data-stu-id="e3107-111">Updates the Virtual Router to allow branch to branch traffic</span></span>

### <span data-ttu-id="e3107-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e3107-112">Example 2</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName
```

<span data-ttu-id="e3107-113">Atualiza o roteador virtual para bloquear o tráfego de ramificação para ramificação</span><span class="sxs-lookup"><span data-stu-id="e3107-113">Updates the Virtual Router to block branch to branch traffic</span></span>

## <span data-ttu-id="e3107-114">OS</span><span class="sxs-lookup"><span data-stu-id="e3107-114">PARAMETERS</span></span>

### <span data-ttu-id="e3107-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="e3107-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="e3107-116">Sinalizador para permitir o tráfego de ramificação para ramificação para o roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="e3107-116">Flag to allow branch to branch traffic for virtual router.</span></span>

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

### <span data-ttu-id="e3107-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3107-117">-DefaultProfile</span></span>
<span data-ttu-id="e3107-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3107-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3107-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3107-119">-ResourceGroupName</span></span>
<span data-ttu-id="e3107-120">O nome do grupo de recursos do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="e3107-120">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="e3107-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3107-121">-ResourceId</span></span>
<span data-ttu-id="e3107-122">ResourceId do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="e3107-122">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="e3107-123">-Roteadorname</span><span class="sxs-lookup"><span data-stu-id="e3107-123">-RouterName</span></span>
<span data-ttu-id="e3107-124">O nome do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="e3107-124">The name of the virtual router.</span></span>

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

### <span data-ttu-id="e3107-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3107-125">CommonParameters</span></span>
<span data-ttu-id="e3107-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3107-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3107-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3107-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3107-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3107-128">INPUTS</span></span>

### <span data-ttu-id="e3107-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e3107-129">System.String</span></span>

## <span data-ttu-id="e3107-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3107-130">OUTPUTS</span></span>

### <span data-ttu-id="e3107-131">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e3107-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="e3107-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3107-132">NOTES</span></span>

## <span data-ttu-id="e3107-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3107-133">RELATED LINKS</span></span>
