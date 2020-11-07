---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: 551371aa6cb8e04c6fbd011ae7c0903004640acb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773756"
---
# <span data-ttu-id="9f153-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="9f153-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="9f153-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f153-102">SYNOPSIS</span></span>
<span data-ttu-id="9f153-103">Define as propriedades de um pool de instâncias do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f153-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="9f153-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f153-104">SYNTAX</span></span>

### <span data-ttu-id="9f153-105">DefaultSetInstancePoolParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9f153-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f153-106">InputObjectSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f153-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f153-107">ResourceIdSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f153-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f153-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f153-108">DESCRIPTION</span></span>
<span data-ttu-id="9f153-109">O cmdlet **set-AzSqlInstancePool** modifica as propriedades de um pool de instâncias do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f153-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="9f153-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f153-110">EXAMPLES</span></span>

### <span data-ttu-id="9f153-111">Exemplo 1: definir um tipo de licença de pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="9f153-111">Example 1 : Set an instance pool license type</span></span>
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

<span data-ttu-id="9f153-112">Esse comando define o tipo de licença e/ou as marcas de um pool de instâncias chamado instancePool0.</span><span class="sxs-lookup"><span data-stu-id="9f153-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="9f153-113">Exemplo 2: definir um tipo de licença de pool de instâncias usando um objeto de pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="9f153-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
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

<span data-ttu-id="9f153-114">Esse comando define o tipo de licença e/ou as marcas para um pool de instâncias usando um objeto de pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="9f153-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="9f153-115">Exemplo 3: definir um tipo de licença de pool de instâncias usando uma ID de recurso do pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="9f153-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
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

<span data-ttu-id="9f153-116">Esse comando define o tipo de licença e/ou as marcas de um pool de instâncias chamado instancePool0.</span><span class="sxs-lookup"><span data-stu-id="9f153-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="9f153-117">OS</span><span class="sxs-lookup"><span data-stu-id="9f153-117">PARAMETERS</span></span>

### <span data-ttu-id="9f153-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f153-118">-AsJob</span></span>
<span data-ttu-id="9f153-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9f153-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f153-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f153-120">-DefaultProfile</span></span>
<span data-ttu-id="9f153-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f153-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f153-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f153-122">-InputObject</span></span>
<span data-ttu-id="9f153-123">O objeto de entrada do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="9f153-123">The instance pool input object.</span></span>

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

### <span data-ttu-id="9f153-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9f153-124">-LicenseType</span></span>
<span data-ttu-id="9f153-125">Determina qual tipo de licença usar.</span><span class="sxs-lookup"><span data-stu-id="9f153-125">Determines which License Type to use.</span></span>
<span data-ttu-id="9f153-126">Os valores possíveis são BasePrice (com desconto AHB) e LicenseIncluded (sem desconto AHB).</span><span class="sxs-lookup"><span data-stu-id="9f153-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="9f153-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f153-127">-Name</span></span>
<span data-ttu-id="9f153-128">O nome do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="9f153-128">The name of the instance pool.</span></span>

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

### <span data-ttu-id="9f153-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f153-129">-ResourceGroupName</span></span>
<span data-ttu-id="9f153-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f153-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="9f153-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f153-131">-ResourceId</span></span>
<span data-ttu-id="9f153-132">O identificador de recurso do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="9f153-132">The instance pool resource identifier.</span></span>

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

### <span data-ttu-id="9f153-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="9f153-133">-Tag</span></span>
<span data-ttu-id="9f153-134">As marcas a serem associadas à instância</span><span class="sxs-lookup"><span data-stu-id="9f153-134">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="9f153-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9f153-135">-Confirm</span></span>
<span data-ttu-id="9f153-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f153-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f153-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f153-137">-WhatIf</span></span>
<span data-ttu-id="9f153-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9f153-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f153-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f153-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f153-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f153-140">CommonParameters</span></span>
<span data-ttu-id="9f153-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f153-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f153-142">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f153-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f153-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f153-143">INPUTS</span></span>

### <span data-ttu-id="9f153-144">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="9f153-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="9f153-145">System. String</span><span class="sxs-lookup"><span data-stu-id="9f153-145">System.String</span></span>

## <span data-ttu-id="9f153-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f153-146">OUTPUTS</span></span>

### <span data-ttu-id="9f153-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="9f153-147">System.Object</span></span>
## <span data-ttu-id="9f153-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f153-148">NOTES</span></span>

## <span data-ttu-id="9f153-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f153-149">RELATED LINKS</span></span>
