---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 5fba45e50076952a0a2e11e2e5541ab9546d3bc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432586"
---
# <span data-ttu-id="93e85-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="93e85-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="93e85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93e85-102">SYNOPSIS</span></span>
<span data-ttu-id="93e85-103">Obtém definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="93e85-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93e85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93e85-104">SYNTAX</span></span>

### <span data-ttu-id="93e85-105">O conjunto de parâmetros da lista todas as definições definidas pela política.</span><span class="sxs-lookup"><span data-stu-id="93e85-105">The list all policy set definitions parameter set.</span></span> <span data-ttu-id="93e85-106">Assume</span><span class="sxs-lookup"><span data-stu-id="93e85-106">(Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93e85-107">O conjunto de parâmetros de nome de definição de política.</span><span class="sxs-lookup"><span data-stu-id="93e85-107">The policy set definition name parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93e85-108">O conjunto de parâmetros de ID de definição de política.</span><span class="sxs-lookup"><span data-stu-id="93e85-108">The policy set definition Id parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93e85-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93e85-109">DESCRIPTION</span></span>
<span data-ttu-id="93e85-110">O cmdlet **Get-AzureRmPolicySetDefinition** obtém todas as definições do conjunto de políticas ou uma definição de conjunto de políticas específica identificada por nome ou ID.</span><span class="sxs-lookup"><span data-stu-id="93e85-110">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="93e85-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93e85-111">EXAMPLES</span></span>

### <span data-ttu-id="93e85-112">Exemplo 1: obter toda a definição do conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="93e85-112">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="93e85-113">Esse comando obtém todas as definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="93e85-113">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="93e85-114">Exemplo 2: obter definição de política definida por nome</span><span class="sxs-lookup"><span data-stu-id="93e85-114">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="93e85-115">Esse comando obtém a definição do conjunto de políticas chamado VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="93e85-115">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="93e85-116">OS</span><span class="sxs-lookup"><span data-stu-id="93e85-116">PARAMETERS</span></span>

### <span data-ttu-id="93e85-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="93e85-117">-ApiVersion</span></span>
<span data-ttu-id="93e85-118">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="93e85-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="93e85-119">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="93e85-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="93e85-120">-ID</span><span class="sxs-lookup"><span data-stu-id="93e85-120">-Id</span></span>
<span data-ttu-id="93e85-121">A ID da definição do conjunto de políticas totalmente qualificadas, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="93e85-121">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="93e85-122">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="93e85-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93e85-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="93e85-123">-Name</span></span>
<span data-ttu-id="93e85-124">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="93e85-124">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93e85-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="93e85-125">-Pre</span></span>
<span data-ttu-id="93e85-126">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="93e85-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="93e85-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e85-127">-DefaultProfile</span></span>
<span data-ttu-id="93e85-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93e85-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93e85-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e85-129">CommonParameters</span></span>
<span data-ttu-id="93e85-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93e85-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e85-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93e85-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e85-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93e85-132">INPUTS</span></span>

### <span data-ttu-id="93e85-133">System. String</span><span class="sxs-lookup"><span data-stu-id="93e85-133">System.String</span></span>

## <span data-ttu-id="93e85-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93e85-134">OUTPUTS</span></span>

### <span data-ttu-id="93e85-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="93e85-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="93e85-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93e85-136">NOTES</span></span>

## <span data-ttu-id="93e85-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93e85-137">RELATED LINKS</span></span>

