---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: 9d63c208daffe6e06da759ff929de120cab58c1c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595931"
---
# <span data-ttu-id="ae472-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="ae472-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="ae472-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae472-102">SYNOPSIS</span></span>
<span data-ttu-id="ae472-103">Exclui a definição de registro.</span><span class="sxs-lookup"><span data-stu-id="ae472-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="ae472-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae472-104">SYNTAX</span></span>

### <span data-ttu-id="ae472-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="ae472-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition -Id <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae472-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ae472-106">ByResourceId</span></span>
```
Remove-AzManagedServicesDefinition -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae472-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ae472-107">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae472-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae472-108">DESCRIPTION</span></span>
<span data-ttu-id="ae472-109">Exclui a definição de registro.</span><span class="sxs-lookup"><span data-stu-id="ae472-109">Deletes the registration definition.</span></span>

## <span data-ttu-id="ae472-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae472-110">EXAMPLES</span></span>

### <span data-ttu-id="ae472-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae472-111">Example 1</span></span>
```powershell
PS C:\> Remove-RegistrationDefinition -Id 0513b566-cab0-4fef-9b53-a285cd33389f
```

<span data-ttu-id="ae472-112">Remove a definição de registro fornecida pelo identificador de ti.</span><span class="sxs-lookup"><span data-stu-id="ae472-112">Removes the registration definition given it identifier.</span></span>

### <span data-ttu-id="ae472-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ae472-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzManagedServicesDefinition -ResourceId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/11b7c937-c5c1-4dd1-9a77-204591f93fcd

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
11b7c937-c5c1-4dd1-9a77-204591f93fcd bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="ae472-114">Remove a definição de registro de acordo com a ID de recurso totalmente qualificada.</span><span class="sxs-lookup"><span data-stu-id="ae472-114">Removes the registration definition given the fully qualified resource id.</span></span> 

### <span data-ttu-id="ae472-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ae472-115">Example 3</span></span>
```powershell
PS C:\> $def = New-AzManagedServicesDefinition -RegistrationDefinitionName 572e1807-b80b-4401-9128-1968f432a5ad -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7"
PS C:\> Remove-AzManagedServicesDefinition -InputObject $def

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
eee59839-119f-453f-adec-4a72a8687125 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="ae472-116">Exclui a definição de registro fornecida ao objeto.</span><span class="sxs-lookup"><span data-stu-id="ae472-116">Deletes the registration definition given the object.</span></span>

## <span data-ttu-id="ae472-117">OS</span><span class="sxs-lookup"><span data-stu-id="ae472-117">PARAMETERS</span></span>

### <span data-ttu-id="ae472-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae472-118">-AsJob</span></span>
<span data-ttu-id="ae472-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ae472-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae472-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae472-120">-DefaultProfile</span></span>
<span data-ttu-id="ae472-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae472-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae472-122">-ID</span><span class="sxs-lookup"><span data-stu-id="ae472-122">-Id</span></span>
<span data-ttu-id="ae472-123">O identificador de definição de registro.</span><span class="sxs-lookup"><span data-stu-id="ae472-123">The registration definition identifier.</span></span>

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

### <span data-ttu-id="ae472-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae472-124">-InputObject</span></span>
<span data-ttu-id="ae472-125">O objeto de definição de registro.</span><span class="sxs-lookup"><span data-stu-id="ae472-125">The registration definition object.</span></span>

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

### <span data-ttu-id="ae472-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae472-126">-ResourceId</span></span>
<span data-ttu-id="ae472-127">ResourceId da definição de registro</span><span class="sxs-lookup"><span data-stu-id="ae472-127">ResourceId of the registration definition</span></span>

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

### <span data-ttu-id="ae472-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae472-128">-Confirm</span></span>
<span data-ttu-id="ae472-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae472-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae472-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae472-130">-WhatIf</span></span>
<span data-ttu-id="ae472-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae472-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae472-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae472-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae472-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae472-133">CommonParameters</span></span>
<span data-ttu-id="ae472-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae472-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae472-135">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae472-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae472-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae472-136">INPUTS</span></span>

### <span data-ttu-id="ae472-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ae472-137">None</span></span>

## <span data-ttu-id="ae472-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae472-138">OUTPUTS</span></span>

### <span data-ttu-id="ae472-139">Microsoft. Azure. PowerShell. cmdlets. Managedservices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="ae472-139">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="ae472-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae472-140">NOTES</span></span>

## <span data-ttu-id="ae472-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae472-141">RELATED LINKS</span></span>
