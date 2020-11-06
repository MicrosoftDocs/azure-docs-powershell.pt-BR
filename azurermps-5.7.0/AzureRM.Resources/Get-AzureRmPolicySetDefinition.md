---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 694f2ef459b50648e934e4ea0e434fe218d4b1f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432906"
---
# <span data-ttu-id="b9c4d-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b9c4d-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="b9c4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c4d-103">Obtém definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="b9c4d-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9c4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9c4d-104">SYNTAX</span></span>

### <span data-ttu-id="b9c4d-105">GetBySubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="b9c4d-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9c4d-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b9c4d-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9c4d-107">GetById</span><span class="sxs-lookup"><span data-stu-id="b9c4d-107">GetById</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9c4d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9c4d-108">DESCRIPTION</span></span>
<span data-ttu-id="b9c4d-109">O cmdlet **Get-AzureRmPolicySetDefinition** obtém todas as definições do conjunto de políticas ou uma definição de conjunto de políticas específica identificada por nome ou ID.</span><span class="sxs-lookup"><span data-stu-id="b9c4d-109">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="b9c4d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9c4d-110">EXAMPLES</span></span>

### <span data-ttu-id="b9c4d-111">Exemplo 1: obter toda a definição do conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="b9c4d-111">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="b9c4d-112">Esse comando obtém todas as definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="b9c4d-112">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="b9c4d-113">Exemplo 2: obter definição de política definida por nome</span><span class="sxs-lookup"><span data-stu-id="b9c4d-113">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="b9c4d-114">Esse comando obtém a definição do conjunto de políticas chamado VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="b9c4d-114">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="b9c4d-115">OS</span><span class="sxs-lookup"><span data-stu-id="b9c4d-115">PARAMETERS</span></span>

### <span data-ttu-id="b9c4d-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b9c4d-116">-ApiVersion</span></span>
<span data-ttu-id="b9c4d-117">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="b9c4d-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b9c4d-118">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="b9c4d-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c4d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c4d-119">-DefaultProfile</span></span>
<span data-ttu-id="b9c4d-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b9c4d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9c4d-121">-ID</span><span class="sxs-lookup"><span data-stu-id="b9c4d-121">-Id</span></span>
<span data-ttu-id="b9c4d-122">A ID da definição do conjunto de políticas totalmente qualificadas, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="b9c4d-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="b9c4d-123">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b9c4d-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c4d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9c4d-124">-Name</span></span>
<span data-ttu-id="b9c4d-125">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="b9c4d-125">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c4d-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="b9c4d-126">-Pre</span></span>
<span data-ttu-id="b9c4d-127">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="b9c4d-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b9c4d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c4d-128">CommonParameters</span></span>
<span data-ttu-id="b9c4d-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9c4d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c4d-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c4d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c4d-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9c4d-131">INPUTS</span></span>

### <span data-ttu-id="b9c4d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c4d-132">System.String</span></span>

## <span data-ttu-id="b9c4d-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9c4d-133">OUTPUTS</span></span>

### <span data-ttu-id="b9c4d-134">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b9c4d-134">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b9c4d-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9c4d-135">NOTES</span></span>

## <span data-ttu-id="b9c4d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9c4d-136">RELATED LINKS</span></span>
