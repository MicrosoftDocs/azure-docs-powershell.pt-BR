---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/powershell/module/az.managedservices/new-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
ms.openlocfilehash: 90ba4f3080f73207430c0751fcc4f90897507819
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886618"
---
# <span data-ttu-id="084b5-101">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="084b5-101">New-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="084b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="084b5-102">SYNOPSIS</span></span>
<span data-ttu-id="084b5-103">Cria ou atualiza uma atribuição de registro.</span><span class="sxs-lookup"><span data-stu-id="084b5-103">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="084b5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="084b5-104">SYNTAX</span></span>

### <span data-ttu-id="084b5-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="084b5-105">Default (Default)</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>] -RegistrationDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="084b5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="084b5-106">ByInputObject</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>]
 -RegistrationDefinition <PSRegistrationDefinition> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="084b5-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="084b5-107">DESCRIPTION</span></span>
<span data-ttu-id="084b5-108">Cria ou atualiza uma atribuição de registro.</span><span class="sxs-lookup"><span data-stu-id="084b5-108">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="084b5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="084b5-109">EXAMPLES</span></span>

### <span data-ttu-id="084b5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="084b5-110">Example 1</span></span>
```
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded

PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\>
```

<span data-ttu-id="084b5-111">Cria uma atribuição de registro no escopo padrão usando o identificador de definição de registro.</span><span class="sxs-lookup"><span data-stu-id="084b5-111">Creates a registration assignment at the default scope using the registration definition identifier.</span></span>

### <span data-ttu-id="084b5-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="084b5-112">Example 2</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinition $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b279ec53-b42f-4952-bd62-cd49982e9572 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/b279ec53-b42f-4952-bd62-cd49982e9572 Succeeded


PS C:\>
```

<span data-ttu-id="084b5-113">Cria uma atribuição de registro com um objeto de definição de registro como entrada.</span><span class="sxs-lookup"><span data-stu-id="084b5-113">Creates a registration assignment with a registration definition object as input.</span></span>

### <span data-ttu-id="084b5-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="084b5-114">Example 3</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded

PS C:\>
```

<span data-ttu-id="084b5-115">Atualiza uma atribuição de registro com um identificador e nome de definição de registro.</span><span class="sxs-lookup"><span data-stu-id="084b5-115">Updates a registration assignment with a registration definition identifier and name.</span></span>


## <span data-ttu-id="084b5-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="084b5-116">PARAMETERS</span></span>

### <span data-ttu-id="084b5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="084b5-117">-DefaultProfile</span></span>
<span data-ttu-id="084b5-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="084b5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="084b5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="084b5-119">-Name</span></span>
<span data-ttu-id="084b5-120">O nome exclusivo da atribuição de registro.</span><span class="sxs-lookup"><span data-stu-id="084b5-120">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="084b5-121">-RegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="084b5-121">-RegistrationDefinition</span></span>
<span data-ttu-id="084b5-122">O objeto de entrada de definição de registro.</span><span class="sxs-lookup"><span data-stu-id="084b5-122">The registration definition input object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="084b5-123">-RegistrationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="084b5-123">-RegistrationDefinitionId</span></span>
<span data-ttu-id="084b5-124">A ID de recurso totalmente qualificada da definição de registro.</span><span class="sxs-lookup"><span data-stu-id="084b5-124">The fully qualified resource id of the registration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="084b5-125">-Scope</span><span class="sxs-lookup"><span data-stu-id="084b5-125">-Scope</span></span>
<span data-ttu-id="084b5-126">O escopo em que a atribuição de registro deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="084b5-126">The scope where the registration assignment should be created.</span></span>

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

### <span data-ttu-id="084b5-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="084b5-127">-AsJob</span></span>
<span data-ttu-id="084b5-128">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="084b5-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="084b5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="084b5-129">-Confirm</span></span>
<span data-ttu-id="084b5-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="084b5-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084b5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="084b5-131">-WhatIf</span></span>
<span data-ttu-id="084b5-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="084b5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="084b5-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="084b5-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084b5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="084b5-134">CommonParameters</span></span>
<span data-ttu-id="084b5-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="084b5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="084b5-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="084b5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="084b5-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="084b5-137">INPUTS</span></span>

### <span data-ttu-id="084b5-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="084b5-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
### <span data-ttu-id="084b5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="084b5-139">System.String</span></span>
## <span data-ttu-id="084b5-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="084b5-140">OUTPUTS</span></span>

### <span data-ttu-id="084b5-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="084b5-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="084b5-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="084b5-142">NOTES</span></span>

## <span data-ttu-id="084b5-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="084b5-143">RELATED LINKS</span></span>
