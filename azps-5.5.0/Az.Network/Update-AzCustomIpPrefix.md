---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 65d47c57720e66ecad8267ae45f9e08eb3e4c4ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117308"
---
# <span data-ttu-id="885b3-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="885b3-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="885b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="885b3-102">SYNOPSIS</span></span>
<span data-ttu-id="885b3-103">Atualiza um CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="885b3-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="885b3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="885b3-104">SYNTAX</span></span>

### <span data-ttu-id="885b3-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="885b3-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="885b3-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="885b3-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="885b3-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="885b3-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="885b3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="885b3-108">DESCRIPTION</span></span>
<span data-ttu-id="885b3-109">O cmdlet **Update-AzCustomIpPrefix** permite que o usuário comissione ou desative seu CustomIpPrefix ou edite as marcas do recurso.</span><span class="sxs-lookup"><span data-stu-id="885b3-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="885b3-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="885b3-110">EXAMPLES</span></span>

### <span data-ttu-id="885b3-111">Exemplo 1: comissão do CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="885b3-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="885b3-112">O comando acima iniciará o processo de comissionamento do CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="885b3-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="885b3-113">Exemplo 2: Desative o CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="885b3-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="885b3-114">O comando acima iniciará o processo de desem comissão do CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="885b3-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="885b3-115">Exemplo 3: Atualizar marcas para o CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="885b3-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="885b3-116">O comando acima atualizará as marcas do CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="885b3-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="885b3-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="885b3-117">PARAMETERS</span></span>

### <span data-ttu-id="885b3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="885b3-118">-AsJob</span></span>
<span data-ttu-id="885b3-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="885b3-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="885b3-120">-Comissão</span><span class="sxs-lookup"><span data-stu-id="885b3-120">-Commission</span></span>
<span data-ttu-id="885b3-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="885b3-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="885b3-122">-Decomission</span><span class="sxs-lookup"><span data-stu-id="885b3-122">-Decomission</span></span>
<span data-ttu-id="885b3-123">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="885b3-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="885b3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="885b3-124">-DefaultProfile</span></span>
<span data-ttu-id="885b3-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="885b3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="885b3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="885b3-126">-InputObject</span></span>
<span data-ttu-id="885b3-127">O CustomIpPrefix a ser definido.</span><span class="sxs-lookup"><span data-stu-id="885b3-127">The CustomIpPrefix to set.</span></span>

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

### <span data-ttu-id="885b3-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="885b3-128">-Name</span></span>
<span data-ttu-id="885b3-129">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="885b3-129">The resource name.</span></span>

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

### <span data-ttu-id="885b3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="885b3-130">-ResourceGroupName</span></span>
<span data-ttu-id="885b3-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="885b3-131">The resource group name.</span></span>

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

### <span data-ttu-id="885b3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="885b3-132">-ResourceId</span></span>
<span data-ttu-id="885b3-133">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="885b3-133">The resource Id.</span></span>

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

### <span data-ttu-id="885b3-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="885b3-134">-Tag</span></span>
<span data-ttu-id="885b3-135">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="885b3-135">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="885b3-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="885b3-136">-Confirm</span></span>
<span data-ttu-id="885b3-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="885b3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="885b3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="885b3-138">-WhatIf</span></span>
<span data-ttu-id="885b3-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="885b3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="885b3-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="885b3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="885b3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="885b3-141">CommonParameters</span></span>
<span data-ttu-id="885b3-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="885b3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="885b3-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="885b3-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="885b3-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="885b3-144">INPUTS</span></span>

### <span data-ttu-id="885b3-145">System.String</span><span class="sxs-lookup"><span data-stu-id="885b3-145">System.String</span></span>

### <span data-ttu-id="885b3-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="885b3-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="885b3-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="885b3-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="885b3-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="885b3-148">OUTPUTS</span></span>

### <span data-ttu-id="885b3-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="885b3-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="885b3-150">Notas</span><span class="sxs-lookup"><span data-stu-id="885b3-150">NOTES</span></span>

## <span data-ttu-id="885b3-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="885b3-151">RELATED LINKS</span></span>

[<span data-ttu-id="885b3-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="885b3-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="885b3-153">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="885b3-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="885b3-154">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="885b3-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)