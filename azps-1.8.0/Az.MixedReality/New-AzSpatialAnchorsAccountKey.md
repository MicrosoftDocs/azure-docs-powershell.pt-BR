---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 043b97a256fff50ca9831685a90f0cfb46ff7277
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770353"
---
# <span data-ttu-id="64955-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="64955-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="64955-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64955-102">SYNOPSIS</span></span>
<span data-ttu-id="64955-103">Regenerar chave da conta de âncoras espaciais</span><span class="sxs-lookup"><span data-stu-id="64955-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="64955-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64955-104">SYNTAX</span></span>

### <span data-ttu-id="64955-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="64955-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64955-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="64955-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64955-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="64955-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64955-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="64955-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64955-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="64955-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64955-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="64955-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64955-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64955-111">DESCRIPTION</span></span>
<span data-ttu-id="64955-112">Chave primária de Renegrate ou chave secundária da conta de âncoras espaciais.</span><span class="sxs-lookup"><span data-stu-id="64955-112">Renegrate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="64955-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64955-113">EXAMPLES</span></span>

### <span data-ttu-id="64955-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="64955-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="64955-115">Regenerar a chave secundária da conta de âncoras espaciais "exemplo" no grupo de recursos "Rg1".</span><span class="sxs-lookup"><span data-stu-id="64955-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="64955-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="64955-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="64955-117">Regenerar a chave secundária da conta de âncoras espaciais "exemplo" da assinatura atual e do grupo de recursos "Rg1" com tubulação.</span><span class="sxs-lookup"><span data-stu-id="64955-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="64955-118">OS</span><span class="sxs-lookup"><span data-stu-id="64955-118">PARAMETERS</span></span>

### <span data-ttu-id="64955-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64955-119">-DefaultProfile</span></span>
<span data-ttu-id="64955-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64955-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64955-121">-Force</span><span class="sxs-lookup"><span data-stu-id="64955-121">-Force</span></span>
<span data-ttu-id="64955-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="64955-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64955-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64955-123">-InputObject</span></span>
<span data-ttu-id="64955-124">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="64955-124">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64955-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="64955-125">-Name</span></span>
<span data-ttu-id="64955-126">Nome da conta de âncoras espaciais.</span><span class="sxs-lookup"><span data-stu-id="64955-126">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64955-127">-Principal</span><span class="sxs-lookup"><span data-stu-id="64955-127">-Primary</span></span>
<span data-ttu-id="64955-128">Regenerar a chave primária da conta de âncoras espaciais.</span><span class="sxs-lookup"><span data-stu-id="64955-128">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64955-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64955-129">-ResourceGroupName</span></span>
<span data-ttu-id="64955-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="64955-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64955-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64955-131">-ResourceId</span></span>
<span data-ttu-id="64955-132">ID do recurso da conta de âncoras espaciais.</span><span class="sxs-lookup"><span data-stu-id="64955-132">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64955-133">-Secundário</span><span class="sxs-lookup"><span data-stu-id="64955-133">-Secondary</span></span>
<span data-ttu-id="64955-134">Regenerar a chave primária da conta de âncoras espaciais.</span><span class="sxs-lookup"><span data-stu-id="64955-134">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64955-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="64955-135">-Confirm</span></span>
<span data-ttu-id="64955-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64955-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64955-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64955-137">-WhatIf</span></span>
<span data-ttu-id="64955-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64955-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64955-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64955-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64955-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64955-140">CommonParameters</span></span>
<span data-ttu-id="64955-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64955-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="64955-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64955-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64955-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64955-143">INPUTS</span></span>

### <span data-ttu-id="64955-144">System. String</span><span class="sxs-lookup"><span data-stu-id="64955-144">System.String</span></span>

### <span data-ttu-id="64955-145">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="64955-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="64955-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64955-146">OUTPUTS</span></span>

### <span data-ttu-id="64955-147">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="64955-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccountKeys</span></span>

## <span data-ttu-id="64955-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64955-148">NOTES</span></span>

## <span data-ttu-id="64955-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64955-149">RELATED LINKS</span></span>
