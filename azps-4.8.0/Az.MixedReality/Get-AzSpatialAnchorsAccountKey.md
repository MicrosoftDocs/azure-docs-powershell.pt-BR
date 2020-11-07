---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 81bce36cb1b8cd4737141e58ad3e220199e726cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955886"
---
# <span data-ttu-id="25c26-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="25c26-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="25c26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25c26-102">SYNOPSIS</span></span>
<span data-ttu-id="25c26-103">Obter chaves da conta de âncoras espaciais</span><span class="sxs-lookup"><span data-stu-id="25c26-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="25c26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25c26-104">SYNTAX</span></span>

### <span data-ttu-id="25c26-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="25c26-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25c26-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25c26-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25c26-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="25c26-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25c26-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25c26-108">DESCRIPTION</span></span>
<span data-ttu-id="25c26-109">Obter as chaves de desenvolvedor da conta de âncoras espaciais.</span><span class="sxs-lookup"><span data-stu-id="25c26-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="25c26-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25c26-110">EXAMPLES</span></span>

### <span data-ttu-id="25c26-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="25c26-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="25c26-112">Obter as chaves de desenvolvedor da conta de âncoras espaciais "exemplo" da assinatura atual e do grupo de recursos "Rg1".</span><span class="sxs-lookup"><span data-stu-id="25c26-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="25c26-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="25c26-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="25c26-114">Obter as chaves de desenvolvedor da conta de âncoras espaciais "exemplo" da assinatura atual e do grupo de recursos "Rg1" com o encanamento.</span><span class="sxs-lookup"><span data-stu-id="25c26-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="25c26-115">OS</span><span class="sxs-lookup"><span data-stu-id="25c26-115">PARAMETERS</span></span>

### <span data-ttu-id="25c26-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25c26-116">-DefaultProfile</span></span>
<span data-ttu-id="25c26-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25c26-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25c26-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25c26-118">-InputObject</span></span>
<span data-ttu-id="25c26-119">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="25c26-119">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25c26-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="25c26-120">-Name</span></span>
<span data-ttu-id="25c26-121">Nome da conta de âncoras espaciais.</span><span class="sxs-lookup"><span data-stu-id="25c26-121">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25c26-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25c26-122">-ResourceGroupName</span></span>
<span data-ttu-id="25c26-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="25c26-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25c26-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25c26-124">-ResourceId</span></span>
<span data-ttu-id="25c26-125">ID do recurso da conta de âncoras espaciais.</span><span class="sxs-lookup"><span data-stu-id="25c26-125">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25c26-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25c26-126">CommonParameters</span></span>
<span data-ttu-id="25c26-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25c26-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="25c26-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25c26-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25c26-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25c26-129">INPUTS</span></span>

### <span data-ttu-id="25c26-130">System. String</span><span class="sxs-lookup"><span data-stu-id="25c26-130">System.String</span></span>

### <span data-ttu-id="25c26-131">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="25c26-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="25c26-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25c26-132">OUTPUTS</span></span>

### <span data-ttu-id="25c26-133">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="25c26-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="25c26-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25c26-134">NOTES</span></span>

## <span data-ttu-id="25c26-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25c26-135">RELATED LINKS</span></span>
