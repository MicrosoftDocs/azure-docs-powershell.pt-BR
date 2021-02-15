---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: e0577342a839424d9a45a91b6c9289a72fe9df12
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111423"
---
# <span data-ttu-id="6d692-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="6d692-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="6d692-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d692-102">SYNOPSIS</span></span>
<span data-ttu-id="6d692-103">Obtém aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="6d692-103">Gets managed applications</span></span>

## <span data-ttu-id="6d692-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d692-104">SYNTAX</span></span>

### <span data-ttu-id="6d692-105">GetBySubscription (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6d692-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d692-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6d692-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d692-107">GetById</span><span class="sxs-lookup"><span data-stu-id="6d692-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d692-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d692-108">DESCRIPTION</span></span>
<span data-ttu-id="6d692-109">O **cmdlet Get-AzManagedApplication** obtém aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="6d692-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="6d692-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6d692-110">EXAMPLES</span></span>

### <span data-ttu-id="6d692-111">Exemplo 1: Obter todos os aplicativos gerenciados em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6d692-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="6d692-112">Esse comando obtém aplicativos gerenciados no grupo de recursos "MyRG"</span><span class="sxs-lookup"><span data-stu-id="6d692-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="6d692-113">Exemplo 2: Obter todos os aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="6d692-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="6d692-114">Este comando obterá todos os aplicativos gerenciados sob a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="6d692-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="6d692-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d692-115">PARAMETERS</span></span>

### <span data-ttu-id="6d692-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6d692-116">-ApiVersion</span></span>
<span data-ttu-id="6d692-117">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="6d692-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6d692-118">Se não especificado, a versão da API será determinada automaticamente como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="6d692-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="6d692-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d692-119">-DefaultProfile</span></span>
<span data-ttu-id="6d692-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6d692-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d692-121">-ID</span><span class="sxs-lookup"><span data-stu-id="6d692-121">-Id</span></span>
<span data-ttu-id="6d692-122">A ID de aplicativo gerenciado totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="6d692-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="6d692-123">por exemplo, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="6d692-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="6d692-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d692-124">-Name</span></span>
<span data-ttu-id="6d692-125">O nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="6d692-125">The managed application name.</span></span>

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

### <span data-ttu-id="6d692-126">-Pré-</span><span class="sxs-lookup"><span data-stu-id="6d692-126">-Pre</span></span>
<span data-ttu-id="6d692-127">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="6d692-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6d692-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d692-128">-ResourceGroupName</span></span>
<span data-ttu-id="6d692-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6d692-129">The resource group name.</span></span>

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

### <span data-ttu-id="6d692-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d692-130">CommonParameters</span></span>
<span data-ttu-id="6d692-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d692-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d692-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d692-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d692-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="6d692-133">INPUTS</span></span>

### <span data-ttu-id="6d692-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6d692-134">System.String</span></span>

## <span data-ttu-id="6d692-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="6d692-135">OUTPUTS</span></span>

### <span data-ttu-id="6d692-136">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="6d692-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6d692-137">Notas</span><span class="sxs-lookup"><span data-stu-id="6d692-137">NOTES</span></span>

## <span data-ttu-id="6d692-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d692-138">RELATED LINKS</span></span>
