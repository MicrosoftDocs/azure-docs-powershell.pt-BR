---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 32c4799f574e94eecee1f7ebf810c2f27bc5eccf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272685"
---
# <span data-ttu-id="bb2a8-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="bb2a8-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="bb2a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb2a8-102">SYNOPSIS</span></span>
<span data-ttu-id="bb2a8-103">Cria um novo projeto migrar.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="bb2a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb2a8-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bb2a8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb2a8-105">DESCRIPTION</span></span>
<span data-ttu-id="bb2a8-106">Cria um novo projeto migrar.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="bb2a8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb2a8-107">EXAMPLES</span></span>

### <span data-ttu-id="bb2a8-108">Exemplo 1: criar (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb2a8-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="bb2a8-109">Método para criar um novo projeto migrar.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="bb2a8-110">OS</span><span class="sxs-lookup"><span data-stu-id="bb2a8-110">PARAMETERS</span></span>

### <span data-ttu-id="bb2a8-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="bb2a8-111">-ETag</span></span>
<span data-ttu-id="bb2a8-112">Especifica o nome do computador VMware.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="bb2a8-113">-Local</span><span class="sxs-lookup"><span data-stu-id="bb2a8-113">-Location</span></span>
<span data-ttu-id="bb2a8-114">Especifica o nome do computador VMware.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="bb2a8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb2a8-115">-Name</span></span>
<span data-ttu-id="bb2a8-116">Especifica o nome do projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="bb2a8-117">-Propriedade</span><span class="sxs-lookup"><span data-stu-id="bb2a8-117">-Property</span></span>
<span data-ttu-id="bb2a8-118">Especifica as propriedades do projeto.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-118">Specifies the project properties.</span></span>
<span data-ttu-id="bb2a8-119">Para construir, consulte a seção observações para propriedades de propriedades e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="bb2a8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb2a8-120">-ResourceGroupName</span></span>
<span data-ttu-id="bb2a8-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="bb2a8-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb2a8-122">-SubscriptionId</span></span>
<span data-ttu-id="bb2a8-123">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="bb2a8-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bb2a8-124">-Confirm</span></span>
<span data-ttu-id="bb2a8-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb2a8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb2a8-126">-WhatIf</span></span>
<span data-ttu-id="bb2a8-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb2a8-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb2a8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb2a8-129">CommonParameters</span></span>
<span data-ttu-id="bb2a8-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb2a8-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb2a8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb2a8-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb2a8-132">INPUTS</span></span>

## <span data-ttu-id="bb2a8-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb2a8-133">OUTPUTS</span></span>

## <span data-ttu-id="bb2a8-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb2a8-134">NOTES</span></span>

<span data-ttu-id="bb2a8-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bb2a8-135">ALIASES</span></span>

<span data-ttu-id="bb2a8-136">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="bb2a8-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bb2a8-137">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bb2a8-138">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bb2a8-139">Propriedade <IMigrateProjectProperties> : especifica as propriedades do projeto.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="bb2a8-140">`[ProvisioningState <ProvisioningState?>]`: Configuração do estado do projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="bb2a8-141">`[RegisteredTool <String[]>]`: Obtém ou define a lista de ferramentas registradas com o projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="bb2a8-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="bb2a8-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb2a8-142">RELATED LINKS</span></span>

