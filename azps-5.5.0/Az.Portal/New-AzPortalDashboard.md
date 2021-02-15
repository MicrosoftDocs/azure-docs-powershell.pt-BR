---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 80b2289b4f481fff126d9cd5dfc98ca94536cfa0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114577"
---
# <span data-ttu-id="f6e25-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="f6e25-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="f6e25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6e25-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e25-103">Cria ou atualiza um Painel.</span><span class="sxs-lookup"><span data-stu-id="f6e25-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="f6e25-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6e25-104">SYNTAX</span></span>

### <span data-ttu-id="f6e25-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="f6e25-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f6e25-106">Criar</span><span class="sxs-lookup"><span data-stu-id="f6e25-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f6e25-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="f6e25-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f6e25-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6e25-108">DESCRIPTION</span></span>
<span data-ttu-id="f6e25-109">Cria ou atualiza um Painel.</span><span class="sxs-lookup"><span data-stu-id="f6e25-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="f6e25-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f6e25-110">EXAMPLES</span></span>

### <span data-ttu-id="f6e25-111">Exemplo 1: Criar um painel usando um arquivo de modelo de painel</span><span class="sxs-lookup"><span data-stu-id="f6e25-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="f6e25-112">Crie um novo painel usando o arquivo de modelo de painel fornecido.</span><span class="sxs-lookup"><span data-stu-id="f6e25-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="f6e25-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6e25-113">PARAMETERS</span></span>

### <span data-ttu-id="f6e25-114">-Painel</span><span class="sxs-lookup"><span data-stu-id="f6e25-114">-Dashboard</span></span>
<span data-ttu-id="f6e25-115">A definição de recurso de painel compartilhado.</span><span class="sxs-lookup"><span data-stu-id="f6e25-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="f6e25-116">Para construir, confira a seção ANOTAÇÕES para propriedades do PAINEL e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="f6e25-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6e25-117">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="f6e25-117">-DashboardPath</span></span>
<span data-ttu-id="f6e25-118">O Caminho para um modelo de painel existente.</span><span class="sxs-lookup"><span data-stu-id="f6e25-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="f6e25-119">Os modelos de painel podem ser baixados do portal.</span><span class="sxs-lookup"><span data-stu-id="f6e25-119">Dashboard templates may be downloaded from the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e25-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6e25-120">-DefaultProfile</span></span>
<span data-ttu-id="f6e25-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6e25-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e25-122">-Lens</span><span class="sxs-lookup"><span data-stu-id="f6e25-122">-Lens</span></span>
<span data-ttu-id="f6e25-123">As lentes do painel.</span><span class="sxs-lookup"><span data-stu-id="f6e25-123">The dashboard lenses.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e25-124">-Local</span><span class="sxs-lookup"><span data-stu-id="f6e25-124">-Location</span></span>
<span data-ttu-id="f6e25-125">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="f6e25-125">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e25-126">-Metadados</span><span class="sxs-lookup"><span data-stu-id="f6e25-126">-Metadata</span></span>
<span data-ttu-id="f6e25-127">Os metadados do painel.</span><span class="sxs-lookup"><span data-stu-id="f6e25-127">The dashboard metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e25-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6e25-128">-Name</span></span>
<span data-ttu-id="f6e25-129">O nome do painel.</span><span class="sxs-lookup"><span data-stu-id="f6e25-129">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e25-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6e25-130">-ResourceGroupName</span></span>
<span data-ttu-id="f6e25-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f6e25-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="f6e25-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6e25-132">-SubscriptionId</span></span>
<span data-ttu-id="f6e25-133">A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="f6e25-133">The Azure subscription ID.</span></span>
<span data-ttu-id="f6e25-134">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="f6e25-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e25-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="f6e25-135">-Tag</span></span>
<span data-ttu-id="f6e25-136">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="f6e25-136">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e25-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f6e25-137">-Confirm</span></span>
<span data-ttu-id="f6e25-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6e25-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6e25-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6e25-139">-WhatIf</span></span>
<span data-ttu-id="f6e25-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f6e25-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6e25-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6e25-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6e25-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e25-142">CommonParameters</span></span>
<span data-ttu-id="f6e25-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6e25-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e25-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6e25-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e25-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="f6e25-145">INPUTS</span></span>

### <span data-ttu-id="f6e25-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="f6e25-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="f6e25-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="f6e25-147">OUTPUTS</span></span>

### <span data-ttu-id="f6e25-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="f6e25-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="f6e25-149">Notas</span><span class="sxs-lookup"><span data-stu-id="f6e25-149">NOTES</span></span>

<span data-ttu-id="f6e25-150">Aliases</span><span class="sxs-lookup"><span data-stu-id="f6e25-150">ALIASES</span></span>

<span data-ttu-id="f6e25-151">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="f6e25-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f6e25-152">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="f6e25-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6e25-153">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f6e25-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f6e25-154">PAINEL: <IDashboard> a definição de recurso de painel compartilhado.</span><span class="sxs-lookup"><span data-stu-id="f6e25-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="f6e25-155">`Location <String>`: Local do recurso</span><span class="sxs-lookup"><span data-stu-id="f6e25-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="f6e25-156">`[Lens <IDashboardPropertiesLenses>]`: as lentes do painel.</span><span class="sxs-lookup"><span data-stu-id="f6e25-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="f6e25-157">`[(Any) <IDashboardLens>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="f6e25-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f6e25-158">`[Metadata <IDashboardPropertiesMetadata>]`: Os metadados do painel.</span><span class="sxs-lookup"><span data-stu-id="f6e25-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="f6e25-159">`[(Any) <Object>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="f6e25-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f6e25-160">`[Tag <IDashboardTags>]`: Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="f6e25-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="f6e25-161">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="f6e25-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="f6e25-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6e25-162">RELATED LINKS</span></span>

