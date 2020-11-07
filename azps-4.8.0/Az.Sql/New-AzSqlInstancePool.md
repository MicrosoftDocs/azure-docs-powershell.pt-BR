---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 1b4f405e9bf6377855439d1f6d3cad9f0538920f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954584"
---
# <span data-ttu-id="44f16-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="44f16-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="44f16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44f16-102">SYNOPSIS</span></span>
<span data-ttu-id="44f16-103">Cria um pool de instâncias do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="44f16-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="44f16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44f16-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44f16-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44f16-105">DESCRIPTION</span></span>
<span data-ttu-id="44f16-106">O cmdlet **New-AzSqlInstancePool** cria um pool de instâncias do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="44f16-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="44f16-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44f16-107">EXAMPLES</span></span>

### <span data-ttu-id="44f16-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44f16-108">Example 1</span></span>
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

<span data-ttu-id="44f16-109">Esse comando cria um novo pool de instâncias do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="44f16-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="44f16-110">OS</span><span class="sxs-lookup"><span data-stu-id="44f16-110">PARAMETERS</span></span>

### <span data-ttu-id="44f16-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44f16-111">-AsJob</span></span>
<span data-ttu-id="44f16-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="44f16-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44f16-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="44f16-113">-ComputeGeneration</span></span>
<span data-ttu-id="44f16-114">A geração de computação do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="44f16-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="44f16-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44f16-115">-DefaultProfile</span></span>
<span data-ttu-id="44f16-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44f16-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44f16-117">-Edição</span><span class="sxs-lookup"><span data-stu-id="44f16-117">-Edition</span></span>
<span data-ttu-id="44f16-118">A edição do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="44f16-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="44f16-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="44f16-119">-LicenseType</span></span>
<span data-ttu-id="44f16-120">Determina qual tipo de licença usar.</span><span class="sxs-lookup"><span data-stu-id="44f16-120">Determines which License Type to use.</span></span>
<span data-ttu-id="44f16-121">Os valores possíveis são BasePrice (com desconto AHB) e LicenseIncluded (sem desconto AHB).</span><span class="sxs-lookup"><span data-stu-id="44f16-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="44f16-122">-Local</span><span class="sxs-lookup"><span data-stu-id="44f16-122">-Location</span></span>
<span data-ttu-id="44f16-123">O local para criar o pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="44f16-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="44f16-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="44f16-124">-Name</span></span>
<span data-ttu-id="44f16-125">O nome do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="44f16-125">The name of the instance pool.</span></span>

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

### <span data-ttu-id="44f16-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44f16-126">-ResourceGroupName</span></span>
<span data-ttu-id="44f16-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44f16-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="44f16-128">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="44f16-128">-SubnetId</span></span>
<span data-ttu-id="44f16-129">A ID de sub-rede a ser usada para criação de pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="44f16-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="44f16-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="44f16-130">-Tag</span></span>
<span data-ttu-id="44f16-131">As marcas a serem associadas à instância</span><span class="sxs-lookup"><span data-stu-id="44f16-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="44f16-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="44f16-132">-VCore</span></span>
<span data-ttu-id="44f16-133">Determina a quantidade de VCore a ser associada à instância.</span><span class="sxs-lookup"><span data-stu-id="44f16-133">Determines how much VCore to associate with instance.</span></span>

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

### <span data-ttu-id="44f16-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="44f16-134">-Confirm</span></span>
<span data-ttu-id="44f16-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44f16-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44f16-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44f16-136">-WhatIf</span></span>
<span data-ttu-id="44f16-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44f16-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44f16-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44f16-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44f16-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44f16-139">CommonParameters</span></span>
<span data-ttu-id="44f16-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44f16-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44f16-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44f16-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44f16-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44f16-142">INPUTS</span></span>

### <span data-ttu-id="44f16-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="44f16-143">None</span></span>

## <span data-ttu-id="44f16-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44f16-144">OUTPUTS</span></span>

### <span data-ttu-id="44f16-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="44f16-145">System.Object</span></span>
## <span data-ttu-id="44f16-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44f16-146">NOTES</span></span>

## <span data-ttu-id="44f16-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44f16-147">RELATED LINKS</span></span>
