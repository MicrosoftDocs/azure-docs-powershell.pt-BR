---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: 8ae2a7acef3459ff1f9310511a3114a609cc6459
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886796"
---
# <span data-ttu-id="d9bad-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d9bad-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="d9bad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9bad-102">SYNOPSIS</span></span>
<span data-ttu-id="d9bad-103">Cria um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9bad-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="d9bad-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d9bad-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9bad-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d9bad-105">DESCRIPTION</span></span>
<span data-ttu-id="d9bad-106">O cmdlet **New-AzAvailabilitySet** cria um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9bad-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="d9bad-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9bad-107">EXAMPLES</span></span>

### <span data-ttu-id="d9bad-108">Exemplo 1: Criar um conjunto de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="d9bad-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="d9bad-109">Este comando cria um conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d9bad-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d9bad-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d9bad-110">PARAMETERS</span></span>

### <span data-ttu-id="d9bad-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9bad-111">-AsJob</span></span>
<span data-ttu-id="d9bad-112">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="d9bad-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d9bad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9bad-113">-DefaultProfile</span></span>
<span data-ttu-id="d9bad-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d9bad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9bad-115">-Location</span><span class="sxs-lookup"><span data-stu-id="d9bad-115">-Location</span></span>
<span data-ttu-id="d9bad-116">Especifica o local do conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="d9bad-116">Specifies the location for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9bad-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d9bad-117">-Name</span></span>
<span data-ttu-id="d9bad-118">Especifica um nome para o conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="d9bad-118">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9bad-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="d9bad-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="d9bad-120">Especifica a contagem de domínios de falha da plataforma.</span><span class="sxs-lookup"><span data-stu-id="d9bad-120">Specifies the platform fault domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9bad-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="d9bad-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="d9bad-122">Especifica a contagem de domínios de atualização da plataforma.</span><span class="sxs-lookup"><span data-stu-id="d9bad-122">Specifies the platform update domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9bad-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="d9bad-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="d9bad-124">A id de recurso do Grupo de Posicionamento de Proximidade a ser usado com esse conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="d9bad-124">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9bad-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9bad-125">-ResourceGroupName</span></span>
<span data-ttu-id="d9bad-126">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d9bad-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9bad-127">-Sku</span><span class="sxs-lookup"><span data-stu-id="d9bad-127">-Sku</span></span>
<span data-ttu-id="d9bad-128">O nome de Sku.</span><span class="sxs-lookup"><span data-stu-id="d9bad-128">The Name of Sku.</span></span>
<span data-ttu-id="d9bad-129">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d9bad-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9bad-130">Alinhado: para discos gerenciados</span><span class="sxs-lookup"><span data-stu-id="d9bad-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="d9bad-131">Clássico: para discos sem gestão</span><span class="sxs-lookup"><span data-stu-id="d9bad-131">Classic: For unmanaged disks</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9bad-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="d9bad-132">-Tag</span></span>
<span data-ttu-id="d9bad-133">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d9bad-133">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9bad-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9bad-134">CommonParameters</span></span>
<span data-ttu-id="d9bad-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9bad-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9bad-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9bad-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9bad-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9bad-137">INPUTS</span></span>

### <span data-ttu-id="d9bad-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d9bad-138">System.String</span></span>

### <span data-ttu-id="d9bad-139">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d9bad-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d9bad-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d9bad-140">OUTPUTS</span></span>

### <span data-ttu-id="d9bad-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d9bad-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="d9bad-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="d9bad-142">NOTES</span></span>

## <span data-ttu-id="d9bad-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9bad-143">RELATED LINKS</span></span>

[<span data-ttu-id="d9bad-144">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d9bad-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="d9bad-145">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d9bad-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


