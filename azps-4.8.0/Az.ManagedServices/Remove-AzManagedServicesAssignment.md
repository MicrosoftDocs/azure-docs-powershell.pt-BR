---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
ms.openlocfilehash: 5f2328ba75a0142a61238665eef41e32bf1fbba6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113524"
---
# <span data-ttu-id="c59a2-101">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="c59a2-101">Remove-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="c59a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c59a2-102">SYNOPSIS</span></span>
<span data-ttu-id="c59a2-103">Exclui uma atribuição de registro.</span><span class="sxs-lookup"><span data-stu-id="c59a2-103">Deletes a registration assignment.</span></span>

## <span data-ttu-id="c59a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c59a2-104">SYNTAX</span></span>

### <span data-ttu-id="c59a2-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="c59a2-105">Default (Default)</span></span>
```
Remove-AzManagedServicesAssignment [[-Scope] <String>] -Id <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c59a2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c59a2-106">ByResourceId</span></span>
```
Remove-AzManagedServicesAssignment -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c59a2-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c59a2-107">ByInputObject</span></span>
```
Remove-AzManagedServicesAssignment -InputObject <PSRegistrationAssignment> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c59a2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c59a2-108">DESCRIPTION</span></span>
<span data-ttu-id="c59a2-109">Exclui uma atribuição de registro.</span><span class="sxs-lookup"><span data-stu-id="c59a2-109">Deletes a registration assignment.</span></span>

## <span data-ttu-id="c59a2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c59a2-110">EXAMPLES</span></span>

### <span data-ttu-id="c59a2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c59a2-111">Example 1</span></span>
```powershell
PS C:\Remove-AzManagedServicesAssignment -Id b037e73c-815e-4472-868f-59e51b49b949

Name                                 RegistrationDefinitionId
----                                 ------------------------
b037e73c-815e-4472-868f-59e51b49b949 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/be2f72e6-93e0-4d3f-ac50-9a756ed4ffa7
```

<span data-ttu-id="c59a2-112">Exclui a atribuição de registro sob o escopo padrão.</span><span class="sxs-lookup"><span data-stu-id="c59a2-112">Deletes the registration assignment under the default scope.</span></span>

### <span data-ttu-id="c59a2-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c59a2-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzManagedServicesAssignment -ResourceId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationAssignments/88ba878b-9a3c-40c3-80da-015cbe488a2f

Name                                 RegistrationDefinitionId
----                                 ------------------------
88ba878b-9a3c-40c3-80da-015cbe488a2f /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/40be0299-6573-4391-be2f-b41dd4aaf4f9
```

<span data-ttu-id="c59a2-114">Exclui a atribuição de registro de acordo com a ID de recurso totalmente qualificada.</span><span class="sxs-lookup"><span data-stu-id="c59a2-114">Deletes the registration assignment given the fully qualified resource id.</span></span>

### <span data-ttu-id="c59a2-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c59a2-115">Example 3</span></span>
```powershell
PS C:\> $assignment = New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/33974646-9bce-461d-89eb-331f20fca33c
PS C:\> Remove-AzManagedServicesAssignment -InputObject $assignment
```

<span data-ttu-id="c59a2-116">Exclui a atribuição de registro usando o objeto de entrada fornecido.</span><span class="sxs-lookup"><span data-stu-id="c59a2-116">Deletes the registration assignment using the input object provided.</span></span>

## <span data-ttu-id="c59a2-117">OS</span><span class="sxs-lookup"><span data-stu-id="c59a2-117">PARAMETERS</span></span>

### <span data-ttu-id="c59a2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c59a2-118">-AsJob</span></span>
<span data-ttu-id="c59a2-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c59a2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c59a2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c59a2-120">-DefaultProfile</span></span>
<span data-ttu-id="c59a2-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c59a2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c59a2-122">-ID</span><span class="sxs-lookup"><span data-stu-id="c59a2-122">-Id</span></span>
<span data-ttu-id="c59a2-123">O GUID de atribuição de registro (por exemplo, b0c052e5-c437-4771-a476-8b1201158a57)</span><span class="sxs-lookup"><span data-stu-id="c59a2-123">The registration assignment GUID (for example, b0c052e5-c437-4771-a476-8b1201158a57)</span></span>
```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59a2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c59a2-124">-InputObject</span></span>
<span data-ttu-id="c59a2-125">O objeto de atribuição de registro.</span><span class="sxs-lookup"><span data-stu-id="c59a2-125">The registration assignment object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c59a2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c59a2-126">-ResourceId</span></span>
<span data-ttu-id="c59a2-127">A ID de recurso totalmente qualificado da atribuição de registro (por exemplo,/subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57).</span><span class="sxs-lookup"><span data-stu-id="c59a2-127">The fully qualified resource id of the registration assignment (for example, /subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57).</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c59a2-128">-Escopo</span><span class="sxs-lookup"><span data-stu-id="c59a2-128">-Scope</span></span>
<span data-ttu-id="c59a2-129">O escopo onde a atribuição de registro deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="c59a2-129">The scope where the registration assignment should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59a2-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c59a2-130">-Confirm</span></span>
<span data-ttu-id="c59a2-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c59a2-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59a2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c59a2-132">-WhatIf</span></span>
<span data-ttu-id="c59a2-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c59a2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c59a2-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c59a2-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c59a2-135">CommonParameters</span></span>
<span data-ttu-id="c59a2-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c59a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c59a2-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c59a2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c59a2-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c59a2-138">INPUTS</span></span>

### <span data-ttu-id="c59a2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c59a2-139">System.String</span></span>

### <span data-ttu-id="c59a2-140">Microsoft. Azure. PowerShell. cmdlets. Managedservices. Models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="c59a2-140">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>

## <span data-ttu-id="c59a2-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c59a2-141">OUTPUTS</span></span>

### <span data-ttu-id="c59a2-142">Microsoft. Azure. PowerShell. cmdlets. Managedservices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="c59a2-142">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="c59a2-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c59a2-143">NOTES</span></span>

## <span data-ttu-id="c59a2-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c59a2-144">RELATED LINKS</span></span>
