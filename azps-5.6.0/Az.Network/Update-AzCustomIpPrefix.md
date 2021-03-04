---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 9d0bca8be88c0448916df27544ce35bf7a6ddee1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885349"
---
# <span data-ttu-id="49874-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="49874-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="49874-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49874-102">SYNOPSIS</span></span>
<span data-ttu-id="49874-103">Atualiza um CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="49874-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="49874-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="49874-104">SYNTAX</span></span>

### <span data-ttu-id="49874-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="49874-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49874-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49874-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49874-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49874-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49874-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="49874-108">DESCRIPTION</span></span>
<span data-ttu-id="49874-109">O cmdlet **Update-AzCustomIpPrefix** permite que o usuário comissione ou desative seu CustomIpPrefix ou edite as marcas do recurso.</span><span class="sxs-lookup"><span data-stu-id="49874-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="49874-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49874-110">EXAMPLES</span></span>

### <span data-ttu-id="49874-111">Exemplo 1 : Comissionar o CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="49874-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="49874-112">O comando acima iniciará o processo de comissionamento do CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="49874-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="49874-113">Exemplo 2 : Descompactar o CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="49874-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="49874-114">O comando acima iniciará o processo de desmissionamento do CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="49874-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="49874-115">Exemplo 3 : Atualizar marcas para o CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="49874-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="49874-116">O comando acima atualizará as marcas do CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="49874-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="49874-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="49874-117">PARAMETERS</span></span>

### <span data-ttu-id="49874-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49874-118">-AsJob</span></span>
<span data-ttu-id="49874-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="49874-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49874-120">-Commission</span><span class="sxs-lookup"><span data-stu-id="49874-120">-Commission</span></span>
<span data-ttu-id="49874-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="49874-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49874-122">-Decomission</span><span class="sxs-lookup"><span data-stu-id="49874-122">-Decomission</span></span>
<span data-ttu-id="49874-123">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="49874-123">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49874-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49874-124">-DefaultProfile</span></span>
<span data-ttu-id="49874-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49874-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49874-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49874-126">-InputObject</span></span>
<span data-ttu-id="49874-127">O CustomIpPrefix a ser definido.</span><span class="sxs-lookup"><span data-stu-id="49874-127">The CustomIpPrefix to set.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49874-128">-Name</span><span class="sxs-lookup"><span data-stu-id="49874-128">-Name</span></span>
<span data-ttu-id="49874-129">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="49874-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49874-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49874-130">-ResourceGroupName</span></span>
<span data-ttu-id="49874-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="49874-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49874-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49874-132">-ResourceId</span></span>
<span data-ttu-id="49874-133">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="49874-133">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49874-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="49874-134">-Tag</span></span>
<span data-ttu-id="49874-135">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="49874-135">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: SetByInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49874-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49874-136">-Confirm</span></span>
<span data-ttu-id="49874-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49874-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49874-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49874-138">-WhatIf</span></span>
<span data-ttu-id="49874-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="49874-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49874-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="49874-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49874-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49874-141">CommonParameters</span></span>
<span data-ttu-id="49874-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49874-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49874-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49874-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49874-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49874-144">INPUTS</span></span>

### <span data-ttu-id="49874-145">System.String</span><span class="sxs-lookup"><span data-stu-id="49874-145">System.String</span></span>

### <span data-ttu-id="49874-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="49874-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="49874-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="49874-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="49874-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="49874-148">OUTPUTS</span></span>

### <span data-ttu-id="49874-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="49874-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="49874-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="49874-150">NOTES</span></span>

## <span data-ttu-id="49874-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49874-151">RELATED LINKS</span></span>

[<span data-ttu-id="49874-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="49874-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="49874-153">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="49874-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="49874-154">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="49874-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)