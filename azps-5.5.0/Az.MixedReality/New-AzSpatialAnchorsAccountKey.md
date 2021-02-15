---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 35c00fca10223a22d586efba8961dd9cab6b0faf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112971"
---
# <span data-ttu-id="837c2-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="837c2-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="837c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="837c2-102">SYNOPSIS</span></span>
<span data-ttu-id="837c2-103">Regenerar a chave da Conta de Âncoras DeSarmado</span><span class="sxs-lookup"><span data-stu-id="837c2-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="837c2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="837c2-104">SYNTAX</span></span>

### <span data-ttu-id="837c2-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="837c2-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="837c2-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="837c2-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="837c2-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="837c2-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="837c2-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="837c2-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="837c2-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="837c2-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="837c2-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="837c2-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="837c2-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="837c2-111">DESCRIPTION</span></span>
<span data-ttu-id="837c2-112">Regenerar a chave primária ou a chave secundária da Conta de Âncoras Desamarradas.</span><span class="sxs-lookup"><span data-stu-id="837c2-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="837c2-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="837c2-113">EXAMPLES</span></span>

### <span data-ttu-id="837c2-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="837c2-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="837c2-115">Regenerar a chave secundária da conta de âncoras de espaço reservado "exemplo" no Grupo de Recursos "rg1".</span><span class="sxs-lookup"><span data-stu-id="837c2-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="837c2-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="837c2-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="837c2-117">Regenerar a chave secundária da Conta de Âncoras Espaciais "exemplo" da assinatura atual e grupo de recursos "rg1" com cana.</span><span class="sxs-lookup"><span data-stu-id="837c2-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="837c2-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="837c2-118">PARAMETERS</span></span>

### <span data-ttu-id="837c2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="837c2-119">-DefaultProfile</span></span>
<span data-ttu-id="837c2-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="837c2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="837c2-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="837c2-121">-Force</span></span>
<span data-ttu-id="837c2-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="837c2-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="837c2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="837c2-123">-InputObject</span></span>
<span data-ttu-id="837c2-124">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="837c2-124">The custom domain object.</span></span>

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

### <span data-ttu-id="837c2-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="837c2-125">-Name</span></span>
<span data-ttu-id="837c2-126">Nome da conta De âncoras de espaço.</span><span class="sxs-lookup"><span data-stu-id="837c2-126">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="837c2-127">-Principal</span><span class="sxs-lookup"><span data-stu-id="837c2-127">-Primary</span></span>
<span data-ttu-id="837c2-128">Regenerar a chave primária da Conta de Âncoras Espaciais.</span><span class="sxs-lookup"><span data-stu-id="837c2-128">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="837c2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="837c2-129">-ResourceGroupName</span></span>
<span data-ttu-id="837c2-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="837c2-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="837c2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="837c2-131">-ResourceId</span></span>
<span data-ttu-id="837c2-132">ID do Recurso da Conta de Âncoras Desarmada.</span><span class="sxs-lookup"><span data-stu-id="837c2-132">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="837c2-133">-Secundário</span><span class="sxs-lookup"><span data-stu-id="837c2-133">-Secondary</span></span>
<span data-ttu-id="837c2-134">Regenerar a chave primária da Conta de Âncoras Espaciais.</span><span class="sxs-lookup"><span data-stu-id="837c2-134">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="837c2-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="837c2-135">-Confirm</span></span>
<span data-ttu-id="837c2-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="837c2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="837c2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="837c2-137">-WhatIf</span></span>
<span data-ttu-id="837c2-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="837c2-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="837c2-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="837c2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="837c2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="837c2-140">CommonParameters</span></span>
<span data-ttu-id="837c2-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="837c2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="837c2-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="837c2-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="837c2-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="837c2-143">INPUTS</span></span>

### <span data-ttu-id="837c2-144">System.String</span><span class="sxs-lookup"><span data-stu-id="837c2-144">System.String</span></span>

### <span data-ttu-id="837c2-145">Microsoft.Azure.Commands.MixedReality.GeoespaciaisAccount.PSSárialEstaresAccount</span><span class="sxs-lookup"><span data-stu-id="837c2-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="837c2-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="837c2-146">OUTPUTS</span></span>

### <span data-ttu-id="837c2-147">Microsoft.Azure.Commands.MixedReality.SpatialKeyrsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="837c2-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="837c2-148">Notas</span><span class="sxs-lookup"><span data-stu-id="837c2-148">NOTES</span></span>

## <span data-ttu-id="837c2-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="837c2-149">RELATED LINKS</span></span>
