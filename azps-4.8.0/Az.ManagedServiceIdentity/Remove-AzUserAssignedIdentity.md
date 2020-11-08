---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 4e133ef82e61d34e4e2915a37cc3f0e0d1e61382
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113539"
---
# <span data-ttu-id="f32e2-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f32e2-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="f32e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f32e2-102">SYNOPSIS</span></span>
<span data-ttu-id="f32e2-103">Remove uma identidade atribuída pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f32e2-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="f32e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f32e2-104">SYNTAX</span></span>

### <span data-ttu-id="f32e2-105">ResourceGroupAndNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f32e2-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f32e2-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f32e2-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f32e2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f32e2-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f32e2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f32e2-108">DESCRIPTION</span></span>
<span data-ttu-id="f32e2-109">O **Remove-AzUserAssignedIdentity** exclui a identidade atribuída pelo usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="f32e2-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="f32e2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f32e2-110">EXAMPLES</span></span>

### <span data-ttu-id="f32e2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f32e2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="f32e2-112">Este cmdlet de exemplo exclui a identidade **ID1** em **PSRG** do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f32e2-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="f32e2-113">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="f32e2-113">True</span></span>

## <span data-ttu-id="f32e2-114">OS</span><span class="sxs-lookup"><span data-stu-id="f32e2-114">PARAMETERS</span></span>

### <span data-ttu-id="f32e2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f32e2-115">-AsJob</span></span>
<span data-ttu-id="f32e2-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f32e2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f32e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f32e2-117">-DefaultProfile</span></span>
<span data-ttu-id="f32e2-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f32e2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f32e2-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f32e2-119">-Force</span></span>
<span data-ttu-id="f32e2-120">{{Descrição da força de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="f32e2-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="f32e2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f32e2-121">-InputObject</span></span>
<span data-ttu-id="f32e2-122">O objeto Identity.</span><span class="sxs-lookup"><span data-stu-id="f32e2-122">The Identity object.</span></span>

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

### <span data-ttu-id="f32e2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="f32e2-123">-Name</span></span>
<span data-ttu-id="f32e2-124">O nome da identidade.</span><span class="sxs-lookup"><span data-stu-id="f32e2-124">The Identity name.</span></span>

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

### <span data-ttu-id="f32e2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f32e2-125">-ResourceGroupName</span></span>
<span data-ttu-id="f32e2-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f32e2-126">The resource group name.</span></span>

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

### <span data-ttu-id="f32e2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f32e2-127">-ResourceId</span></span>
<span data-ttu-id="f32e2-128">A ID do recurso da identidade.</span><span class="sxs-lookup"><span data-stu-id="f32e2-128">The Identity's resource id.</span></span>

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

### <span data-ttu-id="f32e2-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f32e2-129">-Confirm</span></span>
<span data-ttu-id="f32e2-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f32e2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f32e2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f32e2-131">-WhatIf</span></span>
<span data-ttu-id="f32e2-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f32e2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f32e2-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f32e2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f32e2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f32e2-134">CommonParameters</span></span>
<span data-ttu-id="f32e2-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f32e2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f32e2-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f32e2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f32e2-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f32e2-137">INPUTS</span></span>

### <span data-ttu-id="f32e2-138">Microsoft. Azure. Commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f32e2-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="f32e2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f32e2-139">System.String</span></span>

## <span data-ttu-id="f32e2-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f32e2-140">OUTPUTS</span></span>

### <span data-ttu-id="f32e2-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f32e2-141">System.Boolean</span></span>

## <span data-ttu-id="f32e2-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f32e2-142">NOTES</span></span>

## <span data-ttu-id="f32e2-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f32e2-143">RELATED LINKS</span></span>
