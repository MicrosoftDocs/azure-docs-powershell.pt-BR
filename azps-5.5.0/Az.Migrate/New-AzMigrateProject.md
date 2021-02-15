---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 32c4799f574e94eecee1f7ebf810c2f27bc5eccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117549"
---
# <span data-ttu-id="ea17d-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="ea17d-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="ea17d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea17d-102">SYNOPSIS</span></span>
<span data-ttu-id="ea17d-103">Cria um novo projeto migrar.</span><span class="sxs-lookup"><span data-stu-id="ea17d-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="ea17d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea17d-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ea17d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea17d-105">DESCRIPTION</span></span>
<span data-ttu-id="ea17d-106">Cria um novo projeto migrar.</span><span class="sxs-lookup"><span data-stu-id="ea17d-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="ea17d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ea17d-107">EXAMPLES</span></span>

### <span data-ttu-id="ea17d-108">Exemplo 1: Criar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ea17d-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="ea17d-109">Método para criar um novo projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="ea17d-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="ea17d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea17d-110">PARAMETERS</span></span>

### <span data-ttu-id="ea17d-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="ea17d-111">-ETag</span></span>
<span data-ttu-id="ea17d-112">Especifica o nome do computador V Ltd.</span><span class="sxs-lookup"><span data-stu-id="ea17d-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="ea17d-113">-Local</span><span class="sxs-lookup"><span data-stu-id="ea17d-113">-Location</span></span>
<span data-ttu-id="ea17d-114">Especifica o nome do computador V Ltd.</span><span class="sxs-lookup"><span data-stu-id="ea17d-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="ea17d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea17d-115">-Name</span></span>
<span data-ttu-id="ea17d-116">Especifica o nome do projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="ea17d-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="ea17d-117">-Propriedade</span><span class="sxs-lookup"><span data-stu-id="ea17d-117">-Property</span></span>
<span data-ttu-id="ea17d-118">Especifica as propriedades do projeto.</span><span class="sxs-lookup"><span data-stu-id="ea17d-118">Specifies the project properties.</span></span>
<span data-ttu-id="ea17d-119">Para construir, consulte a seção ANOTAÇÕES para propriedades DE PROPRIEDADE e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="ea17d-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="ea17d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea17d-120">-ResourceGroupName</span></span>
<span data-ttu-id="ea17d-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ea17d-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="ea17d-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea17d-122">-SubscriptionId</span></span>
<span data-ttu-id="ea17d-123">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ea17d-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="ea17d-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ea17d-124">-Confirm</span></span>
<span data-ttu-id="ea17d-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea17d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea17d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea17d-126">-WhatIf</span></span>
<span data-ttu-id="ea17d-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ea17d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea17d-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea17d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea17d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea17d-129">CommonParameters</span></span>
<span data-ttu-id="ea17d-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea17d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea17d-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea17d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea17d-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="ea17d-132">INPUTS</span></span>

## <span data-ttu-id="ea17d-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="ea17d-133">OUTPUTS</span></span>

## <span data-ttu-id="ea17d-134">Notas</span><span class="sxs-lookup"><span data-stu-id="ea17d-134">NOTES</span></span>

<span data-ttu-id="ea17d-135">Aliases</span><span class="sxs-lookup"><span data-stu-id="ea17d-135">ALIASES</span></span>

<span data-ttu-id="ea17d-136">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="ea17d-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ea17d-137">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ea17d-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ea17d-138">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ea17d-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ea17d-139">PROPRIEDADE: <IMigrateProjectProperties> especifica as propriedades do projeto.</span><span class="sxs-lookup"><span data-stu-id="ea17d-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="ea17d-140">`[ProvisioningState <ProvisioningState?>]`: Estado de provisionamento do projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="ea17d-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="ea17d-141">`[RegisteredTool <String[]>]`: Obtém ou define a lista de ferramentas registradas com o projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="ea17d-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="ea17d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea17d-142">RELATED LINKS</span></span>

