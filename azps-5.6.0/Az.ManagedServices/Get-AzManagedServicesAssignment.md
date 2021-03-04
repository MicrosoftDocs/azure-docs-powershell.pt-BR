---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 5f0398981f6c3a59c9401df4ec89208a5f8196b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887109"
---
# <span data-ttu-id="497b9-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="497b9-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="497b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="497b9-102">SYNOPSIS</span></span>
<span data-ttu-id="497b9-103">Obtém uma atribuição de registro específica ou uma lista das atribuições de registro.</span><span class="sxs-lookup"><span data-stu-id="497b9-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="497b9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="497b9-104">SYNTAX</span></span>

### <span data-ttu-id="497b9-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="497b9-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="497b9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="497b9-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="497b9-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="497b9-107">DESCRIPTION</span></span>
<span data-ttu-id="497b9-108">Obtém uma atribuição de registro específica ou uma lista das atribuições de registro.</span><span class="sxs-lookup"><span data-stu-id="497b9-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="497b9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="497b9-109">EXAMPLES</span></span>

### <span data-ttu-id="497b9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="497b9-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="497b9-111">Obtém todas as atribuições de registro no escopo padrão.</span><span class="sxs-lookup"><span data-stu-id="497b9-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="497b9-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="497b9-112">Example 2</span></span>
```
PS C:\> $assignments = Get-AzManagedServicesAssignment -ExpandRegistrationDefinition
PS C:\> $assignments[0].Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="497b9-113">Obtém todas as atribuições de registro com os detalhes de definição de registro.</span><span class="sxs-lookup"><span data-stu-id="497b9-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="497b9-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="497b9-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="497b9-115">Obtém uma atribuição de registro por nome sem detalhes de definição de registro.</span><span class="sxs-lookup"><span data-stu-id="497b9-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="497b9-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="497b9-116">Example 4</span></span>
```
PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80 -ExpandRegistrationDefinition
PS C:\> $assignment.Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="497b9-117">Obtém uma atribuição de registro por nome com detalhes de definição de registro.</span><span class="sxs-lookup"><span data-stu-id="497b9-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="497b9-118">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="497b9-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="497b9-119">Obtém todas as atribuições de registro em determinado escopo.</span><span class="sxs-lookup"><span data-stu-id="497b9-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="497b9-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="497b9-120">PARAMETERS</span></span>

### <span data-ttu-id="497b9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="497b9-121">-DefaultProfile</span></span>
<span data-ttu-id="497b9-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="497b9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="497b9-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="497b9-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="497b9-124">Se deve incluir detalhes de definição de registro.</span><span class="sxs-lookup"><span data-stu-id="497b9-124">Whether to include registration definition details.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497b9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="497b9-125">-Name</span></span>
<span data-ttu-id="497b9-126">O nome exclusivo da atribuição de registro.</span><span class="sxs-lookup"><span data-stu-id="497b9-126">The unique name of the Registration Assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497b9-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="497b9-127">-Scope</span></span>
<span data-ttu-id="497b9-128">O escopo em que a atribuição de registro foi criada.</span><span class="sxs-lookup"><span data-stu-id="497b9-128">The scope where the registration assignment created.</span></span>

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

### <span data-ttu-id="497b9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="497b9-129">CommonParameters</span></span>
<span data-ttu-id="497b9-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="497b9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="497b9-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="497b9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="497b9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="497b9-132">INPUTS</span></span>

### <span data-ttu-id="497b9-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="497b9-133">None</span></span>
## <span data-ttu-id="497b9-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="497b9-134">OUTPUTS</span></span>

### <span data-ttu-id="497b9-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="497b9-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="497b9-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="497b9-136">NOTES</span></span>

## <span data-ttu-id="497b9-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="497b9-137">RELATED LINKS</span></span>
