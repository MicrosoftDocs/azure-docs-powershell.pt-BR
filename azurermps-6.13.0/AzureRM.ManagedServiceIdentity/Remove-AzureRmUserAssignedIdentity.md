---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/remove-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 03d73ac28bc1869452ecc96b5c867fcbb8c372c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610301"
---
# <span data-ttu-id="b2623-101">Remove-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b2623-101">Remove-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="b2623-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2623-102">SYNOPSIS</span></span>
<span data-ttu-id="b2623-103">Remove uma identidade atribuída pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="b2623-103">Removes a User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2623-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2623-104">SYNTAX</span></span>

### <span data-ttu-id="b2623-105">ResourceGroupAndNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b2623-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2623-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2623-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2623-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2623-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2623-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2623-108">DESCRIPTION</span></span>
<span data-ttu-id="b2623-109">O **Remove-AzureRmUserAssignedIdentity** exclui a identidade atribuída pelo usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="b2623-109">The **Remove-AzureRmUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="b2623-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2623-110">EXAMPLES</span></span>

### <span data-ttu-id="b2623-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2623-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzurRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="b2623-112">Este cmdlet de exemplo exclui a identidade **ID1** em **PSRG** do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b2623-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="b2623-113">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="b2623-113">True</span></span>

## <span data-ttu-id="b2623-114">OS</span><span class="sxs-lookup"><span data-stu-id="b2623-114">PARAMETERS</span></span>

### <span data-ttu-id="b2623-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2623-115">-AsJob</span></span>
<span data-ttu-id="b2623-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b2623-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2623-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2623-117">-DefaultProfile</span></span>
<span data-ttu-id="b2623-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2623-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2623-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b2623-119">-Force</span></span>
<span data-ttu-id="b2623-120">{{Descrição da força de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="b2623-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="b2623-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2623-121">-InputObject</span></span>
<span data-ttu-id="b2623-122">O objeto Identity.</span><span class="sxs-lookup"><span data-stu-id="b2623-122">The Identity object.</span></span>

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

### <span data-ttu-id="b2623-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2623-123">-Name</span></span>
<span data-ttu-id="b2623-124">O nome da identidade.</span><span class="sxs-lookup"><span data-stu-id="b2623-124">The Identity name.</span></span>

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

### <span data-ttu-id="b2623-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2623-125">-ResourceGroupName</span></span>
<span data-ttu-id="b2623-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b2623-126">The resource group name.</span></span>

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

### <span data-ttu-id="b2623-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2623-127">-ResourceId</span></span>
<span data-ttu-id="b2623-128">A ID do recurso da identidade.</span><span class="sxs-lookup"><span data-stu-id="b2623-128">The Identity's resource id.</span></span>

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

### <span data-ttu-id="b2623-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b2623-129">-Confirm</span></span>
<span data-ttu-id="b2623-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2623-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2623-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2623-131">-WhatIf</span></span>
<span data-ttu-id="b2623-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2623-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2623-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2623-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2623-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2623-134">CommonParameters</span></span>
<span data-ttu-id="b2623-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2623-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2623-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2623-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2623-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2623-137">INPUTS</span></span>

### <span data-ttu-id="b2623-138">Microsoft. Azure. Commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b2623-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>
<span data-ttu-id="b2623-139">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b2623-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="b2623-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b2623-140">System.String</span></span>

## <span data-ttu-id="b2623-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2623-141">OUTPUTS</span></span>

### <span data-ttu-id="b2623-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2623-142">System.Boolean</span></span>

## <span data-ttu-id="b2623-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2623-143">NOTES</span></span>

## <span data-ttu-id="b2623-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2623-144">RELATED LINKS</span></span>
