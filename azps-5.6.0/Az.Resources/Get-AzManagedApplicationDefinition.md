---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: f1f71d188a6b25146103fe3fe5d91b8ba53eaaf8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889613"
---
# <span data-ttu-id="06af5-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="06af5-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="06af5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06af5-102">SYNOPSIS</span></span>
<span data-ttu-id="06af5-103">Obtém definições de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="06af5-103">Gets managed application definitions</span></span>

## <span data-ttu-id="06af5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="06af5-104">SYNTAX</span></span>

### <span data-ttu-id="06af5-105">GetByNameAndResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="06af5-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06af5-106">GetById</span><span class="sxs-lookup"><span data-stu-id="06af5-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06af5-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="06af5-107">DESCRIPTION</span></span>
<span data-ttu-id="06af5-108">O cmdlet **Get-AzManagedApplicationDefinition obtém** definições de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="06af5-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="06af5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06af5-109">EXAMPLES</span></span>

### <span data-ttu-id="06af5-110">Exemplo 1: Obter todas as definições de aplicativos gerenciados em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="06af5-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="06af5-111">Este comando obtém as definições de aplicativo gerenciado no grupo de recursos "MyRG"</span><span class="sxs-lookup"><span data-stu-id="06af5-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="06af5-112">Exemplo 2: Obter uma definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="06af5-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="06af5-113">Este comando obtém a definição de aplicativo gerenciado "myManagedAppDef" no grupo de recursos "MyRG"</span><span class="sxs-lookup"><span data-stu-id="06af5-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="06af5-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="06af5-114">PARAMETERS</span></span>

### <span data-ttu-id="06af5-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="06af5-115">-ApiVersion</span></span>
<span data-ttu-id="06af5-116">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="06af5-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="06af5-117">Se não for especificada, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="06af5-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="06af5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06af5-118">-DefaultProfile</span></span>
<span data-ttu-id="06af5-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="06af5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06af5-120">-Id</span><span class="sxs-lookup"><span data-stu-id="06af5-120">-Id</span></span>
<span data-ttu-id="06af5-121">A ID de definição de aplicativo gerenciado totalmente qualificado, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="06af5-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="06af5-122">por exemplo, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="06af5-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06af5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="06af5-123">-Name</span></span>
<span data-ttu-id="06af5-124">O nome da definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="06af5-124">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06af5-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="06af5-125">-Pre</span></span>
<span data-ttu-id="06af5-126">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="06af5-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="06af5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06af5-127">-ResourceGroupName</span></span>
<span data-ttu-id="06af5-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="06af5-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06af5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06af5-129">CommonParameters</span></span>
<span data-ttu-id="06af5-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06af5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06af5-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06af5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06af5-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06af5-132">INPUTS</span></span>

### <span data-ttu-id="06af5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="06af5-133">System.String</span></span>

## <span data-ttu-id="06af5-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="06af5-134">OUTPUTS</span></span>

### <span data-ttu-id="06af5-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="06af5-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="06af5-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="06af5-136">NOTES</span></span>

## <span data-ttu-id="06af5-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06af5-137">RELATED LINKS</span></span>
