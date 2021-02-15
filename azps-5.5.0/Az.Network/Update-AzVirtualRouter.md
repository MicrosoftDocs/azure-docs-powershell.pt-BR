---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
ms.openlocfilehash: d7f52ded01ce5b785c1e935ba8d3ebf4b1c0a5fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115035"
---
# <span data-ttu-id="fdffb-101">Update-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="fdffb-101">Update-AzVirtualRouter</span></span>

## <span data-ttu-id="fdffb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fdffb-102">SYNOPSIS</span></span>
<span data-ttu-id="fdffb-103">Atualiza um Roteador Virtual.</span><span class="sxs-lookup"><span data-stu-id="fdffb-103">Updates a Virtual Router.</span></span> 

## <span data-ttu-id="fdffb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fdffb-104">SYNTAX</span></span>

### <span data-ttu-id="fdffb-105">VirtualRouterNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fdffb-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdffb-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdffb-106">VirtualRouterResourceIdParameterSet</span></span>
```
Update-AzVirtualRouter [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdffb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fdffb-107">DESCRIPTION</span></span>
<span data-ttu-id="fdffb-108">Atualiza o Roteador Virtual para habilitar ou desabilitar a ramificação para o tráfego de ramificação.</span><span class="sxs-lookup"><span data-stu-id="fdffb-108">Updates Virtual Router to enable or disable branch to branch traffic.</span></span>

## <span data-ttu-id="fdffb-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fdffb-109">EXAMPLES</span></span>

### <span data-ttu-id="fdffb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fdffb-110">Example 1</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName -AllowBranchToBranchTraffic
```

<span data-ttu-id="fdffb-111">Atualiza o Roteador Virtual para permitir a ramificação para o tráfego de ramificação</span><span class="sxs-lookup"><span data-stu-id="fdffb-111">Updates the Virtual Router to allow branch to branch traffic</span></span>

### <span data-ttu-id="fdffb-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fdffb-112">Example 2</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName
```

<span data-ttu-id="fdffb-113">Atualiza o Roteador Virtual para bloquear a ramificação para o tráfego de ramificação</span><span class="sxs-lookup"><span data-stu-id="fdffb-113">Updates the Virtual Router to block branch to branch traffic</span></span>

## <span data-ttu-id="fdffb-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fdffb-114">PARAMETERS</span></span>

### <span data-ttu-id="fdffb-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="fdffb-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="fdffb-116">Sinalizador para permitir ramificação para o tráfego de ramificação para roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="fdffb-116">Flag to allow branch to branch traffic for virtual router.</span></span>

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

### <span data-ttu-id="fdffb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdffb-117">-DefaultProfile</span></span>
<span data-ttu-id="fdffb-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fdffb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdffb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdffb-119">-ResourceGroupName</span></span>
<span data-ttu-id="fdffb-120">O nome do grupo de recursos do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="fdffb-120">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="fdffb-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdffb-121">-ResourceId</span></span>
<span data-ttu-id="fdffb-122">ResourceId do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="fdffb-122">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="fdffb-123">-Nomedo Roteador</span><span class="sxs-lookup"><span data-stu-id="fdffb-123">-RouterName</span></span>
<span data-ttu-id="fdffb-124">O nome do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="fdffb-124">The name of the virtual router.</span></span>

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

### <span data-ttu-id="fdffb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdffb-125">CommonParameters</span></span>
<span data-ttu-id="fdffb-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdffb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdffb-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fdffb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdffb-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="fdffb-128">INPUTS</span></span>

### <span data-ttu-id="fdffb-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fdffb-129">System.String</span></span>

## <span data-ttu-id="fdffb-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="fdffb-130">OUTPUTS</span></span>

### <span data-ttu-id="fdffb-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="fdffb-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="fdffb-132">Notas</span><span class="sxs-lookup"><span data-stu-id="fdffb-132">NOTES</span></span>

## <span data-ttu-id="fdffb-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdffb-133">RELATED LINKS</span></span>
