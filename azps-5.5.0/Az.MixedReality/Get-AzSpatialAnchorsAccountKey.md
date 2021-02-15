---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 81bce36cb1b8cd4737141e58ad3e220199e726cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115235"
---
# <span data-ttu-id="6b0c7-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="6b0c7-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="6b0c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b0c7-102">SYNOPSIS</span></span>
<span data-ttu-id="6b0c7-103">Obter as chaves da Conta de Âncoras Desarmadas</span><span class="sxs-lookup"><span data-stu-id="6b0c7-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="6b0c7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b0c7-104">SYNTAX</span></span>

### <span data-ttu-id="6b0c7-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6b0c7-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b0c7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b0c7-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b0c7-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b0c7-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b0c7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b0c7-108">DESCRIPTION</span></span>
<span data-ttu-id="6b0c7-109">Obter chaves de desenvolvedor da Conta de Âncoras Desastradas.</span><span class="sxs-lookup"><span data-stu-id="6b0c7-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="6b0c7-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6b0c7-110">EXAMPLES</span></span>

### <span data-ttu-id="6b0c7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6b0c7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="6b0c7-112">Obter chaves de desenvolvedor da Conta de Âncoras Desastradas "exemplo" da assinatura atual e do Grupo de Recursos "rg1".</span><span class="sxs-lookup"><span data-stu-id="6b0c7-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="6b0c7-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6b0c7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="6b0c7-114">Obter chaves de desenvolvedor da Conta de Âncoras Desastradas "exemplo" da assinatura atual e do Grupo de Recursos "rg1" com piping.</span><span class="sxs-lookup"><span data-stu-id="6b0c7-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="6b0c7-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b0c7-115">PARAMETERS</span></span>

### <span data-ttu-id="6b0c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b0c7-116">-DefaultProfile</span></span>
<span data-ttu-id="6b0c7-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b0c7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b0c7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b0c7-118">-InputObject</span></span>
<span data-ttu-id="6b0c7-119">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="6b0c7-119">The custom domain object.</span></span>

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

### <span data-ttu-id="6b0c7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b0c7-120">-Name</span></span>
<span data-ttu-id="6b0c7-121">Nome da conta De âncoras de espaço.</span><span class="sxs-lookup"><span data-stu-id="6b0c7-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="6b0c7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b0c7-122">-ResourceGroupName</span></span>
<span data-ttu-id="6b0c7-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6b0c7-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="6b0c7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b0c7-124">-ResourceId</span></span>
<span data-ttu-id="6b0c7-125">ID do Recurso da Conta de Âncoras Desarmada.</span><span class="sxs-lookup"><span data-stu-id="6b0c7-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="6b0c7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b0c7-126">CommonParameters</span></span>
<span data-ttu-id="6b0c7-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b0c7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6b0c7-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b0c7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b0c7-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="6b0c7-129">INPUTS</span></span>

### <span data-ttu-id="6b0c7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6b0c7-130">System.String</span></span>

### <span data-ttu-id="6b0c7-131">Microsoft.Azure.Commands.MixedReality.GeoespaciaisAccount.PSSárialEstaresAccount</span><span class="sxs-lookup"><span data-stu-id="6b0c7-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="6b0c7-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="6b0c7-132">OUTPUTS</span></span>

### <span data-ttu-id="6b0c7-133">Microsoft.Azure.Commands.MixedReality.SpatialKeyrsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6b0c7-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="6b0c7-134">Notas</span><span class="sxs-lookup"><span data-stu-id="6b0c7-134">NOTES</span></span>

## <span data-ttu-id="6b0c7-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b0c7-135">RELATED LINKS</span></span>
