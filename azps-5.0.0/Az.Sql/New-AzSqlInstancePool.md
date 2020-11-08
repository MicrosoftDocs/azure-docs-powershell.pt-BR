---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 1b4f405e9bf6377855439d1f6d3cad9f0538920f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116669"
---
# <span data-ttu-id="385b1-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="385b1-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="385b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="385b1-102">SYNOPSIS</span></span>
<span data-ttu-id="385b1-103">Cria um pool de instâncias do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="385b1-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="385b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="385b1-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="385b1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="385b1-105">DESCRIPTION</span></span>
<span data-ttu-id="385b1-106">O cmdlet **New-AzSqlInstancePool** cria um pool de instâncias do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="385b1-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="385b1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="385b1-107">EXAMPLES</span></span>

### <span data-ttu-id="385b1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="385b1-108">Example 1</span></span>
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

<span data-ttu-id="385b1-109">Esse comando cria um novo pool de instâncias do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="385b1-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="385b1-110">OS</span><span class="sxs-lookup"><span data-stu-id="385b1-110">PARAMETERS</span></span>

### <span data-ttu-id="385b1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="385b1-111">-AsJob</span></span>
<span data-ttu-id="385b1-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="385b1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="385b1-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="385b1-113">-ComputeGeneration</span></span>
<span data-ttu-id="385b1-114">A geração de computação do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="385b1-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="385b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385b1-115">-DefaultProfile</span></span>
<span data-ttu-id="385b1-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="385b1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="385b1-117">-Edição</span><span class="sxs-lookup"><span data-stu-id="385b1-117">-Edition</span></span>
<span data-ttu-id="385b1-118">A edição do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="385b1-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="385b1-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="385b1-119">-LicenseType</span></span>
<span data-ttu-id="385b1-120">Determina qual tipo de licença usar.</span><span class="sxs-lookup"><span data-stu-id="385b1-120">Determines which License Type to use.</span></span>
<span data-ttu-id="385b1-121">Os valores possíveis são BasePrice (com desconto AHB) e LicenseIncluded (sem desconto AHB).</span><span class="sxs-lookup"><span data-stu-id="385b1-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="385b1-122">-Local</span><span class="sxs-lookup"><span data-stu-id="385b1-122">-Location</span></span>
<span data-ttu-id="385b1-123">O local para criar o pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="385b1-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="385b1-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="385b1-124">-Name</span></span>
<span data-ttu-id="385b1-125">O nome do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="385b1-125">The name of the instance pool.</span></span>

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

### <span data-ttu-id="385b1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="385b1-126">-ResourceGroupName</span></span>
<span data-ttu-id="385b1-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="385b1-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="385b1-128">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="385b1-128">-SubnetId</span></span>
<span data-ttu-id="385b1-129">A ID de sub-rede a ser usada para criação de pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="385b1-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="385b1-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="385b1-130">-Tag</span></span>
<span data-ttu-id="385b1-131">As marcas a serem associadas à instância</span><span class="sxs-lookup"><span data-stu-id="385b1-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="385b1-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="385b1-132">-VCore</span></span>
<span data-ttu-id="385b1-133">Determina a quantidade de VCore a ser associada à instância.</span><span class="sxs-lookup"><span data-stu-id="385b1-133">Determines how much VCore to associate with instance.</span></span>

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

### <span data-ttu-id="385b1-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="385b1-134">-Confirm</span></span>
<span data-ttu-id="385b1-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="385b1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="385b1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="385b1-136">-WhatIf</span></span>
<span data-ttu-id="385b1-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="385b1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="385b1-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="385b1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="385b1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385b1-139">CommonParameters</span></span>
<span data-ttu-id="385b1-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="385b1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385b1-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="385b1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385b1-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="385b1-142">INPUTS</span></span>

### <span data-ttu-id="385b1-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="385b1-143">None</span></span>

## <span data-ttu-id="385b1-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="385b1-144">OUTPUTS</span></span>

### <span data-ttu-id="385b1-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="385b1-145">System.Object</span></span>
## <span data-ttu-id="385b1-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="385b1-146">NOTES</span></span>

## <span data-ttu-id="385b1-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="385b1-147">RELATED LINKS</span></span>
