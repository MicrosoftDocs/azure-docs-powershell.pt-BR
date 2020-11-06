---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: 9c670973c9fcff3cd9038809cb955efc32edeee0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599444"
---
# <span data-ttu-id="9cd63-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="9cd63-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="9cd63-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9cd63-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd63-103">Obtém aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="9cd63-103">Gets managed applications</span></span>

## <span data-ttu-id="9cd63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9cd63-104">SYNTAX</span></span>

### <span data-ttu-id="9cd63-105">GetBySubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="9cd63-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9cd63-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9cd63-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cd63-107">GetById</span><span class="sxs-lookup"><span data-stu-id="9cd63-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cd63-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9cd63-108">DESCRIPTION</span></span>
<span data-ttu-id="9cd63-109">O cmdlet **Get-AzManagedApplication** Obtém aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="9cd63-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="9cd63-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9cd63-110">EXAMPLES</span></span>

### <span data-ttu-id="9cd63-111">Exemplo 1: obter todos os aplicativos gerenciados em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9cd63-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="9cd63-112">Este comando obtém aplicativos gerenciados no grupo de recursos "MyRG"</span><span class="sxs-lookup"><span data-stu-id="9cd63-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="9cd63-113">Exemplo 2: obter todos os aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="9cd63-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="9cd63-114">Este comando obtém todos os aplicativos gerenciados sob a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="9cd63-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="9cd63-115">OS</span><span class="sxs-lookup"><span data-stu-id="9cd63-115">PARAMETERS</span></span>

### <span data-ttu-id="9cd63-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9cd63-116">-ApiVersion</span></span>
<span data-ttu-id="9cd63-117">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="9cd63-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9cd63-118">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="9cd63-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="9cd63-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd63-119">-DefaultProfile</span></span>
<span data-ttu-id="9cd63-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9cd63-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cd63-121">-ID</span><span class="sxs-lookup"><span data-stu-id="9cd63-121">-Id</span></span>
<span data-ttu-id="9cd63-122">A ID de aplicativo gerenciada totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="9cd63-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="9cd63-123">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="9cd63-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="9cd63-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9cd63-124">-Name</span></span>
<span data-ttu-id="9cd63-125">O nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9cd63-125">The managed application name.</span></span>

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

### <span data-ttu-id="9cd63-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="9cd63-126">-Pre</span></span>
<span data-ttu-id="9cd63-127">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="9cd63-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9cd63-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cd63-128">-ResourceGroupName</span></span>
<span data-ttu-id="9cd63-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9cd63-129">The resource group name.</span></span>

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

### <span data-ttu-id="9cd63-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd63-130">CommonParameters</span></span>
<span data-ttu-id="9cd63-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cd63-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd63-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cd63-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd63-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9cd63-133">INPUTS</span></span>

### <span data-ttu-id="9cd63-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9cd63-134">System.String</span></span>

## <span data-ttu-id="9cd63-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9cd63-135">OUTPUTS</span></span>

### <span data-ttu-id="9cd63-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9cd63-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9cd63-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9cd63-137">NOTES</span></span>

## <span data-ttu-id="9cd63-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9cd63-138">RELATED LINKS</span></span>
