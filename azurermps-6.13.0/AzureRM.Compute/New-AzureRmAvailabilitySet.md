---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5a1d583d9eee535f519b6748867b4026dcc45006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610099"
---
# <span data-ttu-id="5079b-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5079b-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="5079b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5079b-102">SYNOPSIS</span></span>
<span data-ttu-id="5079b-103">Cria um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="5079b-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5079b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5079b-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5079b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5079b-105">DESCRIPTION</span></span>
<span data-ttu-id="5079b-106">O cmdlet **New-AzureRmAvailabilitySet** cria um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="5079b-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="5079b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5079b-107">EXAMPLES</span></span>

### <span data-ttu-id="5079b-108">Exemplo 1: criar um conjunto de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="5079b-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="5079b-109">Esse comando cria um conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5079b-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="5079b-110">OS</span><span class="sxs-lookup"><span data-stu-id="5079b-110">PARAMETERS</span></span>

### <span data-ttu-id="5079b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5079b-111">-AsJob</span></span>
<span data-ttu-id="5079b-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="5079b-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5079b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5079b-113">-DefaultProfile</span></span>
<span data-ttu-id="5079b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5079b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5079b-115">-Local</span><span class="sxs-lookup"><span data-stu-id="5079b-115">-Location</span></span>
<span data-ttu-id="5079b-116">Especifica o local para o conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="5079b-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="5079b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5079b-117">-Name</span></span>
<span data-ttu-id="5079b-118">Especifica um nome para o conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="5079b-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="5079b-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="5079b-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="5079b-120">Especifica a contagem de domínios com falha na plataforma.</span><span class="sxs-lookup"><span data-stu-id="5079b-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="5079b-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="5079b-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="5079b-122">Especifica a contagem de domínios de atualização de plataforma.</span><span class="sxs-lookup"><span data-stu-id="5079b-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="5079b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5079b-123">-ResourceGroupName</span></span>
<span data-ttu-id="5079b-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5079b-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5079b-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="5079b-125">-Sku</span></span>
<span data-ttu-id="5079b-126">O nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="5079b-126">The Name of Sku.</span></span>
<span data-ttu-id="5079b-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="5079b-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5079b-128">Alinhado: para discos gerenciados</span><span class="sxs-lookup"><span data-stu-id="5079b-128">Aligned: For managed disks</span></span>
- <span data-ttu-id="5079b-129">Clássico: para discos não gerenciados</span><span class="sxs-lookup"><span data-stu-id="5079b-129">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="5079b-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="5079b-130">-Tag</span></span>
<span data-ttu-id="5079b-131">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5079b-131">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="5079b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5079b-132">CommonParameters</span></span>
<span data-ttu-id="5079b-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5079b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5079b-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5079b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5079b-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5079b-135">INPUTS</span></span>

### <span data-ttu-id="5079b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5079b-136">System.String</span></span>

### <span data-ttu-id="5079b-137">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5079b-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="5079b-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5079b-138">OUTPUTS</span></span>

### <span data-ttu-id="5079b-139">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5079b-139">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="5079b-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5079b-140">NOTES</span></span>

## <span data-ttu-id="5079b-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5079b-141">RELATED LINKS</span></span>

[<span data-ttu-id="5079b-142">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5079b-142">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="5079b-143">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5079b-143">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


