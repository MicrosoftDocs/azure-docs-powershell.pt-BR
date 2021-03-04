---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 8b3a14c9e8416c1ffc9809d09d664b7809f53a1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889222"
---
# <span data-ttu-id="2b9f4-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="2b9f4-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="2b9f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b9f4-102">SYNOPSIS</span></span>
<span data-ttu-id="2b9f4-103">Cria um novo projeto Migrate.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="2b9f4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2b9f4-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2b9f4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2b9f4-105">DESCRIPTION</span></span>
<span data-ttu-id="2b9f4-106">Cria um novo projeto Migrate.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="2b9f4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b9f4-107">EXAMPLES</span></span>

### <span data-ttu-id="2b9f4-108">Exemplo 1: Criar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2b9f4-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="2b9f4-109">Método para criar um novo projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="2b9f4-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2b9f4-110">PARAMETERS</span></span>

### <span data-ttu-id="2b9f4-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="2b9f4-111">-ETag</span></span>
<span data-ttu-id="2b9f4-112">Especifica o nome da máquina VMware.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="2b9f4-113">-Location</span><span class="sxs-lookup"><span data-stu-id="2b9f4-113">-Location</span></span>
<span data-ttu-id="2b9f4-114">Especifica o nome da máquina VMware.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="2b9f4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2b9f4-115">-Name</span></span>
<span data-ttu-id="2b9f4-116">Especifica o nome do projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="2b9f4-117">-Property</span><span class="sxs-lookup"><span data-stu-id="2b9f4-117">-Property</span></span>
<span data-ttu-id="2b9f4-118">Especifica as propriedades do projeto.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-118">Specifies the project properties.</span></span>
<span data-ttu-id="2b9f4-119">Para construir, consulte a seção NOTES para propriedades PROPERTY e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProjectProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9f4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b9f4-120">-ResourceGroupName</span></span>
<span data-ttu-id="2b9f4-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="2b9f4-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b9f4-122">-SubscriptionId</span></span>
<span data-ttu-id="2b9f4-123">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="2b9f4-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b9f4-124">-Confirm</span></span>
<span data-ttu-id="2b9f4-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b9f4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b9f4-126">-WhatIf</span></span>
<span data-ttu-id="2b9f4-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b9f4-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b9f4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b9f4-129">CommonParameters</span></span>
<span data-ttu-id="2b9f4-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b9f4-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b9f4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b9f4-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b9f4-132">INPUTS</span></span>

## <span data-ttu-id="2b9f4-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2b9f4-133">OUTPUTS</span></span>

## <span data-ttu-id="2b9f4-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="2b9f4-134">NOTES</span></span>

<span data-ttu-id="2b9f4-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2b9f4-135">ALIASES</span></span>

<span data-ttu-id="2b9f4-136">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="2b9f4-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2b9f4-137">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2b9f4-138">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2b9f4-139">PROPRIEDADE <IMigrateProjectProperties> : Especifica as propriedades do projeto.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="2b9f4-140">`[ProvisioningState <ProvisioningState?>]`: Estado de provisionamento do projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="2b9f4-141">`[RegisteredTool <String[]>]`: Obtém ou define a lista de ferramentas registradas no projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="2b9f4-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="2b9f4-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b9f4-142">RELATED LINKS</span></span>

