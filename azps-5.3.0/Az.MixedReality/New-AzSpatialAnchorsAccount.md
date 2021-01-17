---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 0b61764d358cc234f66dc8bb24249ca93a4e9919
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429489"
---
# <span data-ttu-id="a3b3b-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="a3b3b-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="a3b3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3b3b-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b3b-103">Criar conta de âncoras espaciais</span><span class="sxs-lookup"><span data-stu-id="a3b3b-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="a3b3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3b3b-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3b3b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3b3b-105">DESCRIPTION</span></span>
<span data-ttu-id="a3b3b-106">Crie uma nova conta de âncora espacial em determinada assinatura, grupo de recursos e região.</span><span class="sxs-lookup"><span data-stu-id="a3b3b-106">Create a new Spatial Anchors Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="a3b3b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3b3b-107">EXAMPLES</span></span>

### <span data-ttu-id="a3b3b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3b3b-108">Example 1</span></span>
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

<span data-ttu-id="a3b3b-109">Criar uma nova conta de âncora espacial "exemplo" na assinatura atual, grupo de recursos "Rg1" e centro dos EUA.</span><span class="sxs-lookup"><span data-stu-id="a3b3b-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="a3b3b-110">OS</span><span class="sxs-lookup"><span data-stu-id="a3b3b-110">PARAMETERS</span></span>

### <span data-ttu-id="a3b3b-111">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a3b3b-111">-Confirm</span></span>
<span data-ttu-id="a3b3b-112">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3b3b-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3b3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b3b-113">-DefaultProfile</span></span>
<span data-ttu-id="a3b3b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3b3b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3b3b-115">-Local</span><span class="sxs-lookup"><span data-stu-id="a3b3b-115">-Location</span></span>
<span data-ttu-id="a3b3b-116">Local da conta de âncoras espaciais.</span><span class="sxs-lookup"><span data-stu-id="a3b3b-116">Spatial Anchors Account Location.</span></span>

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

### <span data-ttu-id="a3b3b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3b3b-117">-Name</span></span>
<span data-ttu-id="a3b3b-118">Nome da conta de âncoras espaciais.</span><span class="sxs-lookup"><span data-stu-id="a3b3b-118">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="a3b3b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3b3b-119">-ResourceGroupName</span></span>
<span data-ttu-id="a3b3b-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a3b3b-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="a3b3b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3b3b-121">-WhatIf</span></span>
<span data-ttu-id="a3b3b-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3b3b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3b3b-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3b3b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3b3b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b3b-124">CommonParameters</span></span>
<span data-ttu-id="a3b3b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3b3b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a3b3b-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3b3b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b3b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3b3b-127">INPUTS</span></span>

### <span data-ttu-id="a3b3b-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a3b3b-128">None</span></span>

## <span data-ttu-id="a3b3b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3b3b-129">OUTPUTS</span></span>

### <span data-ttu-id="a3b3b-130">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="a3b3b-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="a3b3b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3b3b-131">NOTES</span></span>

## <span data-ttu-id="a3b3b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3b3b-132">RELATED LINKS</span></span>
