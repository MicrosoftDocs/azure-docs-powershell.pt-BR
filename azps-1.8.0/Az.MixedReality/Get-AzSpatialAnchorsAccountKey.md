---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: ec84b4def7b1dfd19b2c85c71dc6562fa4cae763
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770356"
---
# <span data-ttu-id="58a5a-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="58a5a-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="58a5a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="58a5a-103">Obter chaves da conta de âncoras espaciais</span><span class="sxs-lookup"><span data-stu-id="58a5a-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="58a5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58a5a-104">SYNTAX</span></span>

### <span data-ttu-id="58a5a-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="58a5a-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58a5a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58a5a-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58a5a-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="58a5a-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58a5a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58a5a-108">DESCRIPTION</span></span>
<span data-ttu-id="58a5a-109">Obter as chaves de desenvolvedor da conta de âncoras espaciais.</span><span class="sxs-lookup"><span data-stu-id="58a5a-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="58a5a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58a5a-110">EXAMPLES</span></span>

### <span data-ttu-id="58a5a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="58a5a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="58a5a-112">Obter as chaves de desenvolvedor da conta de âncoras espaciais "exemplo" da assinatura atual e do grupo de recursos "Rg1".</span><span class="sxs-lookup"><span data-stu-id="58a5a-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="58a5a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="58a5a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="58a5a-114">Obter as chaves de desenvolvedor da conta de âncoras espaciais "exemplo" da assinatura atual e do grupo de recursos "Rg1" com o encanamento.</span><span class="sxs-lookup"><span data-stu-id="58a5a-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="58a5a-115">OS</span><span class="sxs-lookup"><span data-stu-id="58a5a-115">PARAMETERS</span></span>

### <span data-ttu-id="58a5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a5a-116">-DefaultProfile</span></span>
<span data-ttu-id="58a5a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58a5a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58a5a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58a5a-118">-InputObject</span></span>
<span data-ttu-id="58a5a-119">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="58a5a-119">The custom domain object.</span></span>

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

### <span data-ttu-id="58a5a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="58a5a-120">-Name</span></span>
<span data-ttu-id="58a5a-121">Nome da conta de âncoras espaciais.</span><span class="sxs-lookup"><span data-stu-id="58a5a-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="58a5a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58a5a-122">-ResourceGroupName</span></span>
<span data-ttu-id="58a5a-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="58a5a-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="58a5a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58a5a-124">-ResourceId</span></span>
<span data-ttu-id="58a5a-125">ID do recurso da conta de âncoras espaciais.</span><span class="sxs-lookup"><span data-stu-id="58a5a-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="58a5a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a5a-126">CommonParameters</span></span>
<span data-ttu-id="58a5a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58a5a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="58a5a-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58a5a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a5a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58a5a-129">INPUTS</span></span>

### <span data-ttu-id="58a5a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="58a5a-130">System.String</span></span>

### <span data-ttu-id="58a5a-131">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="58a5a-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="58a5a-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58a5a-132">OUTPUTS</span></span>

### <span data-ttu-id="58a5a-133">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="58a5a-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccountKeys</span></span>

## <span data-ttu-id="58a5a-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58a5a-134">NOTES</span></span>

## <span data-ttu-id="58a5a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58a5a-135">RELATED LINKS</span></span>
