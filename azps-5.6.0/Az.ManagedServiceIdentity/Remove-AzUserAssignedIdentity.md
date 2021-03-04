---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 83280df19363285ab23ca1e27441a491a783b03a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886750"
---
# <span data-ttu-id="6efe5-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6efe5-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="6efe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6efe5-102">SYNOPSIS</span></span>
<span data-ttu-id="6efe5-103">Remove uma identidade atribuída pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="6efe5-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="6efe5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6efe5-104">SYNTAX</span></span>

### <span data-ttu-id="6efe5-105">ResourceGroupAndNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6efe5-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6efe5-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6efe5-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6efe5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6efe5-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6efe5-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6efe5-108">DESCRIPTION</span></span>
<span data-ttu-id="6efe5-109">O **Remove-AzUserAssignedIdentity** exclui a Identidade Atribuída pelo Usuário especificada.</span><span class="sxs-lookup"><span data-stu-id="6efe5-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="6efe5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6efe5-110">EXAMPLES</span></span>

### <span data-ttu-id="6efe5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6efe5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="6efe5-112">Este cmdlet de exemplo exclui a **ID1** de identidade no grupo de recursos **PSRG**.</span><span class="sxs-lookup"><span data-stu-id="6efe5-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="6efe5-113">True</span><span class="sxs-lookup"><span data-stu-id="6efe5-113">True</span></span>

## <span data-ttu-id="6efe5-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6efe5-114">PARAMETERS</span></span>

### <span data-ttu-id="6efe5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6efe5-115">-AsJob</span></span>
<span data-ttu-id="6efe5-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6efe5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6efe5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6efe5-117">-DefaultProfile</span></span>
<span data-ttu-id="6efe5-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6efe5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6efe5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6efe5-119">-Force</span></span>
<span data-ttu-id="6efe5-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="6efe5-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="6efe5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6efe5-121">-InputObject</span></span>
<span data-ttu-id="6efe5-122">O objeto Identity.</span><span class="sxs-lookup"><span data-stu-id="6efe5-122">The Identity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6efe5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6efe5-123">-Name</span></span>
<span data-ttu-id="6efe5-124">O nome da identidade.</span><span class="sxs-lookup"><span data-stu-id="6efe5-124">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6efe5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6efe5-125">-ResourceGroupName</span></span>
<span data-ttu-id="6efe5-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6efe5-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6efe5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6efe5-127">-ResourceId</span></span>
<span data-ttu-id="6efe5-128">A ID de recurso da Identidade.</span><span class="sxs-lookup"><span data-stu-id="6efe5-128">The Identity's resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6efe5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6efe5-129">-Confirm</span></span>
<span data-ttu-id="6efe5-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6efe5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6efe5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6efe5-131">-WhatIf</span></span>
<span data-ttu-id="6efe5-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6efe5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6efe5-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6efe5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6efe5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6efe5-134">CommonParameters</span></span>
<span data-ttu-id="6efe5-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6efe5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6efe5-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6efe5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6efe5-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6efe5-137">INPUTS</span></span>

### <span data-ttu-id="6efe5-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6efe5-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="6efe5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6efe5-139">System.String</span></span>

## <span data-ttu-id="6efe5-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6efe5-140">OUTPUTS</span></span>

### <span data-ttu-id="6efe5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6efe5-141">System.Boolean</span></span>

## <span data-ttu-id="6efe5-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="6efe5-142">NOTES</span></span>

## <span data-ttu-id="6efe5-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6efe5-143">RELATED LINKS</span></span>
