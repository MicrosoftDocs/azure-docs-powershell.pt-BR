---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: a34754e0032f2dc8b833eb6b03de6e97ab5486fe
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776404"
---
# <span data-ttu-id="089dc-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="089dc-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="089dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="089dc-102">SYNOPSIS</span></span>
<span data-ttu-id="089dc-103">Cria um aplicativo gerenciado do Azure.</span><span class="sxs-lookup"><span data-stu-id="089dc-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="089dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="089dc-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="089dc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="089dc-105">DESCRIPTION</span></span>
<span data-ttu-id="089dc-106">O cmdlet **New-AzManagedApplication** cria um aplicativo gerenciado do Azure.</span><span class="sxs-lookup"><span data-stu-id="089dc-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="089dc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="089dc-107">EXAMPLES</span></span>

### <span data-ttu-id="089dc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="089dc-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="089dc-109">Este comando cria um aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="089dc-109">This command creates a managed application</span></span>

## <span data-ttu-id="089dc-110">OS</span><span class="sxs-lookup"><span data-stu-id="089dc-110">PARAMETERS</span></span>

### <span data-ttu-id="089dc-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="089dc-111">-ApiVersion</span></span>
<span data-ttu-id="089dc-112">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="089dc-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="089dc-113">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="089dc-113">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="089dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="089dc-114">-DefaultProfile</span></span>
<span data-ttu-id="089dc-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="089dc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="089dc-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="089dc-116">-Kind</span></span>
<span data-ttu-id="089dc-117">O tipo de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="089dc-117">The managed application kind.</span></span>
<span data-ttu-id="089dc-118">Um dos Marketplaces ou catálogos</span><span class="sxs-lookup"><span data-stu-id="089dc-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="089dc-119">-Local</span><span class="sxs-lookup"><span data-stu-id="089dc-119">-Location</span></span>
<span data-ttu-id="089dc-120">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="089dc-120">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="089dc-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="089dc-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="089dc-122">O nome do grupo de recursos gerenciado.</span><span class="sxs-lookup"><span data-stu-id="089dc-122">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089dc-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="089dc-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="089dc-124">O nome do grupo de recursos gerenciado.</span><span class="sxs-lookup"><span data-stu-id="089dc-124">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089dc-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="089dc-125">-Name</span></span>
<span data-ttu-id="089dc-126">O nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="089dc-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089dc-127">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="089dc-127">-Parameter</span></span>
<span data-ttu-id="089dc-128">A cadeia de caracteres de parâmetros da JSON formatada para o aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="089dc-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="089dc-129">Isso pode ser um caminho para um nome de arquivo ou URI que contém os parâmetros ou os parâmetros como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="089dc-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089dc-130">-Plano</span><span class="sxs-lookup"><span data-stu-id="089dc-130">-Plan</span></span>
<span data-ttu-id="089dc-131">Uma tabela de hash que representa as propriedades do plano de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="089dc-131">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="089dc-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="089dc-132">-Pre</span></span>
<span data-ttu-id="089dc-133">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="089dc-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="089dc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="089dc-134">-ResourceGroupName</span></span>
<span data-ttu-id="089dc-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="089dc-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089dc-136">-Marca</span><span class="sxs-lookup"><span data-stu-id="089dc-136">-Tag</span></span>
<span data-ttu-id="089dc-137">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="089dc-137">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089dc-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="089dc-138">-Confirm</span></span>
<span data-ttu-id="089dc-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="089dc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="089dc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="089dc-140">-WhatIf</span></span>
<span data-ttu-id="089dc-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="089dc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="089dc-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="089dc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="089dc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="089dc-143">CommonParameters</span></span>
<span data-ttu-id="089dc-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="089dc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="089dc-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="089dc-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="089dc-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="089dc-146">INPUTS</span></span>

### <span data-ttu-id="089dc-147">System. String</span><span class="sxs-lookup"><span data-stu-id="089dc-147">System.String</span></span>

### <span data-ttu-id="089dc-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="089dc-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="089dc-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="089dc-149">OUTPUTS</span></span>

### <span data-ttu-id="089dc-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="089dc-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="089dc-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="089dc-151">NOTES</span></span>

## <span data-ttu-id="089dc-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="089dc-152">RELATED LINKS</span></span>
