---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: db7d9165b8aec6a69f31850f7a37eddb2450e53b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428492"
---
# <span data-ttu-id="ffd16-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="ffd16-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="ffd16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ffd16-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd16-103">Define as propriedades de um pool de instâncias do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ffd16-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="ffd16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffd16-104">SYNTAX</span></span>

### <span data-ttu-id="ffd16-105">DefaultSetInstancePoolParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ffd16-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffd16-106">InputObjectSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffd16-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffd16-107">ResourceIdSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffd16-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffd16-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ffd16-108">DESCRIPTION</span></span>
<span data-ttu-id="ffd16-109">O cmdlet **set-AzSqlInstancePool** modifica as propriedades de um pool de instâncias do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ffd16-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="ffd16-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ffd16-110">EXAMPLES</span></span>

### <span data-ttu-id="ffd16-111">Exemplo 1: definir um tipo de licença de pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="ffd16-111">Example 1 : Set an instance pool license type</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0 -LicenseType LicenseIncluded
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

<span data-ttu-id="ffd16-112">Esse comando define o tipo de licença e/ou as marcas de um pool de instâncias chamado instancePool0.</span><span class="sxs-lookup"><span data-stu-id="ffd16-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="ffd16-113">Exemplo 2: definir um tipo de licença de pool de instâncias usando um objeto de pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="ffd16-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
PS C:\> Set-AzSqlInstancePool -InputObject $instancePool -LicenseType LicenseIncluded
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

<span data-ttu-id="ffd16-114">Esse comando define o tipo de licença e/ou as marcas para um pool de instâncias usando um objeto de pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="ffd16-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="ffd16-115">Exemplo 3: definir um tipo de licença de pool de instâncias usando uma ID de recurso do pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="ffd16-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0" -LicenseType LicenseIncluded
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

<span data-ttu-id="ffd16-116">Esse comando define o tipo de licença e/ou as marcas de um pool de instâncias chamado instancePool0.</span><span class="sxs-lookup"><span data-stu-id="ffd16-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="ffd16-117">OS</span><span class="sxs-lookup"><span data-stu-id="ffd16-117">PARAMETERS</span></span>

### <span data-ttu-id="ffd16-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffd16-118">-AsJob</span></span>
<span data-ttu-id="ffd16-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ffd16-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ffd16-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffd16-120">-DefaultProfile</span></span>
<span data-ttu-id="ffd16-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ffd16-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffd16-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffd16-122">-InputObject</span></span>
<span data-ttu-id="ffd16-123">O objeto de entrada do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="ffd16-123">The instance pool input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InputObjectSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd16-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ffd16-124">-LicenseType</span></span>
<span data-ttu-id="ffd16-125">Determina qual tipo de licença usar.</span><span class="sxs-lookup"><span data-stu-id="ffd16-125">Determines which License Type to use.</span></span>
<span data-ttu-id="ffd16-126">Os valores possíveis são BasePrice (com desconto AHB) e LicenseIncluded (sem desconto AHB).</span><span class="sxs-lookup"><span data-stu-id="ffd16-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="ffd16-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="ffd16-127">-Name</span></span>
<span data-ttu-id="ffd16-128">O nome do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="ffd16-128">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffd16-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffd16-129">-ResourceGroupName</span></span>
<span data-ttu-id="ffd16-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ffd16-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffd16-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffd16-131">-ResourceId</span></span>
<span data-ttu-id="ffd16-132">O identificador de recurso do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="ffd16-132">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd16-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="ffd16-133">-Tag</span></span>
<span data-ttu-id="ffd16-134">As marcas a serem associadas à instância</span><span class="sxs-lookup"><span data-stu-id="ffd16-134">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="ffd16-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ffd16-135">-Confirm</span></span>
<span data-ttu-id="ffd16-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffd16-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffd16-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffd16-137">-WhatIf</span></span>
<span data-ttu-id="ffd16-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ffd16-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffd16-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ffd16-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffd16-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd16-140">CommonParameters</span></span>
<span data-ttu-id="ffd16-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffd16-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd16-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffd16-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd16-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ffd16-143">INPUTS</span></span>

### <span data-ttu-id="ffd16-144">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="ffd16-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="ffd16-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ffd16-145">System.String</span></span>

## <span data-ttu-id="ffd16-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ffd16-146">OUTPUTS</span></span>

### <span data-ttu-id="ffd16-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="ffd16-147">System.Object</span></span>
## <span data-ttu-id="ffd16-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ffd16-148">NOTES</span></span>

## <span data-ttu-id="ffd16-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ffd16-149">RELATED LINKS</span></span>
