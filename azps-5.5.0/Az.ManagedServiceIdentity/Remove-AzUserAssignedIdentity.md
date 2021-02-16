---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 4e133ef82e61d34e4e2915a37cc3f0e0d1e61382
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113591"
---
# <span data-ttu-id="70822-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="70822-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="70822-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70822-102">SYNOPSIS</span></span>
<span data-ttu-id="70822-103">Remove uma identidade atribuída pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="70822-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="70822-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70822-104">SYNTAX</span></span>

### <span data-ttu-id="70822-105">ResourceGroupAndNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="70822-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70822-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70822-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70822-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70822-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70822-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="70822-108">DESCRIPTION</span></span>
<span data-ttu-id="70822-109">A **Remove-AzUserAssignedIdentity** exclui a identidade atribuída pelo usuário especificada.</span><span class="sxs-lookup"><span data-stu-id="70822-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="70822-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="70822-110">EXAMPLES</span></span>

### <span data-ttu-id="70822-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="70822-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="70822-112">Este cmdlet de exemplo exclui a **ID1 de** identidade no grupo de recursos **PSRG.**</span><span class="sxs-lookup"><span data-stu-id="70822-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="70822-113">Verdade</span><span class="sxs-lookup"><span data-stu-id="70822-113">True</span></span>

## <span data-ttu-id="70822-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70822-114">PARAMETERS</span></span>

### <span data-ttu-id="70822-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70822-115">-AsJob</span></span>
<span data-ttu-id="70822-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="70822-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70822-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70822-117">-DefaultProfile</span></span>
<span data-ttu-id="70822-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="70822-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70822-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="70822-119">-Force</span></span>
<span data-ttu-id="70822-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="70822-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="70822-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70822-121">-InputObject</span></span>
<span data-ttu-id="70822-122">O objeto Identity.</span><span class="sxs-lookup"><span data-stu-id="70822-122">The Identity object.</span></span>

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

### <span data-ttu-id="70822-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="70822-123">-Name</span></span>
<span data-ttu-id="70822-124">O nome da identidade.</span><span class="sxs-lookup"><span data-stu-id="70822-124">The Identity name.</span></span>

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

### <span data-ttu-id="70822-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70822-125">-ResourceGroupName</span></span>
<span data-ttu-id="70822-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="70822-126">The resource group name.</span></span>

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

### <span data-ttu-id="70822-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70822-127">-ResourceId</span></span>
<span data-ttu-id="70822-128">A ID de recurso da Identidade.</span><span class="sxs-lookup"><span data-stu-id="70822-128">The Identity's resource id.</span></span>

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

### <span data-ttu-id="70822-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="70822-129">-Confirm</span></span>
<span data-ttu-id="70822-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70822-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70822-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70822-131">-WhatIf</span></span>
<span data-ttu-id="70822-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="70822-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70822-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="70822-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70822-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70822-134">CommonParameters</span></span>
<span data-ttu-id="70822-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70822-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70822-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70822-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70822-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="70822-137">INPUTS</span></span>

### <span data-ttu-id="70822-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="70822-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="70822-139">System.String</span><span class="sxs-lookup"><span data-stu-id="70822-139">System.String</span></span>

## <span data-ttu-id="70822-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="70822-140">OUTPUTS</span></span>

### <span data-ttu-id="70822-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="70822-141">System.Boolean</span></span>

## <span data-ttu-id="70822-142">Notas</span><span class="sxs-lookup"><span data-stu-id="70822-142">NOTES</span></span>

## <span data-ttu-id="70822-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70822-143">RELATED LINKS</span></span>
