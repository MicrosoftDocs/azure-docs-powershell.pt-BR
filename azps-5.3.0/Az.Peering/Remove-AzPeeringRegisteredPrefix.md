---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: b3d505d7c9412b15c2933ec03bb66af6f43a6b26
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272528"
---
# <span data-ttu-id="ababb-101">Remove-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="ababb-101">Remove-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="ababb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ababb-102">SYNOPSIS</span></span>
<span data-ttu-id="ababb-103">Exclua ou remova um prefixo registrado do recurso de emparelhamento pai.</span><span class="sxs-lookup"><span data-stu-id="ababb-103">Delete or remove a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="ababb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ababb-104">SYNTAX</span></span>

### <span data-ttu-id="ababb-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ababb-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ababb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ababb-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredPrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ababb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ababb-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ababb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ababb-108">DESCRIPTION</span></span>
<span data-ttu-id="ababb-109">Permite a remoção de prefixo registrado do recurso de emparelhamento pai.</span><span class="sxs-lookup"><span data-stu-id="ababb-109">Allows the removal of registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="ababb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ababb-110">EXAMPLES</span></span>

### <span data-ttu-id="ababb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ababb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredPrefix -ResourceId $resourceId
```

<span data-ttu-id="ababb-112">Remover um prefixo registrado por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="ababb-112">Remove a registerd prefix by resource id.</span></span>

## <span data-ttu-id="ababb-113">OS</span><span class="sxs-lookup"><span data-stu-id="ababb-113">PARAMETERS</span></span>

### <span data-ttu-id="ababb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ababb-114">-AsJob</span></span>
<span data-ttu-id="ababb-115">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="ababb-115">Run in the background.</span></span>

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

### <span data-ttu-id="ababb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ababb-116">-DefaultProfile</span></span>
<span data-ttu-id="ababb-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ababb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ababb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ababb-118">-Force</span></span>
<span data-ttu-id="ababb-119">Forçar a conclusão da operação</span><span class="sxs-lookup"><span data-stu-id="ababb-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="ababb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ababb-120">-InputObject</span></span>
<span data-ttu-id="ababb-121">Usar uma Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="ababb-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ababb-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ababb-122">-Name</span></span>
<span data-ttu-id="ababb-123">O nome do prefixo.</span><span class="sxs-lookup"><span data-stu-id="ababb-123">The name of prefix.</span></span>

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

### <span data-ttu-id="ababb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ababb-124">-PassThru</span></span>
<span data-ttu-id="ababb-125">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="ababb-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ababb-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="ababb-126">-PeeringName</span></span>
<span data-ttu-id="ababb-127">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="ababb-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="ababb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ababb-128">-ResourceGroupName</span></span>
<span data-ttu-id="ababb-129">Criar ou usar um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="ababb-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="ababb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ababb-130">-ResourceId</span></span>
<span data-ttu-id="ababb-131">O nome da cadeia de caracteres da ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="ababb-131">The resource id string name.</span></span>

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

### <span data-ttu-id="ababb-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ababb-132">-Confirm</span></span>
<span data-ttu-id="ababb-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ababb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ababb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ababb-134">-WhatIf</span></span>
<span data-ttu-id="ababb-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ababb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ababb-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ababb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ababb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ababb-137">CommonParameters</span></span>
<span data-ttu-id="ababb-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ababb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ababb-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ababb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ababb-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ababb-140">INPUTS</span></span>

### <span data-ttu-id="ababb-141">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="ababb-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="ababb-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ababb-142">System.String</span></span>

## <span data-ttu-id="ababb-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ababb-143">OUTPUTS</span></span>

### <span data-ttu-id="ababb-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ababb-144">System.Boolean</span></span>

## <span data-ttu-id="ababb-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ababb-145">NOTES</span></span>

## <span data-ttu-id="ababb-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ababb-146">RELATED LINKS</span></span>
