---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: e0577342a839424d9a45a91b6c9289a72fe9df12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257031"
---
# <span data-ttu-id="0b32c-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="0b32c-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="0b32c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b32c-102">SYNOPSIS</span></span>
<span data-ttu-id="0b32c-103">Obtém aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="0b32c-103">Gets managed applications</span></span>

## <span data-ttu-id="0b32c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b32c-104">SYNTAX</span></span>

### <span data-ttu-id="0b32c-105">GetBySubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="0b32c-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b32c-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0b32c-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b32c-107">GetById</span><span class="sxs-lookup"><span data-stu-id="0b32c-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b32c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b32c-108">DESCRIPTION</span></span>
<span data-ttu-id="0b32c-109">O cmdlet **Get-AzManagedApplication** Obtém aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="0b32c-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="0b32c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b32c-110">EXAMPLES</span></span>

### <span data-ttu-id="0b32c-111">Exemplo 1: obter todos os aplicativos gerenciados em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0b32c-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="0b32c-112">Este comando obtém aplicativos gerenciados no grupo de recursos "MyRG"</span><span class="sxs-lookup"><span data-stu-id="0b32c-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="0b32c-113">Exemplo 2: obter todos os aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="0b32c-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="0b32c-114">Este comando obtém todos os aplicativos gerenciados sob a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="0b32c-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="0b32c-115">OS</span><span class="sxs-lookup"><span data-stu-id="0b32c-115">PARAMETERS</span></span>

### <span data-ttu-id="0b32c-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0b32c-116">-ApiVersion</span></span>
<span data-ttu-id="0b32c-117">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="0b32c-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0b32c-118">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="0b32c-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="0b32c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b32c-119">-DefaultProfile</span></span>
<span data-ttu-id="0b32c-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b32c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b32c-121">-ID</span><span class="sxs-lookup"><span data-stu-id="0b32c-121">-Id</span></span>
<span data-ttu-id="0b32c-122">A ID de aplicativo gerenciada totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="0b32c-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="0b32c-123">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="0b32c-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="0b32c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b32c-124">-Name</span></span>
<span data-ttu-id="0b32c-125">O nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="0b32c-125">The managed application name.</span></span>

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

### <span data-ttu-id="0b32c-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="0b32c-126">-Pre</span></span>
<span data-ttu-id="0b32c-127">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="0b32c-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0b32c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b32c-128">-ResourceGroupName</span></span>
<span data-ttu-id="0b32c-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b32c-129">The resource group name.</span></span>

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

### <span data-ttu-id="0b32c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b32c-130">CommonParameters</span></span>
<span data-ttu-id="0b32c-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b32c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b32c-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b32c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b32c-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b32c-133">INPUTS</span></span>

### <span data-ttu-id="0b32c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0b32c-134">System.String</span></span>

## <span data-ttu-id="0b32c-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b32c-135">OUTPUTS</span></span>

### <span data-ttu-id="0b32c-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0b32c-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0b32c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b32c-137">NOTES</span></span>

## <span data-ttu-id="0b32c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b32c-138">RELATED LINKS</span></span>
