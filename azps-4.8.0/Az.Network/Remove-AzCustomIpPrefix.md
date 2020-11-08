---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: bcb250c8967c10e5b200e62d843e99eab374d81d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114348"
---
# <span data-ttu-id="e2505-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e2505-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="e2505-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2505-102">SYNOPSIS</span></span>
<span data-ttu-id="e2505-103">Remove um CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e2505-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="e2505-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2505-104">SYNTAX</span></span>

### <span data-ttu-id="e2505-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e2505-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2505-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2505-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2505-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2505-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2505-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2505-108">DESCRIPTION</span></span>
<span data-ttu-id="e2505-109">O cmdlet **Remove-AzCustomIpPrefix** remove um CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="e2505-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="e2505-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2505-110">EXAMPLES</span></span>

### <span data-ttu-id="e2505-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e2505-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="e2505-112">Remove o CustomIpPrefix com o nome $prefixName do grupo de recursos $rgName</span><span class="sxs-lookup"><span data-stu-id="e2505-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="e2505-113">OS</span><span class="sxs-lookup"><span data-stu-id="e2505-113">PARAMETERS</span></span>

### <span data-ttu-id="e2505-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2505-114">-AsJob</span></span>
<span data-ttu-id="e2505-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e2505-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2505-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2505-116">-DefaultProfile</span></span>
<span data-ttu-id="e2505-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2505-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2505-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e2505-118">-Force</span></span>
<span data-ttu-id="e2505-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="e2505-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e2505-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2505-120">-InputObject</span></span>
<span data-ttu-id="e2505-121">Um objeto customIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="e2505-121">A customIpPrefix object.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2505-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2505-122">-Name</span></span>
<span data-ttu-id="e2505-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e2505-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2505-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2505-124">-PassThru</span></span>
<span data-ttu-id="e2505-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e2505-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e2505-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e2505-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e2505-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2505-127">-ResourceGroupName</span></span>
<span data-ttu-id="e2505-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e2505-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2505-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2505-129">-ResourceId</span></span>
<span data-ttu-id="e2505-130">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="e2505-130">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2505-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e2505-131">-Confirm</span></span>
<span data-ttu-id="e2505-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2505-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2505-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2505-133">-WhatIf</span></span>
<span data-ttu-id="e2505-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e2505-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2505-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e2505-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2505-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2505-136">CommonParameters</span></span>
<span data-ttu-id="e2505-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2505-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2505-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2505-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2505-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2505-139">INPUTS</span></span>

### <span data-ttu-id="e2505-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e2505-140">System.String</span></span>

### <span data-ttu-id="e2505-141">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e2505-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="e2505-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2505-142">OUTPUTS</span></span>

### <span data-ttu-id="e2505-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2505-143">System.Boolean</span></span>

## <span data-ttu-id="e2505-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2505-144">NOTES</span></span>

## <span data-ttu-id="e2505-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2505-145">RELATED LINKS</span></span>

[<span data-ttu-id="e2505-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e2505-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="e2505-147">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e2505-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="e2505-148">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e2505-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)