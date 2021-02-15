---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: db7d9165b8aec6a69f31850f7a37eddb2450e53b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116124"
---
# <span data-ttu-id="480e8-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="480e8-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="480e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="480e8-102">SYNOPSIS</span></span>
<span data-ttu-id="480e8-103">Define propriedades para um pool de Instância SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="480e8-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="480e8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="480e8-104">SYNTAX</span></span>

### <span data-ttu-id="480e8-105">DefaultSetInstancePoolParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="480e8-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="480e8-106">InputObjectSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="480e8-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="480e8-107">ResourceIdSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="480e8-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="480e8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="480e8-108">DESCRIPTION</span></span>
<span data-ttu-id="480e8-109">O cmdlet **Set-AzSqlInstancePool** modifica as propriedades de um pool de Instância SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="480e8-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="480e8-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="480e8-110">EXAMPLES</span></span>

### <span data-ttu-id="480e8-111">Exemplo 1: Definir um tipo de licença de pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="480e8-111">Example 1 : Set an instance pool license type</span></span>
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

<span data-ttu-id="480e8-112">Esse comando define o tipo de licença e/ou marcas para um pool de instâncias chamado instancePool0.</span><span class="sxs-lookup"><span data-stu-id="480e8-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="480e8-113">Exemplo 2: Definir um tipo de licença de pool de instâncias usando um objeto de pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="480e8-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
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

<span data-ttu-id="480e8-114">Esse comando define o tipo de licença e/ou marcas para um pool de instâncias usando um objeto de pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="480e8-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="480e8-115">Exemplo 3: Definir um tipo de licença de pool de instâncias usando uma ID de recurso de pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="480e8-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
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

<span data-ttu-id="480e8-116">Esse comando define o tipo de licença e/ou marcas para um pool de instâncias chamado instancePool0.</span><span class="sxs-lookup"><span data-stu-id="480e8-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="480e8-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="480e8-117">PARAMETERS</span></span>

### <span data-ttu-id="480e8-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="480e8-118">-AsJob</span></span>
<span data-ttu-id="480e8-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="480e8-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="480e8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="480e8-120">-DefaultProfile</span></span>
<span data-ttu-id="480e8-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="480e8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="480e8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="480e8-122">-InputObject</span></span>
<span data-ttu-id="480e8-123">O objeto de entrada do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="480e8-123">The instance pool input object.</span></span>

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

### <span data-ttu-id="480e8-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="480e8-124">-LicenseType</span></span>
<span data-ttu-id="480e8-125">Determina qual Tipo de Licença usar.</span><span class="sxs-lookup"><span data-stu-id="480e8-125">Determines which License Type to use.</span></span>
<span data-ttu-id="480e8-126">Os valores possíveis são o Preço Base (com desconto AHB) e o LicenseInc inc conforme (sem desconto AHB).</span><span class="sxs-lookup"><span data-stu-id="480e8-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="480e8-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="480e8-127">-Name</span></span>
<span data-ttu-id="480e8-128">O nome do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="480e8-128">The name of the instance pool.</span></span>

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

### <span data-ttu-id="480e8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="480e8-129">-ResourceGroupName</span></span>
<span data-ttu-id="480e8-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="480e8-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="480e8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="480e8-131">-ResourceId</span></span>
<span data-ttu-id="480e8-132">O identificador de recurso de pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="480e8-132">The instance pool resource identifier.</span></span>

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

### <span data-ttu-id="480e8-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="480e8-133">-Tag</span></span>
<span data-ttu-id="480e8-134">As marcas a associar à instância</span><span class="sxs-lookup"><span data-stu-id="480e8-134">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="480e8-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="480e8-135">-Confirm</span></span>
<span data-ttu-id="480e8-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="480e8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="480e8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="480e8-137">-WhatIf</span></span>
<span data-ttu-id="480e8-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="480e8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="480e8-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="480e8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="480e8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="480e8-140">CommonParameters</span></span>
<span data-ttu-id="480e8-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="480e8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="480e8-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="480e8-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="480e8-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="480e8-143">INPUTS</span></span>

### <span data-ttu-id="480e8-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="480e8-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="480e8-145">System.String</span><span class="sxs-lookup"><span data-stu-id="480e8-145">System.String</span></span>

## <span data-ttu-id="480e8-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="480e8-146">OUTPUTS</span></span>

### <span data-ttu-id="480e8-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="480e8-147">System.Object</span></span>
## <span data-ttu-id="480e8-148">Notas</span><span class="sxs-lookup"><span data-stu-id="480e8-148">NOTES</span></span>

## <span data-ttu-id="480e8-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="480e8-149">RELATED LINKS</span></span>
