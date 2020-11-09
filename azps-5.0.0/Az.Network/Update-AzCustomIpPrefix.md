---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 65d47c57720e66ecad8267ae45f9e08eb3e4c4ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284056"
---
# <span data-ttu-id="6c08b-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6c08b-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="6c08b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c08b-102">SYNOPSIS</span></span>
<span data-ttu-id="6c08b-103">Atualiza um CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6c08b-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="6c08b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c08b-104">SYNTAX</span></span>

### <span data-ttu-id="6c08b-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c08b-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c08b-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c08b-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c08b-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c08b-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c08b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6c08b-108">DESCRIPTION</span></span>
<span data-ttu-id="6c08b-109">O cmdlet **Update-AzCustomIpPrefix** permite que o usuário use a Comissão ou a descomissionação de seu CustomIpPrefix ou edite as marcas do recurso.</span><span class="sxs-lookup"><span data-stu-id="6c08b-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="6c08b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c08b-110">EXAMPLES</span></span>

### <span data-ttu-id="6c08b-111">Exemplo 1: Commission a CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6c08b-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="6c08b-112">O comando acima iniciará o processo de comissões do CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="6c08b-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="6c08b-113">Exemplo 2: encerrar o CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6c08b-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="6c08b-114">O comando acima iniciará o processo de descomissionamento do CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="6c08b-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="6c08b-115">Exemplo 3: atualizar marcas para o CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6c08b-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="6c08b-116">O comando acima atualizará as marcas para o CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="6c08b-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="6c08b-117">OS</span><span class="sxs-lookup"><span data-stu-id="6c08b-117">PARAMETERS</span></span>

### <span data-ttu-id="6c08b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c08b-118">-AsJob</span></span>
<span data-ttu-id="6c08b-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6c08b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c08b-120">-Commission</span><span class="sxs-lookup"><span data-stu-id="6c08b-120">-Commission</span></span>
<span data-ttu-id="6c08b-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6c08b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c08b-122">-Decomission</span><span class="sxs-lookup"><span data-stu-id="6c08b-122">-Decomission</span></span>
<span data-ttu-id="6c08b-123">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6c08b-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c08b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c08b-124">-DefaultProfile</span></span>
<span data-ttu-id="6c08b-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6c08b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c08b-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c08b-126">-InputObject</span></span>
<span data-ttu-id="6c08b-127">O CustomIpPrefix a ser definido.</span><span class="sxs-lookup"><span data-stu-id="6c08b-127">The CustomIpPrefix to set.</span></span>

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

### <span data-ttu-id="6c08b-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c08b-128">-Name</span></span>
<span data-ttu-id="6c08b-129">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="6c08b-129">The resource name.</span></span>

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

### <span data-ttu-id="6c08b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c08b-130">-ResourceGroupName</span></span>
<span data-ttu-id="6c08b-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6c08b-131">The resource group name.</span></span>

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

### <span data-ttu-id="6c08b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c08b-132">-ResourceId</span></span>
<span data-ttu-id="6c08b-133">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="6c08b-133">The resource Id.</span></span>

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

### <span data-ttu-id="6c08b-134">-Marca</span><span class="sxs-lookup"><span data-stu-id="6c08b-134">-Tag</span></span>
<span data-ttu-id="6c08b-135">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="6c08b-135">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6c08b-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6c08b-136">-Confirm</span></span>
<span data-ttu-id="6c08b-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c08b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c08b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c08b-138">-WhatIf</span></span>
<span data-ttu-id="6c08b-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6c08b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c08b-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6c08b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c08b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c08b-141">CommonParameters</span></span>
<span data-ttu-id="6c08b-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c08b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c08b-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c08b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c08b-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6c08b-144">INPUTS</span></span>

### <span data-ttu-id="6c08b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="6c08b-145">System.String</span></span>

### <span data-ttu-id="6c08b-146">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6c08b-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="6c08b-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6c08b-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6c08b-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6c08b-148">OUTPUTS</span></span>

### <span data-ttu-id="6c08b-149">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6c08b-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="6c08b-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6c08b-150">NOTES</span></span>

## <span data-ttu-id="6c08b-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c08b-151">RELATED LINKS</span></span>

[<span data-ttu-id="6c08b-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6c08b-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="6c08b-153">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6c08b-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="6c08b-154">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6c08b-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)