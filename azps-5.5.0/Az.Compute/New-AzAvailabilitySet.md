---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: cd61e2119ea84ccfc5fb6a7f5fe597e80c9fd417
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112132"
---
# <span data-ttu-id="7f32f-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7f32f-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="7f32f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f32f-102">SYNOPSIS</span></span>
<span data-ttu-id="7f32f-103">Cria um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="7f32f-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="7f32f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f32f-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f32f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f32f-105">DESCRIPTION</span></span>
<span data-ttu-id="7f32f-106">O **cmdlet New-AzAvailabilitySet** cria um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="7f32f-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="7f32f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7f32f-107">EXAMPLES</span></span>

### <span data-ttu-id="7f32f-108">Exemplo 1: Criar um conjunto de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="7f32f-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="7f32f-109">Esse comando cria um conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7f32f-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="7f32f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f32f-110">PARAMETERS</span></span>

### <span data-ttu-id="7f32f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f32f-111">-AsJob</span></span>
<span data-ttu-id="7f32f-112">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="7f32f-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7f32f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f32f-113">-DefaultProfile</span></span>
<span data-ttu-id="7f32f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7f32f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f32f-115">-Local</span><span class="sxs-lookup"><span data-stu-id="7f32f-115">-Location</span></span>
<span data-ttu-id="7f32f-116">Especifica o local do conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="7f32f-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="7f32f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f32f-117">-Name</span></span>
<span data-ttu-id="7f32f-118">Especifica um nome para o conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="7f32f-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="7f32f-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="7f32f-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="7f32f-120">Especifica a contagem de domínios de falha da plataforma.</span><span class="sxs-lookup"><span data-stu-id="7f32f-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="7f32f-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="7f32f-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="7f32f-122">Especifica a contagem de domínios de atualização da plataforma.</span><span class="sxs-lookup"><span data-stu-id="7f32f-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="7f32f-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="7f32f-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="7f32f-124">A ID do recurso do Grupo de Posicionamento de Proximidade a ser usado com esse conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="7f32f-124">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="7f32f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f32f-125">-ResourceGroupName</span></span>
<span data-ttu-id="7f32f-126">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7f32f-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7f32f-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="7f32f-127">-Sku</span></span>
<span data-ttu-id="7f32f-128">O Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="7f32f-128">The Name of Sku.</span></span>
<span data-ttu-id="7f32f-129">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7f32f-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f32f-130">Alinhado: para discos gerenciados</span><span class="sxs-lookup"><span data-stu-id="7f32f-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="7f32f-131">Clássico: Para discos nãomanados</span><span class="sxs-lookup"><span data-stu-id="7f32f-131">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="7f32f-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="7f32f-132">-Tag</span></span>
<span data-ttu-id="7f32f-133">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="7f32f-133">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="7f32f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f32f-134">CommonParameters</span></span>
<span data-ttu-id="7f32f-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f32f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f32f-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f32f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f32f-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="7f32f-137">INPUTS</span></span>

### <span data-ttu-id="7f32f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7f32f-138">System.String</span></span>

### <span data-ttu-id="7f32f-139">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7f32f-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7f32f-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="7f32f-140">OUTPUTS</span></span>

### <span data-ttu-id="7f32f-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7f32f-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="7f32f-142">Notas</span><span class="sxs-lookup"><span data-stu-id="7f32f-142">NOTES</span></span>

## <span data-ttu-id="7f32f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f32f-143">RELATED LINKS</span></span>

[<span data-ttu-id="7f32f-144">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7f32f-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="7f32f-145">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7f32f-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


