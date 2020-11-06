---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/remove-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
ms.openlocfilehash: c558a5d7228253e0a76b0d47fb21f581b4e06f11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432259"
---
# <span data-ttu-id="96ecb-101">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="96ecb-101">Remove-AzureRmSearchService</span></span>

## <span data-ttu-id="96ecb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="96ecb-103">Remover um serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="96ecb-103">Remove an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96ecb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96ecb-104">SYNTAX</span></span>

### <span data-ttu-id="96ecb-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="96ecb-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96ecb-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96ecb-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96ecb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96ecb-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSearchService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96ecb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="96ecb-108">DESCRIPTION</span></span>
<span data-ttu-id="96ecb-109">O cmdlet **Remove-AzureRmSearchService** remove um serviço de pesquisa do Azure com o paramters especificado.</span><span class="sxs-lookup"><span data-stu-id="96ecb-109">The **Remove-AzureRmSearchService** cmdlet removes an Azure Search service with specified paramters.</span></span>

## <span data-ttu-id="96ecb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96ecb-110">EXAMPLES</span></span>

### <span data-ttu-id="96ecb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="96ecb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="96ecb-112">O exemplo remove um serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="96ecb-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="96ecb-113">OS</span><span class="sxs-lookup"><span data-stu-id="96ecb-113">PARAMETERS</span></span>

### <span data-ttu-id="96ecb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96ecb-114">-DefaultProfile</span></span>
<span data-ttu-id="96ecb-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96ecb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ecb-116">-Force</span><span class="sxs-lookup"><span data-stu-id="96ecb-116">-Force</span></span>
<span data-ttu-id="96ecb-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="96ecb-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="96ecb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96ecb-118">-InputObject</span></span>
<span data-ttu-id="96ecb-119">Objeto de entrada do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="96ecb-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96ecb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="96ecb-120">-Name</span></span>
<span data-ttu-id="96ecb-121">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="96ecb-121">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ecb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96ecb-122">-PassThru</span></span>
<span data-ttu-id="96ecb-123">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="96ecb-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="96ecb-124">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="96ecb-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="96ecb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96ecb-125">-ResourceGroupName</span></span>
<span data-ttu-id="96ecb-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="96ecb-126">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ecb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96ecb-127">-ResourceId</span></span>
<span data-ttu-id="96ecb-128">ID do recurso do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="96ecb-128">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96ecb-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="96ecb-129">-Confirm</span></span>
<span data-ttu-id="96ecb-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96ecb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96ecb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96ecb-131">-WhatIf</span></span>
<span data-ttu-id="96ecb-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="96ecb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96ecb-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96ecb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96ecb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96ecb-134">CommonParameters</span></span>
<span data-ttu-id="96ecb-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96ecb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96ecb-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96ecb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96ecb-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="96ecb-137">INPUTS</span></span>

### <span data-ttu-id="96ecb-138">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="96ecb-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="96ecb-139">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="96ecb-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="96ecb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="96ecb-140">System.String</span></span>

## <span data-ttu-id="96ecb-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="96ecb-141">OUTPUTS</span></span>

### <span data-ttu-id="96ecb-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96ecb-142">System.Boolean</span></span>

## <span data-ttu-id="96ecb-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="96ecb-143">NOTES</span></span>

## <span data-ttu-id="96ecb-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96ecb-144">RELATED LINKS</span></span>

[<span data-ttu-id="96ecb-145">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="96ecb-145">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="96ecb-146">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="96ecb-146">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="96ecb-147">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="96ecb-147">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)
