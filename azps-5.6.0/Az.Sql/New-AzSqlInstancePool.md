---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 818e76c9ea46b2593b3bdd3871f417dbaca044a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888596"
---
# <span data-ttu-id="44337-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="44337-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="44337-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44337-102">SYNOPSIS</span></span>
<span data-ttu-id="44337-103">Cria um pool de instâncias SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="44337-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="44337-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="44337-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44337-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="44337-105">DESCRIPTION</span></span>
<span data-ttu-id="44337-106">O cmdlet **New-AzSqlInstancePool** cria um pool de instâncias SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="44337-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="44337-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44337-107">EXAMPLES</span></span>

### <span data-ttu-id="44337-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44337-108">Example 1</span></span>
```powershell
PS C:\> New-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0 -Location canadacentral -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -Edition GeneralPurpose -ComputeGeneration Gen5 -LicenseType LicenseIncluded
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="44337-109">Este comando cria um novo pool de instâncias SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="44337-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="44337-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="44337-110">PARAMETERS</span></span>

### <span data-ttu-id="44337-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44337-111">-AsJob</span></span>
<span data-ttu-id="44337-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="44337-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44337-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="44337-113">-ComputeGeneration</span></span>
<span data-ttu-id="44337-114">A geração de computação para o pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="44337-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="44337-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44337-115">-DefaultProfile</span></span>
<span data-ttu-id="44337-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44337-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44337-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="44337-117">-Edition</span></span>
<span data-ttu-id="44337-118">A edição do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="44337-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="44337-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="44337-119">-LicenseType</span></span>
<span data-ttu-id="44337-120">Determina qual Tipo de Licença usar.</span><span class="sxs-lookup"><span data-stu-id="44337-120">Determines which License Type to use.</span></span>
<span data-ttu-id="44337-121">Os valores possíveis são BasePrice (com desconto AHB) e LicenseIncluded (sem desconto AHB).</span><span class="sxs-lookup"><span data-stu-id="44337-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="44337-122">-Location</span><span class="sxs-lookup"><span data-stu-id="44337-122">-Location</span></span>
<span data-ttu-id="44337-123">O local para criar o pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="44337-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="44337-124">-Name</span><span class="sxs-lookup"><span data-stu-id="44337-124">-Name</span></span>
<span data-ttu-id="44337-125">O nome do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="44337-125">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44337-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44337-126">-ResourceGroupName</span></span>
<span data-ttu-id="44337-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44337-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44337-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="44337-128">-SubnetId</span></span>
<span data-ttu-id="44337-129">A id da sub-rede a ser usada para criação de pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="44337-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="44337-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="44337-130">-Tag</span></span>
<span data-ttu-id="44337-131">As marcas a associar à instância</span><span class="sxs-lookup"><span data-stu-id="44337-131">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44337-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="44337-132">-VCore</span></span>
<span data-ttu-id="44337-133">Determina quanto VCore deve ser associado à instância.</span><span class="sxs-lookup"><span data-stu-id="44337-133">Determines how much VCore to associate with instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: VCores

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44337-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44337-134">-Confirm</span></span>
<span data-ttu-id="44337-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44337-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44337-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44337-136">-WhatIf</span></span>
<span data-ttu-id="44337-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44337-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44337-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44337-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44337-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44337-139">CommonParameters</span></span>
<span data-ttu-id="44337-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44337-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44337-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44337-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44337-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44337-142">INPUTS</span></span>

### <span data-ttu-id="44337-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="44337-143">None</span></span>

## <span data-ttu-id="44337-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="44337-144">OUTPUTS</span></span>

### <span data-ttu-id="44337-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="44337-145">System.Object</span></span>
## <span data-ttu-id="44337-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="44337-146">NOTES</span></span>

## <span data-ttu-id="44337-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44337-147">RELATED LINKS</span></span>
