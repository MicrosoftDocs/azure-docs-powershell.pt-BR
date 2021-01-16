---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 8aae61e163baf95cbed62ea239c7d1a6190aed1f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428291"
---
# <span data-ttu-id="84c4a-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="84c4a-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="84c4a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="84c4a-103">Obtém uma atribuição de Registro específica ou uma lista de atribuições de registro.</span><span class="sxs-lookup"><span data-stu-id="84c4a-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="84c4a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84c4a-104">SYNTAX</span></span>

### <span data-ttu-id="84c4a-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="84c4a-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84c4a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="84c4a-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84c4a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84c4a-107">DESCRIPTION</span></span>
<span data-ttu-id="84c4a-108">Obtém uma atribuição de Registro específica ou uma lista de atribuições de registro.</span><span class="sxs-lookup"><span data-stu-id="84c4a-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="84c4a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84c4a-109">EXAMPLES</span></span>

### <span data-ttu-id="84c4a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="84c4a-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="84c4a-111">Obtém todas as atribuições de registro sob o escopo padrão.</span><span class="sxs-lookup"><span data-stu-id="84c4a-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="84c4a-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="84c4a-112">Example 2</span></span>
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

<span data-ttu-id="84c4a-113">Obtém todas as tarefas de registro com os detalhes da definição de registro.</span><span class="sxs-lookup"><span data-stu-id="84c4a-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="84c4a-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="84c4a-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="84c4a-115">Obtém uma atribuição de registro por nome sem detalhes de definição de registro.</span><span class="sxs-lookup"><span data-stu-id="84c4a-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="84c4a-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="84c4a-116">Example 4</span></span>
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

<span data-ttu-id="84c4a-117">Obtém uma atribuição de registro por nome com detalhes de definição de registro.</span><span class="sxs-lookup"><span data-stu-id="84c4a-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="84c4a-118">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="84c4a-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="84c4a-119">Obtém todas as atribuições de registro em um determinado escopo.</span><span class="sxs-lookup"><span data-stu-id="84c4a-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="84c4a-120">OS</span><span class="sxs-lookup"><span data-stu-id="84c4a-120">PARAMETERS</span></span>

### <span data-ttu-id="84c4a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84c4a-121">-DefaultProfile</span></span>
<span data-ttu-id="84c4a-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="84c4a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84c4a-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="84c4a-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="84c4a-124">Se você deseja incluir detalhes da definição de registro.</span><span class="sxs-lookup"><span data-stu-id="84c4a-124">Whether to include registration definition details.</span></span>

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

### <span data-ttu-id="84c4a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="84c4a-125">-Name</span></span>
<span data-ttu-id="84c4a-126">O nome exclusivo da atribuição de registro.</span><span class="sxs-lookup"><span data-stu-id="84c4a-126">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="84c4a-127">-Escopo</span><span class="sxs-lookup"><span data-stu-id="84c4a-127">-Scope</span></span>
<span data-ttu-id="84c4a-128">O escopo onde a atribuição de registro foi criada.</span><span class="sxs-lookup"><span data-stu-id="84c4a-128">The scope where the registration assignment created.</span></span>

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

### <span data-ttu-id="84c4a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c4a-129">CommonParameters</span></span>
<span data-ttu-id="84c4a-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84c4a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c4a-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84c4a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c4a-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84c4a-132">INPUTS</span></span>

### <span data-ttu-id="84c4a-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="84c4a-133">None</span></span>
## <span data-ttu-id="84c4a-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84c4a-134">OUTPUTS</span></span>

### <span data-ttu-id="84c4a-135">Microsoft. Azure. PowerShell. cmdlets. Managedservices. Models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="84c4a-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="84c4a-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84c4a-136">NOTES</span></span>

## <span data-ttu-id="84c4a-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84c4a-137">RELATED LINKS</span></span>
