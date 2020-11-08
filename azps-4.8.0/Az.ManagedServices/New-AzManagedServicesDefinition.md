---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: 6c9c4b562acbf80dba9b1b414345d5eb8e3ecc60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113530"
---
# <span data-ttu-id="f317e-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="f317e-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="f317e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f317e-102">SYNOPSIS</span></span>
<span data-ttu-id="f317e-103">Cria ou atualiza uma definição de registro.</span><span class="sxs-lookup"><span data-stu-id="f317e-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="f317e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f317e-104">SYNTAX</span></span>

### <span data-ttu-id="f317e-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="f317e-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f317e-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="f317e-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] -PlanName <String>
 -PlanPublisher <String> -PlanProduct <String> -PlanVersion <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f317e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f317e-107">DESCRIPTION</span></span>
<span data-ttu-id="f317e-108">Cria ou atualiza uma definição de registro.</span><span class="sxs-lookup"><span data-stu-id="f317e-108">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="f317e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f317e-109">EXAMPLES</span></span>

### <span data-ttu-id="f317e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f317e-110">Example 1</span></span>
```powershell
PS C:\> PS C:\> New-AzManagedServicesDefinition -Name name -ManagedByTenantId bab3375b-6197-4a15-a44b-16c41faa91d7 -PrincipalId d6f6c88a-5b7a-455e-ba40-ce146d4d3671 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -Description mydef

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fdad02a1-a715-4352-844f-2923233590da bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="f317e-111">Cria ou atualiza uma definição de registro de acordo com os parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="f317e-111">Creates or updates a registration definition given the required parameters.</span></span>

### <span data-ttu-id="f317e-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f317e-112">Example 2</span></span>
```powershell
PS C> New-AzManagedServicesDefinition -Name asd -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7" -PlanName plan -PlanPublisher publisher -PlanProduct product -PlanVersion 0.1

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
8cde7c19-1750-468e-973e-b711549edc35 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="f317e-113">Cria ou atualiza uma definição de registro com os detalhes do plano.</span><span class="sxs-lookup"><span data-stu-id="f317e-113">Creates or updates a registration definition with the plan details.</span></span>

## <span data-ttu-id="f317e-114">OS</span><span class="sxs-lookup"><span data-stu-id="f317e-114">PARAMETERS</span></span>

### <span data-ttu-id="f317e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f317e-115">-AsJob</span></span>
<span data-ttu-id="f317e-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f317e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f317e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f317e-117">-DefaultProfile</span></span>
<span data-ttu-id="f317e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f317e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f317e-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="f317e-119">-Description</span></span>
<span data-ttu-id="f317e-120">A descrição da definição de registro.</span><span class="sxs-lookup"><span data-stu-id="f317e-120">The description of the Registration Definition.</span></span>

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

### <span data-ttu-id="f317e-121">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="f317e-121">-ManagedByTenantId</span></span>
<span data-ttu-id="f317e-122">O identificador de locatário ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="f317e-122">The ManagedBy Tenant Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f317e-123">-PlanName</span><span class="sxs-lookup"><span data-stu-id="f317e-123">-PlanName</span></span>
<span data-ttu-id="f317e-124">O nome do plano.</span><span class="sxs-lookup"><span data-stu-id="f317e-124">The name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f317e-125">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="f317e-125">-PlanProduct</span></span>
<span data-ttu-id="f317e-126">O nome do produto.</span><span class="sxs-lookup"><span data-stu-id="f317e-126">The name of the Product.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f317e-127">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="f317e-127">-PlanPublisher</span></span>
<span data-ttu-id="f317e-128">O nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="f317e-128">The name of the Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f317e-129">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="f317e-129">-PlanVersion</span></span>
<span data-ttu-id="f317e-130">O número da versão do plano.</span><span class="sxs-lookup"><span data-stu-id="f317e-130">The version number of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f317e-131">-Entidade de segurança</span><span class="sxs-lookup"><span data-stu-id="f317e-131">-PrincipalId</span></span>
<span data-ttu-id="f317e-132">O identificador principal do ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="f317e-132">The ManagedBy Principal Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f317e-133">-RegistrationDefinitionName</span><span class="sxs-lookup"><span data-stu-id="f317e-133">-RegistrationDefinitionName</span></span>
<span data-ttu-id="f317e-134">O nome da definição de registro.</span><span class="sxs-lookup"><span data-stu-id="f317e-134">The name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f317e-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f317e-135">-RoleDefinitionId</span></span>
<span data-ttu-id="f317e-136">O identificador de função do provedor de serviços gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f317e-136">The Managed Service Provider's Role Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f317e-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f317e-137">-Confirm</span></span>
<span data-ttu-id="f317e-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f317e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f317e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f317e-139">-WhatIf</span></span>
<span data-ttu-id="f317e-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f317e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f317e-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f317e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f317e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f317e-142">CommonParameters</span></span>
<span data-ttu-id="f317e-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f317e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f317e-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f317e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f317e-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f317e-145">INPUTS</span></span>

### <span data-ttu-id="f317e-146">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f317e-146">None</span></span>

## <span data-ttu-id="f317e-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f317e-147">OUTPUTS</span></span>

### <span data-ttu-id="f317e-148">Microsoft. Azure. PowerShell. cmdlets. Managedservices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="f317e-148">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="f317e-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f317e-149">NOTES</span></span>

## <span data-ttu-id="f317e-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f317e-150">RELATED LINKS</span></span>
