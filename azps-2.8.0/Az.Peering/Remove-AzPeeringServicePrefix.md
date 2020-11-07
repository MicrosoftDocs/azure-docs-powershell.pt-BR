---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 36003d1fbca7566ae663a1d878386f3d8d67f484
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772839"
---
# <span data-ttu-id="d96bb-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="d96bb-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="d96bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d96bb-102">SYNOPSIS</span></span>
<span data-ttu-id="d96bb-103">Remove um novo prefixo de serviço de emparelhamento</span><span class="sxs-lookup"><span data-stu-id="d96bb-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="d96bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d96bb-104">SYNTAX</span></span>

### <span data-ttu-id="d96bb-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d96bb-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PeeringServiceName] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d96bb-106">Assume</span><span class="sxs-lookup"><span data-stu-id="d96bb-106">Default</span></span>
```
Remove-AzPeeringServicePrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d96bb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d96bb-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d96bb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d96bb-108">DESCRIPTION</span></span>
<span data-ttu-id="d96bb-109">Remove um prefixo de serviço de emparelhamento de um serviço de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="d96bb-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="d96bb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d96bb-110">EXAMPLES</span></span>

### <span data-ttu-id="d96bb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d96bb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="d96bb-112">Remover um prefixo de um objeto de serviço de emparelhamento</span><span class="sxs-lookup"><span data-stu-id="d96bb-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="d96bb-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d96bb-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="d96bb-114">Remover um prefixo de uma ID de recurso do serviço de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="d96bb-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="d96bb-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d96bb-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="d96bb-116">Remover um prefixo de um nome e nome de grupo de recursos de serviço de correspondência</span><span class="sxs-lookup"><span data-stu-id="d96bb-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="d96bb-117">OS</span><span class="sxs-lookup"><span data-stu-id="d96bb-117">PARAMETERS</span></span>

### <span data-ttu-id="d96bb-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d96bb-118">-AsJob</span></span>
<span data-ttu-id="d96bb-119">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="d96bb-119">Run in the background.</span></span>

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

### <span data-ttu-id="d96bb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d96bb-120">-DefaultProfile</span></span>
<span data-ttu-id="d96bb-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d96bb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d96bb-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d96bb-122">-Force</span></span>
<span data-ttu-id="d96bb-123">Forçar a conclusão da operação</span><span class="sxs-lookup"><span data-stu-id="d96bb-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="d96bb-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d96bb-124">-InputObject</span></span>
<span data-ttu-id="d96bb-125">Usar uma Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="d96bb-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d96bb-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="d96bb-126">-Name</span></span>
<span data-ttu-id="d96bb-127">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="d96bb-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d96bb-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d96bb-128">-PassThru</span></span>
<span data-ttu-id="d96bb-129">Retorna verdadeiro para êxito ou falso para falha.</span><span class="sxs-lookup"><span data-stu-id="d96bb-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="d96bb-130">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="d96bb-130">-PeeringServiceName</span></span>
<span data-ttu-id="d96bb-131">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="d96bb-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d96bb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d96bb-132">-ResourceGroupName</span></span>
<span data-ttu-id="d96bb-133">Criar ou usar um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="d96bb-133">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d96bb-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d96bb-134">-ResourceId</span></span>
<span data-ttu-id="d96bb-135">O nome da cadeia de caracteres da ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="d96bb-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d96bb-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d96bb-136">-Confirm</span></span>
<span data-ttu-id="d96bb-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d96bb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d96bb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d96bb-138">-WhatIf</span></span>
<span data-ttu-id="d96bb-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d96bb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d96bb-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d96bb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d96bb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d96bb-141">CommonParameters</span></span>
<span data-ttu-id="d96bb-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d96bb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d96bb-143">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d96bb-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d96bb-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d96bb-144">INPUTS</span></span>

### <span data-ttu-id="d96bb-145">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="d96bb-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="d96bb-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d96bb-146">System.String</span></span>

## <span data-ttu-id="d96bb-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d96bb-147">OUTPUTS</span></span>

### <span data-ttu-id="d96bb-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d96bb-148">System.Boolean</span></span>

## <span data-ttu-id="d96bb-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d96bb-149">NOTES</span></span>

## <span data-ttu-id="d96bb-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d96bb-150">RELATED LINKS</span></span>
