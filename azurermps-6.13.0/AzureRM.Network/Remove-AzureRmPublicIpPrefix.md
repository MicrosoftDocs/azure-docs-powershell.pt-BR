---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpPrefix.md
ms.openlocfilehash: e361e4d3c4daec88ddb35fa7973b65f630dcc390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610273"
---
# <span data-ttu-id="0a57f-101">Remove-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0a57f-101">Remove-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="0a57f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a57f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a57f-103">Remove um prefixo de IP público</span><span class="sxs-lookup"><span data-stu-id="0a57f-103">Removes a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a57f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a57f-104">SYNTAX</span></span>

### <span data-ttu-id="0a57f-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a57f-105">RemoveByNameParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a57f-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a57f-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a57f-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a57f-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a57f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0a57f-108">DESCRIPTION</span></span>
<span data-ttu-id="0a57f-109">O cmdlet \* \* Remove-AzureRmPublicIpPrefix remove um prefixo de IP público do Azure desde que não haja endereços IP públicos atribuídos a ele.</span><span class="sxs-lookup"><span data-stu-id="0a57f-109">The \*\*Remove-AzureRmPublicIpPrefix cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="0a57f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a57f-110">EXAMPLES</span></span>

### <span data-ttu-id="0a57f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0a57f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="0a57f-112">Remove o prefixo de IP público com o nome $prefixName do grupo de recursos $rgName</span><span class="sxs-lookup"><span data-stu-id="0a57f-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="0a57f-113">OS</span><span class="sxs-lookup"><span data-stu-id="0a57f-113">PARAMETERS</span></span>

### <span data-ttu-id="0a57f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a57f-114">-AsJob</span></span>
<span data-ttu-id="0a57f-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0a57f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a57f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a57f-116">-DefaultProfile</span></span>
<span data-ttu-id="0a57f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a57f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a57f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0a57f-118">-Force</span></span>
<span data-ttu-id="0a57f-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="0a57f-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0a57f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a57f-120">-InputObject</span></span>
<span data-ttu-id="0a57f-121">Um objeto PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0a57f-121">A PublicIpPrefix object</span></span>

```yaml
Type: PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a57f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a57f-122">-Name</span></span>
<span data-ttu-id="0a57f-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="0a57f-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a57f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a57f-124">-PassThru</span></span>
<span data-ttu-id="0a57f-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="0a57f-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0a57f-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="0a57f-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0a57f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a57f-127">-ResourceGroupName</span></span>
<span data-ttu-id="0a57f-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0a57f-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a57f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a57f-129">-ResourceId</span></span>
<span data-ttu-id="0a57f-130">A ResourceId do recurso a ser removido</span><span class="sxs-lookup"><span data-stu-id="0a57f-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="0a57f-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0a57f-131">-Confirm</span></span>
<span data-ttu-id="0a57f-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a57f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a57f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a57f-133">-WhatIf</span></span>
<span data-ttu-id="0a57f-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0a57f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a57f-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0a57f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a57f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a57f-136">CommonParameters</span></span>
<span data-ttu-id="0a57f-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a57f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0a57f-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a57f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a57f-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0a57f-139">INPUTS</span></span>

### <span data-ttu-id="0a57f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0a57f-140">System.String</span></span>
<span data-ttu-id="0a57f-141">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0a57f-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="0a57f-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0a57f-142">OUTPUTS</span></span>

### <span data-ttu-id="0a57f-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="0a57f-143">System.Object</span></span>

## <span data-ttu-id="0a57f-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0a57f-144">NOTES</span></span>

## <span data-ttu-id="0a57f-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a57f-145">RELATED LINKS</span></span>
