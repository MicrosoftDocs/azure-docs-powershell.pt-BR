---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 1b4f405e9bf6377855439d1f6d3cad9f0538920f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116141"
---
# <span data-ttu-id="f106c-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="f106c-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="f106c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f106c-102">SYNOPSIS</span></span>
<span data-ttu-id="f106c-103">Cria um pool de Instância SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f106c-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="f106c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f106c-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f106c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f106c-105">DESCRIPTION</span></span>
<span data-ttu-id="f106c-106">O cmdlet **New-AzSqlInstancePool cria** um pool de Instância SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f106c-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="f106c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f106c-107">EXAMPLES</span></span>

### <span data-ttu-id="f106c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f106c-108">Example 1</span></span>
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

<span data-ttu-id="f106c-109">Esse comando cria um novo pool de Instância SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f106c-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="f106c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f106c-110">PARAMETERS</span></span>

### <span data-ttu-id="f106c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f106c-111">-AsJob</span></span>
<span data-ttu-id="f106c-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f106c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f106c-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="f106c-113">-ComputeGeneration</span></span>
<span data-ttu-id="f106c-114">A geração de cálculo para o pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="f106c-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="f106c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f106c-115">-DefaultProfile</span></span>
<span data-ttu-id="f106c-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f106c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f106c-117">-Edição</span><span class="sxs-lookup"><span data-stu-id="f106c-117">-Edition</span></span>
<span data-ttu-id="f106c-118">A edição do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="f106c-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="f106c-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f106c-119">-LicenseType</span></span>
<span data-ttu-id="f106c-120">Determina qual Tipo de Licença usar.</span><span class="sxs-lookup"><span data-stu-id="f106c-120">Determines which License Type to use.</span></span>
<span data-ttu-id="f106c-121">Os valores possíveis são o Preço Base (com desconto AHB) e o LicenseInc inc conforme (sem desconto AHB).</span><span class="sxs-lookup"><span data-stu-id="f106c-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="f106c-122">-Local</span><span class="sxs-lookup"><span data-stu-id="f106c-122">-Location</span></span>
<span data-ttu-id="f106c-123">O local para criar o pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="f106c-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="f106c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f106c-124">-Name</span></span>
<span data-ttu-id="f106c-125">O nome do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="f106c-125">The name of the instance pool.</span></span>

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

### <span data-ttu-id="f106c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f106c-126">-ResourceGroupName</span></span>
<span data-ttu-id="f106c-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f106c-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="f106c-128">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="f106c-128">-SubnetId</span></span>
<span data-ttu-id="f106c-129">A ID da sub-rede a ser usada para a criação de pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="f106c-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="f106c-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="f106c-130">-Tag</span></span>
<span data-ttu-id="f106c-131">As marcas a associar à instância</span><span class="sxs-lookup"><span data-stu-id="f106c-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="f106c-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="f106c-132">-VCore</span></span>
<span data-ttu-id="f106c-133">Determina quanto vCore deve ser associado à instância.</span><span class="sxs-lookup"><span data-stu-id="f106c-133">Determines how much VCore to associate with instance.</span></span>

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

### <span data-ttu-id="f106c-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f106c-134">-Confirm</span></span>
<span data-ttu-id="f106c-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f106c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f106c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f106c-136">-WhatIf</span></span>
<span data-ttu-id="f106c-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f106c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f106c-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f106c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f106c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f106c-139">CommonParameters</span></span>
<span data-ttu-id="f106c-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f106c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f106c-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f106c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f106c-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="f106c-142">INPUTS</span></span>

### <span data-ttu-id="f106c-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f106c-143">None</span></span>

## <span data-ttu-id="f106c-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="f106c-144">OUTPUTS</span></span>

### <span data-ttu-id="f106c-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="f106c-145">System.Object</span></span>
## <span data-ttu-id="f106c-146">Notas</span><span class="sxs-lookup"><span data-stu-id="f106c-146">NOTES</span></span>

## <span data-ttu-id="f106c-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f106c-147">RELATED LINKS</span></span>
