---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: c95fe4a977c70964cf8b4dab86985d79315d3141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892733"
---
# <span data-ttu-id="c4cbc-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="c4cbc-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="c4cbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="c4cbc-103">Obtém aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="c4cbc-103">Gets managed applications</span></span>

## <span data-ttu-id="c4cbc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c4cbc-104">SYNTAX</span></span>

### <span data-ttu-id="c4cbc-105">GetBySubscription (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c4cbc-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4cbc-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c4cbc-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4cbc-107">GetById</span><span class="sxs-lookup"><span data-stu-id="c4cbc-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4cbc-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c4cbc-108">DESCRIPTION</span></span>
<span data-ttu-id="c4cbc-109">O cmdlet **Get-AzManagedApplication** obtém aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="c4cbc-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="c4cbc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4cbc-110">EXAMPLES</span></span>

### <span data-ttu-id="c4cbc-111">Exemplo 1: Obter todos os aplicativos gerenciados em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c4cbc-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="c4cbc-112">Este comando obtém aplicativos gerenciados no grupo de recursos "MyRG"</span><span class="sxs-lookup"><span data-stu-id="c4cbc-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="c4cbc-113">Exemplo 2: Obter todos os aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="c4cbc-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="c4cbc-114">Este comando obterá todos os aplicativos gerenciados na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="c4cbc-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="c4cbc-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c4cbc-115">PARAMETERS</span></span>

### <span data-ttu-id="c4cbc-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c4cbc-116">-ApiVersion</span></span>
<span data-ttu-id="c4cbc-117">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="c4cbc-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c4cbc-118">Se não for especificada, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="c4cbc-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c4cbc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4cbc-119">-DefaultProfile</span></span>
<span data-ttu-id="c4cbc-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c4cbc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4cbc-121">-Id</span><span class="sxs-lookup"><span data-stu-id="c4cbc-121">-Id</span></span>
<span data-ttu-id="c4cbc-122">A ID do aplicativo gerenciado totalmente qualificado, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="c4cbc-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="c4cbc-123">por exemplo, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="c4cbc-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4cbc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c4cbc-124">-Name</span></span>
<span data-ttu-id="c4cbc-125">O nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c4cbc-125">The managed application name.</span></span>

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

### <span data-ttu-id="c4cbc-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="c4cbc-126">-Pre</span></span>
<span data-ttu-id="c4cbc-127">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="c4cbc-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c4cbc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4cbc-128">-ResourceGroupName</span></span>
<span data-ttu-id="c4cbc-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c4cbc-129">The resource group name.</span></span>

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

### <span data-ttu-id="c4cbc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4cbc-130">CommonParameters</span></span>
<span data-ttu-id="c4cbc-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4cbc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4cbc-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4cbc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4cbc-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4cbc-133">INPUTS</span></span>

### <span data-ttu-id="c4cbc-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c4cbc-134">System.String</span></span>

## <span data-ttu-id="c4cbc-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c4cbc-135">OUTPUTS</span></span>

### <span data-ttu-id="c4cbc-136">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c4cbc-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c4cbc-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="c4cbc-137">NOTES</span></span>

## <span data-ttu-id="c4cbc-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4cbc-138">RELATED LINKS</span></span>
