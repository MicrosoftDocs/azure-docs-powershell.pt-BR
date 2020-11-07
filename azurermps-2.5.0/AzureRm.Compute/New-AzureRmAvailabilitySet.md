---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: f08de8d1ea5f157270617c69a2092764d0ad4657
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785372"
---
# <span data-ttu-id="2724e-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2724e-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="2724e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2724e-102">SYNOPSIS</span></span>
<span data-ttu-id="2724e-103">Cria um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="2724e-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2724e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2724e-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2724e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2724e-105">DESCRIPTION</span></span>
<span data-ttu-id="2724e-106">O cmdlet **New-AzureRmAvailabilitySet** cria um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="2724e-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="2724e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2724e-107">EXAMPLES</span></span>

### <span data-ttu-id="2724e-108">Exemplo 1: criar um conjunto de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="2724e-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="2724e-109">Esse comando cria um conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2724e-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="2724e-110">OS</span><span class="sxs-lookup"><span data-stu-id="2724e-110">PARAMETERS</span></span>

### <span data-ttu-id="2724e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2724e-111">-AsJob</span></span>
<span data-ttu-id="2724e-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="2724e-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2724e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2724e-113">-DefaultProfile</span></span>
<span data-ttu-id="2724e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2724e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2724e-115">-Local</span><span class="sxs-lookup"><span data-stu-id="2724e-115">-Location</span></span>
<span data-ttu-id="2724e-116">Especifica o local para o conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="2724e-116">Specifies the location for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2724e-117">Gerenciados por</span><span class="sxs-lookup"><span data-stu-id="2724e-117">-Managed</span></span>
<span data-ttu-id="2724e-118">Conjunto de disponibilidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="2724e-118">Managed Availability Set</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2724e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2724e-119">-Name</span></span>
<span data-ttu-id="2724e-120">Especifica um nome para o conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="2724e-120">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2724e-121">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="2724e-121">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="2724e-122">Especifica a contagem de domínios com falha na plataforma.</span><span class="sxs-lookup"><span data-stu-id="2724e-122">Specifies the platform fault domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2724e-123">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="2724e-123">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="2724e-124">Especifica a contagem de domínios de atualização de plataforma.</span><span class="sxs-lookup"><span data-stu-id="2724e-124">Specifies the platform update domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2724e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2724e-125">-ResourceGroupName</span></span>
<span data-ttu-id="2724e-126">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2724e-126">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2724e-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="2724e-127">-Sku</span></span>
<span data-ttu-id="2724e-128">O nome do SKU</span><span class="sxs-lookup"><span data-stu-id="2724e-128">The Name of Sku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2724e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2724e-129">CommonParameters</span></span>
<span data-ttu-id="2724e-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2724e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2724e-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2724e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2724e-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2724e-132">INPUTS</span></span>

### <span data-ttu-id="2724e-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2724e-133">None</span></span>
<span data-ttu-id="2724e-134">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="2724e-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2724e-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2724e-135">OUTPUTS</span></span>

### <span data-ttu-id="2724e-136">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2724e-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="2724e-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2724e-137">NOTES</span></span>

## <span data-ttu-id="2724e-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2724e-138">RELATED LINKS</span></span>

[<span data-ttu-id="2724e-139">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2724e-139">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="2724e-140">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2724e-140">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


