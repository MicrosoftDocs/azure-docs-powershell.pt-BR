---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: cd61e2119ea84ccfc5fb6a7f5fe597e80c9fd417
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112422"
---
# <span data-ttu-id="6f185-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6f185-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="6f185-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f185-102">SYNOPSIS</span></span>
<span data-ttu-id="6f185-103">Cria um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="6f185-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="6f185-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f185-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f185-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6f185-105">DESCRIPTION</span></span>
<span data-ttu-id="6f185-106">O cmdlet **New-AzAvailabilitySet** cria um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="6f185-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="6f185-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f185-107">EXAMPLES</span></span>

### <span data-ttu-id="6f185-108">Exemplo 1: criar um conjunto de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="6f185-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="6f185-109">Esse comando cria um conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6f185-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="6f185-110">OS</span><span class="sxs-lookup"><span data-stu-id="6f185-110">PARAMETERS</span></span>

### <span data-ttu-id="6f185-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f185-111">-AsJob</span></span>
<span data-ttu-id="6f185-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="6f185-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6f185-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f185-113">-DefaultProfile</span></span>
<span data-ttu-id="6f185-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f185-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f185-115">-Local</span><span class="sxs-lookup"><span data-stu-id="6f185-115">-Location</span></span>
<span data-ttu-id="6f185-116">Especifica o local para o conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="6f185-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="6f185-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6f185-117">-Name</span></span>
<span data-ttu-id="6f185-118">Especifica um nome para o conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="6f185-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="6f185-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="6f185-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="6f185-120">Especifica a contagem de domínios com falha na plataforma.</span><span class="sxs-lookup"><span data-stu-id="6f185-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="6f185-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="6f185-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="6f185-122">Especifica a contagem de domínios de atualização de plataforma.</span><span class="sxs-lookup"><span data-stu-id="6f185-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="6f185-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="6f185-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="6f185-124">A ID do recurso do grupo de posicionamento de proximidade a ser usado com esse conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="6f185-124">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="6f185-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f185-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f185-126">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6f185-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6f185-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="6f185-127">-Sku</span></span>
<span data-ttu-id="6f185-128">O nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="6f185-128">The Name of Sku.</span></span>
<span data-ttu-id="6f185-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6f185-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6f185-130">Alinhado: para discos gerenciados</span><span class="sxs-lookup"><span data-stu-id="6f185-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="6f185-131">Clássico: para discos não gerenciados</span><span class="sxs-lookup"><span data-stu-id="6f185-131">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="6f185-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="6f185-132">-Tag</span></span>
<span data-ttu-id="6f185-133">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6f185-133">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="6f185-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f185-134">CommonParameters</span></span>
<span data-ttu-id="6f185-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f185-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f185-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f185-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f185-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6f185-137">INPUTS</span></span>

### <span data-ttu-id="6f185-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6f185-138">System.String</span></span>

### <span data-ttu-id="6f185-139">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6f185-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6f185-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6f185-140">OUTPUTS</span></span>

### <span data-ttu-id="6f185-141">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6f185-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="6f185-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6f185-142">NOTES</span></span>

## <span data-ttu-id="6f185-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f185-143">RELATED LINKS</span></span>

[<span data-ttu-id="6f185-144">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6f185-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="6f185-145">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6f185-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


