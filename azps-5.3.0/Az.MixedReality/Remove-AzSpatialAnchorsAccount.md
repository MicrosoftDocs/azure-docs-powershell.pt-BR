---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 5ba079a17dcfb0a263766237adbbec9beb4cc64c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429483"
---
# <span data-ttu-id="3d622-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="3d622-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="3d622-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d622-102">SYNOPSIS</span></span>
<span data-ttu-id="3d622-103">Excluir conta de âncoras espaciais</span><span class="sxs-lookup"><span data-stu-id="3d622-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="3d622-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d622-104">SYNTAX</span></span>

### <span data-ttu-id="3d622-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3d622-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d622-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d622-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d622-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d622-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d622-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d622-108">DESCRIPTION</span></span>
<span data-ttu-id="3d622-109">Excluir a conta de âncoras espaciais especificadas de determinada assinatura e grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d622-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="3d622-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d622-110">EXAMPLES</span></span>

### <span data-ttu-id="3d622-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3d622-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="3d622-112">Excluir uma conta de âncora espacial "exemplo" da assinatura atual e do grupo de recursos "Rg1".</span><span class="sxs-lookup"><span data-stu-id="3d622-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="3d622-113">OS</span><span class="sxs-lookup"><span data-stu-id="3d622-113">PARAMETERS</span></span>

### <span data-ttu-id="3d622-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d622-114">-Confirm</span></span>
<span data-ttu-id="3d622-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d622-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d622-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d622-116">-DefaultProfile</span></span>
<span data-ttu-id="3d622-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d622-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d622-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d622-118">-InputObject</span></span>
<span data-ttu-id="3d622-119">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="3d622-119">The custom domain object.</span></span>

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

### <span data-ttu-id="3d622-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d622-120">-Name</span></span>
<span data-ttu-id="3d622-121">Nome da conta de âncoras espaciais.</span><span class="sxs-lookup"><span data-stu-id="3d622-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="3d622-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d622-122">-PassThru</span></span>
<span data-ttu-id="3d622-123">Objeto de retorno, se especificado.</span><span class="sxs-lookup"><span data-stu-id="3d622-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d622-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d622-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d622-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d622-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="3d622-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d622-126">-ResourceId</span></span>
<span data-ttu-id="3d622-127">ID do recurso da conta de âncoras espaciais.</span><span class="sxs-lookup"><span data-stu-id="3d622-127">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="3d622-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d622-128">-WhatIf</span></span>
<span data-ttu-id="3d622-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d622-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d622-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d622-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d622-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d622-131">CommonParameters</span></span>
<span data-ttu-id="3d622-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d622-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3d622-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d622-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d622-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d622-134">INPUTS</span></span>

### <span data-ttu-id="3d622-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3d622-135">System.String</span></span>

### <span data-ttu-id="3d622-136">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="3d622-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="3d622-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3d622-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3d622-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d622-138">OUTPUTS</span></span>

### <span data-ttu-id="3d622-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3d622-139">System.Boolean</span></span>

## <span data-ttu-id="3d622-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d622-140">NOTES</span></span>

## <span data-ttu-id="3d622-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d622-141">RELATED LINKS</span></span>
