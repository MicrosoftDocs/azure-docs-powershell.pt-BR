---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 62b8dff0b2d5fc52b080b35e4a205ad2bb00ea52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943493"
---
# <span data-ttu-id="adb72-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="adb72-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="adb72-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="adb72-102">SYNOPSIS</span></span>
<span data-ttu-id="adb72-103">Remover um serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="adb72-103">Remove an Azure Search service.</span></span>

## <span data-ttu-id="adb72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="adb72-104">SYNTAX</span></span>

### <span data-ttu-id="adb72-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="adb72-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adb72-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adb72-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adb72-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="adb72-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adb72-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="adb72-108">DESCRIPTION</span></span>
<span data-ttu-id="adb72-109">O cmdlet **Remove-AzSearchService** remove um serviço de pesquisa do Azure com parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="adb72-109">The **Remove-AzSearchService** cmdlet removes an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="adb72-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="adb72-110">EXAMPLES</span></span>

### <span data-ttu-id="adb72-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="adb72-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="adb72-112">O exemplo remove um serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="adb72-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="adb72-113">OS</span><span class="sxs-lookup"><span data-stu-id="adb72-113">PARAMETERS</span></span>

### <span data-ttu-id="adb72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb72-114">-DefaultProfile</span></span>
<span data-ttu-id="adb72-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="adb72-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adb72-116">-Force</span><span class="sxs-lookup"><span data-stu-id="adb72-116">-Force</span></span>
<span data-ttu-id="adb72-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="adb72-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="adb72-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adb72-118">-InputObject</span></span>
<span data-ttu-id="adb72-119">Objeto de entrada do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="adb72-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="adb72-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="adb72-120">-Name</span></span>
<span data-ttu-id="adb72-121">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="adb72-121">Search Service name.</span></span>

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

### <span data-ttu-id="adb72-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adb72-122">-PassThru</span></span>
<span data-ttu-id="adb72-123">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="adb72-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="adb72-124">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="adb72-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="adb72-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adb72-125">-ResourceGroupName</span></span>
<span data-ttu-id="adb72-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="adb72-126">Resource Group name.</span></span>

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

### <span data-ttu-id="adb72-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adb72-127">-ResourceId</span></span>
<span data-ttu-id="adb72-128">ID do recurso do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="adb72-128">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="adb72-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="adb72-129">-Confirm</span></span>
<span data-ttu-id="adb72-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adb72-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adb72-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adb72-131">-WhatIf</span></span>
<span data-ttu-id="adb72-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="adb72-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adb72-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="adb72-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adb72-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb72-134">CommonParameters</span></span>
<span data-ttu-id="adb72-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adb72-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb72-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adb72-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb72-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="adb72-137">INPUTS</span></span>

### <span data-ttu-id="adb72-138">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="adb72-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="adb72-139">System. String</span><span class="sxs-lookup"><span data-stu-id="adb72-139">System.String</span></span>

## <span data-ttu-id="adb72-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="adb72-140">OUTPUTS</span></span>

### <span data-ttu-id="adb72-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="adb72-141">System.Boolean</span></span>

## <span data-ttu-id="adb72-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="adb72-142">NOTES</span></span>

## <span data-ttu-id="adb72-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="adb72-143">RELATED LINKS</span></span>

[<span data-ttu-id="adb72-144">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="adb72-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="adb72-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="adb72-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="adb72-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="adb72-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

