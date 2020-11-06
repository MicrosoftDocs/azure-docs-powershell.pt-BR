---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
ms.openlocfilehash: 953a810585550ec8895fc9306f78633beb4846a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427799"
---
# <span data-ttu-id="37ef5-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="37ef5-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="37ef5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37ef5-102">SYNOPSIS</span></span>
<span data-ttu-id="37ef5-103">Obtém aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="37ef5-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37ef5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37ef5-104">SYNTAX</span></span>

### <span data-ttu-id="37ef5-105">O conjunto de parâmetros da lista todos os aplicativos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="37ef5-105">The list all managed applications parameter set.</span></span> <span data-ttu-id="37ef5-106">Assume</span><span class="sxs-lookup"><span data-stu-id="37ef5-106">(Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37ef5-107">O conjunto de parâmetros de nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="37ef5-107">The managed application name parameter set.</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37ef5-108">O conjunto de parâmetros de ID do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="37ef5-108">The managed application Id parameter set.</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37ef5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="37ef5-109">DESCRIPTION</span></span>
<span data-ttu-id="37ef5-110">O cmdlet **Get-AzureRmManagedApplication** Obtém aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="37ef5-110">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="37ef5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37ef5-111">EXAMPLES</span></span>

### <span data-ttu-id="37ef5-112">Exemplo 1: obter todos os aplicativos gerenciados em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="37ef5-112">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="37ef5-113">Este comando obtém aplicativos gerenciados no grupo de recursos "MyRG"</span><span class="sxs-lookup"><span data-stu-id="37ef5-113">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="37ef5-114">Exemplo 2: obter todos os aplicativos gerenciados</span><span class="sxs-lookup"><span data-stu-id="37ef5-114">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="37ef5-115">Este comando obtém todos os aplicativos gerenciados sob a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="37ef5-115">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="37ef5-116">OS</span><span class="sxs-lookup"><span data-stu-id="37ef5-116">PARAMETERS</span></span>

### <span data-ttu-id="37ef5-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="37ef5-117">-ApiVersion</span></span>
<span data-ttu-id="37ef5-118">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="37ef5-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="37ef5-119">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="37ef5-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="37ef5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ef5-120">-DefaultProfile</span></span>
<span data-ttu-id="37ef5-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37ef5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37ef5-122">-ID</span><span class="sxs-lookup"><span data-stu-id="37ef5-122">-Id</span></span>
<span data-ttu-id="37ef5-123">A ID de aplicativo gerenciada totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="37ef5-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="37ef5-124">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="37ef5-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ef5-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="37ef5-125">-Name</span></span>
<span data-ttu-id="37ef5-126">O nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="37ef5-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ef5-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="37ef5-127">-Pre</span></span>
<span data-ttu-id="37ef5-128">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="37ef5-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="37ef5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37ef5-129">-ResourceGroupName</span></span>
<span data-ttu-id="37ef5-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="37ef5-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ef5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ef5-131">CommonParameters</span></span>
<span data-ttu-id="37ef5-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37ef5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ef5-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37ef5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ef5-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="37ef5-134">INPUTS</span></span>

### <span data-ttu-id="37ef5-135">System. String</span><span class="sxs-lookup"><span data-stu-id="37ef5-135">System.String</span></span>

## <span data-ttu-id="37ef5-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="37ef5-136">OUTPUTS</span></span>

### <span data-ttu-id="37ef5-137">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="37ef5-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="37ef5-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="37ef5-138">NOTES</span></span>

## <span data-ttu-id="37ef5-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37ef5-139">RELATED LINKS</span></span>

