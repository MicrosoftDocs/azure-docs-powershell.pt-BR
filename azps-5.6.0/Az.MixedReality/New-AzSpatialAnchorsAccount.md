---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: a2a6dafe9aedfc41200e12bb3c583ad1b5fb02b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887701"
---
# <span data-ttu-id="4901f-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="4901f-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="4901f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4901f-102">SYNOPSIS</span></span>
<span data-ttu-id="4901f-103">Criar Conta de Âncoras Espaciais</span><span class="sxs-lookup"><span data-stu-id="4901f-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="4901f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4901f-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4901f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4901f-105">DESCRIPTION</span></span>
<span data-ttu-id="4901f-106">Crie uma nova Conta de Âncoras Espaciais em determinada Assinatura, Grupo de Recursos e Região.</span><span class="sxs-lookup"><span data-stu-id="4901f-106">Create a new Spatial Anchors Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="4901f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4901f-107">EXAMPLES</span></span>

### <span data-ttu-id="4901f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4901f-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSpatialAnchorsAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="4901f-109">Crie um novo "exemplo" de Conta de Âncoras Espaciais na Assinatura atual, Grupo de Recursos "rg1" e Central US.</span><span class="sxs-lookup"><span data-stu-id="4901f-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="4901f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4901f-110">PARAMETERS</span></span>

### <span data-ttu-id="4901f-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4901f-111">-Confirm</span></span>
<span data-ttu-id="4901f-112">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4901f-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4901f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4901f-113">-DefaultProfile</span></span>
<span data-ttu-id="4901f-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4901f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4901f-115">-Location</span><span class="sxs-lookup"><span data-stu-id="4901f-115">-Location</span></span>
<span data-ttu-id="4901f-116">Localização da conta de Âncoras Espaciais.</span><span class="sxs-lookup"><span data-stu-id="4901f-116">Spatial Anchors Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4901f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4901f-117">-Name</span></span>
<span data-ttu-id="4901f-118">Nome da conta de Âncoras Espaciais.</span><span class="sxs-lookup"><span data-stu-id="4901f-118">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4901f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4901f-119">-ResourceGroupName</span></span>
<span data-ttu-id="4901f-120">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="4901f-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4901f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4901f-121">-WhatIf</span></span>
<span data-ttu-id="4901f-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4901f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4901f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4901f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4901f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4901f-124">CommonParameters</span></span>
<span data-ttu-id="4901f-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4901f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4901f-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4901f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4901f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4901f-127">INPUTS</span></span>

### <span data-ttu-id="4901f-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4901f-128">None</span></span>

## <span data-ttu-id="4901f-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4901f-129">OUTPUTS</span></span>

### <span data-ttu-id="4901f-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="4901f-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="4901f-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="4901f-131">NOTES</span></span>

## <span data-ttu-id="4901f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4901f-132">RELATED LINKS</span></span>
